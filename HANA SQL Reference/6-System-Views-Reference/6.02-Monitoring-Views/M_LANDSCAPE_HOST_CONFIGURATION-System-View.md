# 6.2.144 M_LANDSCAPE_HOST_CONFIGURATION System View

> [↑ 6.2 Monitoring Views](README.md) · Fuente: *SAP HANA SQL Reference Guide for SAP HANA Platform (SAP HANA Platform 2.0)*, páginas 1842–1846

Specifies the host roles in a distributed landscape.

## Structure

| **Column name** | **Data type** | **Description** |
| --- | --- | --- |
| HOST | VARCHAR(64) | Displays the host name. |
| HOST_ACTIVE | VARCHAR(128) | Displays the host active status which is a summary of the active values of all the services on that host. |
| HOST_STATUS | VARCHAR(128) | Displays the host status:<br>**OK**<br>The host is operational; the host actual role equals the configured role. **IGNORE**<br>The host is operational; the host configured as standby is available, but not used. **INFO**<br>The host is operational; the host actual role is different from the configured role. **WARNING**<br>The host is not operational; the host should become operational after startup/failover. **ERROR**<br>The host not operational; the host is in an erroneous state. |
| FAILOVER_STATUS | VARCHAR(128) | Displays the failover status:<br>**(empty value)**<br>No failover is pending or active. **waiting .. sec**<br>A failure is detected. Waiting is required to prevent an unnecessary failover. A restart of another host does not trigger an immediate fail over. **waiting**<br>A failure is detected. Waiting for another starting host. **failover to 'host'**<br>Failover to an active host named 'host'. **failback to 'host'**<br>Failback to worker host active. This happens when a standby host was assigned and is stopped. There is no automatic failback while the standby host is assigned because this would cause downtime. **failed**<br>The failover failed. See `nameserver.trc` for details |
| FAILOVER_GROUP | VARCHAR(256) | Deprecated. This has been replaced by the FAILOVER_..._GROUP columns. |
| FAILOVER_CONFIG_GROUP | VARCHAR(256) | Displays the configured failover group.<br>Hosts can be grouped and during fail over a host is looked for within the same group. If no host is available in the same group, hosts from other groups are used. |
| FAILOVER_ACTUAL_GROUP | VARCHAR(256) | Displays the actual failover group. |
| NAMESERVER_CONFIG_ROLE | VARCHAR(16) | Displays the nameserver configured roles: MASTER/SLAVE. During installation, up to 3 hosts are automatically configured as MASTER candidates. All others are SLAVE. |
| NAMESERVER_ACTUAL_ROLE | VARCHAR(16) | Displays the nameserver actual roles: MASTER/SLAVE. Exactly one of the master candidates is MASTER and all others are SLAVE.<br>The MASTER name server and MASTER index server are both on the same host. |
| INDEXSERVER_CONFIG_ROLE | VARCHAR(16) | Displays the indexserver configured roles: WORKER/STANDBY.<br>During SAP HANA system installation or host addition, hosts can be assigned the SAP HANA server roles WORKER or STANDBY. The host can also be as signed other roles. |
| INDEXSERVER_ACTUAL_ROLE | VARCHAR(16) | Displays the indexserver roles: MAS TER, SLAVE, or STANDBY. Exactly one host is MASTER and all others are SLAVE or STANDBY. |
| HOST_CONFIG_ROLES | VARCHAR(64) | Displays the host's configured database and SAP HANA option roles: ETS_WORKER, ETS_STANDBY, EXTENDED_STORAGE_WORKER, EXTENDED_STORAGE_STANDBY, STANDBY, STREAMING, WORKER, XS_WORKER, or XS_STANDBY. |
| HOST_ACTUAL_ROLES | VARCHAR(64) | Displays the host's current database and SAP HANA option roles (these may change due to host auto-failover): ETS_WORKER, ETS_STANDBY, EXTENDED_STORAGE_WORKER, EXTENDED_STORAGE_STANDBY, STANDBY, STREAMING, WORKER, XS_WORKER, or XS_STANDBY. |
| STORAGE_PARTITION | - | Deprecated. This has been replaced by the STORAGE_CONFIG_PARTITION, and STORAGE_ACTUAL_PARTITION columns. |
| STORAGE_CONFIG_PARTITION | INTEGER | Displays the stable subpath to reassign the same storage partition after fail overs. |
| STORAGE_ACTUAL_PARTITION | INTEGER | Displays the unique number of the mount sub-directory used by the host for storing data and logs (also known as the "subpath"). |
| WORKER_CONFIG_GROUPS | VARCHAR(256) | Displays the stable classification values to assign hosts to logical worker groups. |
| WORKER_ACTUAL_GROUPS | VARCHAR(256) | Displays the current classification values to assign hosts to logical worker groups. |
| REMOVE_STATUS | VARCHAR(16) | Removes progress information. |
