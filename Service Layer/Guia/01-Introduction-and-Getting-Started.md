# 1–2. Introduction and Getting Started

> Source: *Working with SAP Business One Service Layer*, user guide v1.29 (2026-07-27), chapters 1–2. Technical reference written for developers/agents; content restructured and paraphrased.
>
> **Resumen (ES):** qué es el Service Layer, para quién es esta guía, requisitos, arquitectura y opciones de instalación.

## 1. What is SAP Business One Service Layer

Service Layer (SL) is the web API for SAP Business One data and services. It is built on HTTP and **OData**, and exposes the complete business objects (the same ones you get through DI API) from a scalable, highly available web server.

| Aspect | Detail | Detalle (ES) |
|---|---|---|
| Protocols | OData v3 and OData v4 | OData v3 y v4 |
| OData v3 root | `/b1s/v1/` (metadata at `/b1s/v1/$metadata`) | Raíz OData v3 |
| OData v4 root | `/b1s/v2/` (metadata at `/b1s/v2/$metadata`) | Raíz OData v4 (recomendada) |
| Payload format | JSON | Formato JSON |
| Client libraries mentioned | WCF (.NET), data.js (JavaScript) — any HTTP client works | Cualquier cliente HTTP sirve |
| Intended readers | Add-on/integration developers, admins doing load balancing, performance and stability tuning | Desarrolladores de integraciones/add-ons y administradores |

## 2.1 System requirements

- Runs on **SUSE Linux Enterprise** and, since SAP Business One 10.0 PL01, on **Microsoft Windows**.
- It is an application server built on top of the **Apache HTTP Server**.
- Two deployment modes:

| Mode | Description | Descripción (ES) |
|---|---|---|
| Integrated | Installed on the same machine as the database server, simplest landscape | En el mismo servidor de base de datos |
| Distributed | Installed on separate machines to get more CPU for high concurrency | En máquinas separadas, más capacidad |

Hardware sizing (RAM, CPU cores) follows the SAP HANA hardware specifications and the *Hardware Requirements Guide for SAP Business One*. Platform support is in the Platform Support Matrix / Product Availability Matrix and the Administrator's Guides (SQL Server and HANA versions).

## 2.2 Architecture

Three tiers: **client → web server (Service Layer) → database**. Inside the web server:

| Component | Role | Función (ES) |
|---|---|---|
| OData Parser | Reads URL + HTTP verb (GET/POST/PATCH/DELETE), maps them to the business object and CRUD method; converts the object result back into HTTP status + JSON | Traduce URL/verbo a operación sobre el objeto y la respuesta a JSON |
| DI Core | Same core used by DI API to access objects and services. **SL and DI API share object and property definitions**, so DI API knowledge transfers directly | Mismo núcleo que la DI API: mismos objetos y propiedades |
| Session manager | Implements session stickiness together with the load balancer, so one client is served by the same node | Afinidad de sesión con el balanceador |
| OBServer | Business logic engine (tax calculation, postings, etc.). SL scales by multi-processing | Lógica de negocio (impuestos, contabilizaciones) |

Recommended: several SL instances behind a load balancer. Benefits: requests run in parallel on different instances; in distributed mode, if a host fails, requests are re-dispatched to a live node **without forcing the user to log in again**.

## 2.3 Installation topology

- SL uses **Apache as load balancer**; behind it are the *load balancer members* (SL worker nodes).
- Traffic **between the load balancer and its members is plain HTTP** (not HTTPS) → configure each member's firewall so it only accepts connections from the load balancer.

| Topology | Notes | Notas (ES) |
|---|---|---|
| **Recommended:** load balancer and all members on the same machine | Simplest | Recomendado: todo en la misma máquina |
| Load balancer and members on different machines | At least one member must be on the same machine as the load balancer | Al menos un miembro junto al balanceador |

- Remote installation is **not supported**: run the Server Components setup wizard on every server separately (e.g., LB on A, members on B and C → run setup on A, B and C).
- Details: chapter *Installing the Service Layer* in the SAP Business One Administrator's Guide (SQL / HANA).
