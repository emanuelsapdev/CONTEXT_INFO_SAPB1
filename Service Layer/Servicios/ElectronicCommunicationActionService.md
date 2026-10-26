# ElectronicCommunicationActionService — Servicio de acciones de comunicación electrónica

> Generated from the Service Layer `$metadata` (OData v4, `/b1s/v2/`). User-created UDFs/UDTs/UDOs removed; SAP Argentina localization UDFs (`U_B1SYS_*`) kept and marked **[Loc. AR]**. English descriptions are derived from the property names; Spanish descriptions follow SAP Business One Spanish terminology.

- **Service:** `ElectronicCommunicationActionService`
- **Descripción (ES):** Servicio de acciones de comunicación electrónica
- **Operations:** 13

> Actions are invoked with `POST /b1s/v2/<Operation>` and a JSON body whose top-level keys are the parameter names. Functions (marked *function*) are invoked with `GET /b1s/v2/<Operation>` in OData v4 (`POST` in OData v3, `/b1s/v1`).

| Operation | Kind | Returns | Description (EN) | Descripción (ES) |
|---|---|---|---|---|
| [`ElectronicCommunicationActionService_AFE_FceAction_GetByFceID`](#electroniccommunicationactionservice_afe_fceaction_getbyfceid) | action | Collection([AFEFceActionGetByFceID](../Tipos-Complejos/AFEFceActionGetByFceID.md)) | AFE Fce Action Get By Fce ID | [Loc. AR] Obtener acción FCE por ID de FCE |
| [`ElectronicCommunicationActionService_AFE_FceAction_GetPaymentData`](#electroniccommunicationactionservice_afe_fceaction_getpaymentdata) | action | Collection([AFEFceActionGetPaymentData](../Tipos-Complejos/AFEFceActionGetPaymentData.md)) | AFE Fce Action Get Payment Data | [Loc. AR] Obtener datos de pago de la FCE |
| [`ElectronicCommunicationActionService_AFE_FceAP_CheckECM2Entry`](#electroniccommunicationactionservice_afe_fceap_checkecm2entry) | action | Collection([AFEFceAPCheckECM2Entry](../Tipos-Complejos/AFEFceAPCheckECM2Entry.md)) | AFE Fce AP Check ECM 2 Entry | [Loc. AR] FCE de compras: verificar entrada de comunicación electrónica |
| [`ElectronicCommunicationActionService_AFE_FceAP_GetLatestAFIPDate`](#electroniccommunicationactionservice_afe_fceap_getlatestafipdate) | function | [AFEFceAPGetLatestAFIPDate](../Tipos-Complejos/AFEFceAPGetLatestAFIPDate.md) | AFE Fce AP Get Latest AFIP Date | [Loc. AR] FCE de compras: obtener la última fecha informada por AFIP |
| [`ElectronicCommunicationActionService_AFE_FceAR_GetDateFromTo`](#electroniccommunicationactionservice_afe_fcear_getdatefromto) | function | [AFEFceARGetDateFromTo](../Tipos-Complejos/AFEFceARGetDateFromTo.md) | AFE Fce AR Get Date From To | [Loc. AR] FCE de ventas: obtener rango de fechas |
| [`ElectronicCommunicationActionService_AFE_FceAR_GetDocuments`](#electroniccommunicationactionservice_afe_fcear_getdocuments) | function | Collection([AFEFceARGetDocuments](../Tipos-Complejos/AFEFceARGetDocuments.md)) | AFE Fce AR Get Documents | [Loc. AR] FCE de ventas: obtener documentos |
| [`ElectronicCommunicationActionService_AFE_RenumberFolioNumbers`](#electroniccommunicationactionservice_afe_renumberfolionumbers) | action | — | AFE Renumber Folio Numbers | [Loc. AR] Renumerar números de folio |
| [`ElectronicCommunicationActionService_AFE_UpdFceAPAR_GetDocuments`](#electroniccommunicationactionservice_afe_updfceapar_getdocuments) | function | Collection([AFEUpdFceAPARGetDocuments](../Tipos-Complejos/AFEUpdFceAPARGetDocuments.md)) | AFE Upd Fce APAR Get Documents | [Loc. AR] Actualizar FCE de compras/ventas: obtener documentos |
| [`ElectronicCommunicationActionService_ConfirmSuccessOfCommunication`](#electroniccommunicationactionservice_confirmsuccessofcommunication) | action | — | Confirm Success Of Communication | Confirmar éxito de la comunicación |
| [`ElectronicCommunicationActionService_GetAction`](#electroniccommunicationactionservice_getaction) | action | [ECMActionStatusData](../Tipos-Complejos/ECMActionStatusData.md) | Get Action | Obtener acción |
| [`ElectronicCommunicationActionService_ReportErrorAndContinue`](#electroniccommunicationactionservice_reporterrorandcontinue) | action | — | Report Error And Continue | Informar error y continuar |
| [`ElectronicCommunicationActionService_ReportErrorAndStop`](#electroniccommunicationactionservice_reporterrorandstop) | action | — | Report Error And Stop | Informar error y detener |
| [`ElectronicCommunicationActionService_UpdateAction`](#electroniccommunicationactionservice_updateaction) | action | — | Update Action | Actualizar acción |

## ElectronicCommunicationActionService_AFE_FceAction_GetByFceID

- **Descripción (ES):** [Loc. AR] Obtener acción FCE por ID de FCE
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_AFE_FceAction_GetByFceID`
- **Parameters:** `AFEFceID` ([AFEFceID](../Tipos-Complejos/AFEFceID.md))
- **Returns:** Collection([AFEFceActionGetByFceID](../Tipos-Complejos/AFEFceActionGetByFceID.md))

```json
{
  "AFEFceID": {
    "FceID": 0
  }
}
```

## ElectronicCommunicationActionService_AFE_FceAction_GetPaymentData

- **Descripción (ES):** [Loc. AR] Obtener datos de pago de la FCE
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_AFE_FceAction_GetPaymentData`
- **Parameters:** `ECMCodeParams` ([ECMCodeParams](../Tipos-Complejos/ECMCodeParams.md))
- **Returns:** Collection([AFEFceActionGetPaymentData](../Tipos-Complejos/AFEFceActionGetPaymentData.md))

```json
{
  "ECMCodeParams": {
    "AbsEntry": 0
  }
}
```

## ElectronicCommunicationActionService_AFE_FceAP_CheckECM2Entry

- **Descripción (ES):** [Loc. AR] FCE de compras: verificar entrada de comunicación electrónica
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_AFE_FceAP_CheckECM2Entry`
- **Parameters:** `AFEFceAPCheckECM2EntryParams` ([AFEFceAPCheckECM2EntryParams](../Tipos-Complejos/AFEFceAPCheckECM2EntryParams.md))
- **Returns:** Collection([AFEFceAPCheckECM2Entry](../Tipos-Complejos/AFEFceAPCheckECM2Entry.md))

```json
{
  "AFEFceAPCheckECM2EntryParams": {
    "assignedID": "string",
    "docType": 0,
    "poi": "string",
    "folio": 0
  }
}
```

## ElectronicCommunicationActionService_AFE_FceAP_GetLatestAFIPDate

- **Descripción (ES):** [Loc. AR] FCE de compras: obtener la última fecha informada por AFIP
- **Request:** `GET /b1s/v2/ElectronicCommunicationActionService_AFE_FceAP_GetLatestAFIPDate`
- **Parameters:** none
- **Returns:** [AFEFceAPGetLatestAFIPDate](../Tipos-Complejos/AFEFceAPGetLatestAFIPDate.md)

## ElectronicCommunicationActionService_AFE_FceAR_GetDateFromTo

- **Descripción (ES):** [Loc. AR] FCE de ventas: obtener rango de fechas
- **Request:** `GET /b1s/v2/ElectronicCommunicationActionService_AFE_FceAR_GetDateFromTo`
- **Parameters:** none
- **Returns:** [AFEFceARGetDateFromTo](../Tipos-Complejos/AFEFceARGetDateFromTo.md)

## ElectronicCommunicationActionService_AFE_FceAR_GetDocuments

- **Descripción (ES):** [Loc. AR] FCE de ventas: obtener documentos
- **Request:** `GET /b1s/v2/ElectronicCommunicationActionService_AFE_FceAR_GetDocuments`
- **Parameters:** none
- **Returns:** Collection([AFEFceARGetDocuments](../Tipos-Complejos/AFEFceARGetDocuments.md))

## ElectronicCommunicationActionService_AFE_RenumberFolioNumbers

- **Descripción (ES):** [Loc. AR] Renumerar números de folio
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_AFE_RenumberFolioNumbers`
- **Parameters:** `AFERenumberFolioParams` ([AFERenumberFolioParams](../Tipos-Complejos/AFERenumberFolioParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "AFERenumberFolioParams": {
    "AbsEntry": 0,
    "NewFolioNumber": 0
  }
}
```

## ElectronicCommunicationActionService_AFE_UpdFceAPAR_GetDocuments

- **Descripción (ES):** [Loc. AR] Actualizar FCE de compras/ventas: obtener documentos
- **Request:** `GET /b1s/v2/ElectronicCommunicationActionService_AFE_UpdFceAPAR_GetDocuments`
- **Parameters:** none
- **Returns:** Collection([AFEUpdFceAPARGetDocuments](../Tipos-Complejos/AFEUpdFceAPARGetDocuments.md))

## ElectronicCommunicationActionService_ConfirmSuccessOfCommunication

- **Descripción (ES):** Confirmar éxito de la comunicación
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_ConfirmSuccessOfCommunication`
- **Parameters:** `ECMCodeParams` ([ECMCodeParams](../Tipos-Complejos/ECMCodeParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ECMCodeParams": {
    "AbsEntry": 0
  }
}
```

## ElectronicCommunicationActionService_GetAction

- **Descripción (ES):** Obtener acción
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_GetAction`
- **Parameters:** `ECMCodeParams` ([ECMCodeParams](../Tipos-Complejos/ECMCodeParams.md))
- **Returns:** [ECMActionStatusData](../Tipos-Complejos/ECMActionStatusData.md)

```json
{
  "ECMCodeParams": {
    "AbsEntry": 0
  }
}
```

## ElectronicCommunicationActionService_ReportErrorAndContinue

- **Descripción (ES):** Informar error y continuar
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_ReportErrorAndContinue`
- **Parameters:** `ECMCodeParams` ([ECMCodeParams](../Tipos-Complejos/ECMCodeParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ECMCodeParams": {
    "AbsEntry": 0
  }
}
```

## ElectronicCommunicationActionService_ReportErrorAndStop

- **Descripción (ES):** Informar error y detener
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_ReportErrorAndStop`
- **Parameters:** `ECMCodeParams` ([ECMCodeParams](../Tipos-Complejos/ECMCodeParams.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ECMCodeParams": {
    "AbsEntry": 0
  }
}
```

## ElectronicCommunicationActionService_UpdateAction

- **Descripción (ES):** Actualizar acción
- **Request:** `POST /b1s/v2/ElectronicCommunicationActionService_UpdateAction`
- **Parameters:** `ECMActionStatusData` ([ECMActionStatusData](../Tipos-Complejos/ECMActionStatusData.md))
- **Returns:** nothing (`204 No Content`)

```json
{
  "ECMActionStatusData": {
    "AbsEntry": 0,
    "ReportID": "string",
    "ReceivDate": "2026-01-31",
    "ActMessage": "string",
    ...
  }
}
```

