[Back](../../Readme.md)

# Update records

> POST http://172.104.142.164:8080/sanarip-tamga/ws/rest/:model/:id

Этот запрос схож **Save**-ом, его отличия в том что, нужно ещё передать версию записи
"version" : число

Например  
После создании записи у него версия будет "**0**", при обновлении записи нужно в теле запроса добавить

> POST http://172.104.142.164:8080/sanarip-tamga/ws/rest/com.axelor.apps.sale.db.Declaration/1

`Тело запроса:`

```json
{
  "data": {
    "version": 0,
    "piType": 1,
    "creationDate": "2022-01-01",
    "company": {
      "id": 1
    },
    "arrivalLocation": {
      "id": 1
    },
    "personType": "CARRIER"
  }
}
```

`Ответ:`

```json
{
  "status": 0,
  "data": [
    {
      "destinationCodeGoods": null,
      "motivatedAnswerFito": null,
      "carrierPartner": null,
      "periodicityTypeSelect": 2,
      "transitTransportMeans": null,
      "transportMeansQuantity": null,
      "mainInvoicingAddressStr": null,
      "deliveryCondition": null,
      "nextInvoicingEndPeriodDate": null,
      "statusFitoView": 2,
      "invoicedPartner": null,
      "groupProductsOnPrintings": false,
      "opportunity": null,
      "signTransportationTirCarnet": false,
      "taxNumber": null,
      "updatedOn": "2023-02-16T09:51:34.017Z",
      "version": 2,
      "isToPrintLineSubTotal": false,
      "$wkfStatus": null,
      "externalReference": "CF-2014-342",
      "deliveredPartner": null,
      "countCargoSpaces": 0,
      "publicVET": false,
      "signOfAvailability": false,
      "confirmationDateTime": null,
      "routePointId": [],
      "stockLocation": null,
      "computationDate": null,
      "advancePaymentList": [],
      "createdByInterco": false,
      "proformaComments": null,
      "piCreateDate": null,
      "declarationLineList": [],
      "timetableList": [],
      "cancelReasonStr": null,
      "currency": {
        "code": "EUR",
        "name": "Euro",
        "id": 46,
        "$version": 0
      },
      "cancelReason": null,
      "countProducts": 0,
      "personType": "CARRIER",
      "countShippingSpecifications": 0,
      "trailedVehicleId": [],
      "toInvoiceViaTask": false,
      "blockedOnCustCreditExceed": false,
      "attachmentFileMinTrans": null,
      "stockMoveList": [],
      "team": {
        "code": "NTH",
        "name": "North",
        "id": 1,
        "$version": 0
      },
      "broker": null,
      "statusSelect": 2,
      "specificNotes": null,
      "declarationSeq": null,
      "manualUnblock": false,
      "pickingOrderComments": null,
      "statusMinTrans": 0,
      "orderNumber": null,
      "companyExTaxTotal": "0.00",
      "taxTotal": "0.00",
      "project": null,
      "totalGrossMargin": "0",
      "transportMeansRegId": null,
      "attachmentFile": null,
      "weightValue": null,
      "nameVehicle": null,
      "noticePeriodInDays": 0,
      "transportMeansEntryPurposeCode": null,
      "productionNote": null,
      "permissionToCarryOutCargoTransportationId": [],
      "customsTransitEnforcementMeasure": [],
      "countryCodeId": null,
      "isTacitAgreement": false,
      "inTaxTotal": "0.00",
      "declarationLineTaxList": [],
      "subscriptionText": null,
      "nextInvoicingDate": null,
      "attachmentFileGTS": null,
      "arrivalLocation": {
        "$t:name": "МПТП ТОРУГАРТ",
        "name": "MPTP TORUGART",
        "id": 1,
        "$version": 0
      },
      "advancePaymentAmountNeeded": "0.00",
      "templateUser": null,
      "electronicSignature": null,
      "carrierReps": [],
      "endOfValidityDate": null,
      "orderDate": null,
      "transportTypeCode": null,
      "nextInvPeriodStartDate": null,
      "registrationNumberTirCarnet": null,
      "statusVet": 0,
      "description": null,
      "motivatedGTS": null,
      "inAti": false,
      "title": null,
      "priceList": null,
      "duration": null,
      "preliminaryInformationUsageCode": null,
      "countShippingSpecificationSheets": 0,
      "marginRate": "0",
      "toStockLocation": null,
      "company": {
        "code": "AXE",
        "name": "Axelor",
        "id": 1,
        "$version": 2
      },
      "deliveryAddressStr": null,
      "vehicleId": null,
      "nextInvoicingStartPeriodDate": null,
      "declarationType": "TT",
      "paymentMode": null,
      "specificPackage": null,
      "contractEndDate": null,
      "fullName": "123 Services",
      "salespersonUser": {
        "code": "democrm",
        "fullName": "Charles DEMOCRM",
        "id": 9,
        "$version": 0
      },
      "vehicleModelName": null,
      "amountInvoiced": "0.00",
      "salespersonUserMinTrans": null,
      "createdBy": {
        "code": "admin",
        "fullName": "Admin",
        "id": 1,
        "$version": 4
      },
      "advancePaymentNeeded": false,
      "deliveryState": 1,
      "salespersonUserVet": null,
      "interco": false,
      "deliveryComments": null,
      "declarationScheduleLineList": [],
      "expectedRealisationDate": null,
      "vehicleBodyId": null,
      "customsTransitDeclaration": null,
      "statusMinTransView": 2,
      "deliveryAddress": {
        "fullName": " 40 RUE ABELARD 59000 LILLE",
        "id": 58,
        "$version": 0
      },
      "railwayStationCalendarStamp": null,
      "id": 1,
      "companyCostTotal": "0.00",
      "attrs": null,
      "salespersonUserFito": null,
      "cargoOperations": [],
      "vehicleChassisId": null,
      "motivatedGsen": null,
      "invoicedFirstDate": null,
      "template": false,
      "currentContractPeriodEndDate": null,
      "otherPersonText": null,
      "numberOfPeriods": 1,
      "contractPeriodInMonths": 0,
      "createdOn": "2023-02-16T07:41:08.647Z",
      "statusGts": 0,
      "publicMinTrans": false,
      "statusFito": 0,
      "motivatedMinTrans": null,
      "registrationNumberPreliminaryInformation": null,
      "isIspmRequired": false,
      "contactPartner": {
        "fullNameParties": "null - Jean Marc - null",
        "id": 15,
        "$version": 3
      },
      "deliveryDate": null,
      "statusGsenView": 2,
      "lastReminderDate": null,
      "totalCostPrice": "0",
      "tradingName": null,
      "statusGsen": 0,
      "subscriptionComment": null,
      "motivatedAnswer": null,
      "hideDiscount": false,
      "statusVetView": 2,
      "companyBankDetails": null,
      "standardDelay": 0,
      "importId": "6",
      "nameTransportCode": null,
      "internalNote": null,
      "salespersonUserGts": null,
      "fiscalPosition": null,
      "arrivalLocationArrivalDateTime": null,
      "isNeedingConformityCertificate": false,
      "advanceTotal": "0.00",
      "vehicleMakeName": null,
      "oneoffSale": false,
      "attachmentFileGsen": null,
      "statusGtsView": 2,
      "invoiceComments": null,
      "freightCarrierMode": null,
      "selected": false,
      "processInstanceId": null,
      "orderBeingEdited": false,
      "otherVehicle": null,
      "updatedBy": {
        "code": "admin",
        "fullName": "Admin",
        "id": 1,
        "$version": 4
      },
      "codeFeaturesTransitTransportMeans": null,
      "markup": "0",
      "contractStartDate": null,
      "creationDate": "2022-01-01",
      "mainInvoicingAddress": {
        "fullName": " 40 RUE ABELARD 59000 LILLE",
        "id": 58,
        "$version": 0
      },
      "sparePartsId": [],
      "clientPartner": {
        "fullNameParties": "null - 123 Services",
        "id": 14,
        "$version": 4
      },
      "containerIndicator": false,
      "incoterm": null,
      "attachmentFileFito": null,
      "timetableTemplate": null,
      "publicGTS": false,
      "amountToBeSpreadOverTheTimetable": "0.00",
      "importOrigin": null,
      "declarationTypeSelect": 1,
      "forwarderPartner": null,
      "batchSet": [],
      "infoIdentificationMeans": null,
      "printingSettings": {
        "name": "Default print settings",
        "id": 1,
        "$version": 0
      },
      "directOrderLocation": false,
      "unifiedTransportModeCode": null,
      "salespersonUserGsen": null,
      "shipmentDate": null,
      "accountedRevenue": "0",
      "piType": 1,
      "publicGsen": false,
      "lastReminderComments": null,
      "paymentCondition": null,
      "customsAuthorityAndDestination": null,
      "exTaxTotal": "0.00",
      "shipmentMode": null,
      "versionNumber": 1,
      "confirmedByUser": null,
      "nameModeCode": null,
      "publicFito": false
    }
  ]
}
```

# Вкладки

##  №1

`Тело запроса:`

```json
{
  "data": {
    "version": 0,
    "piType": 1,
    "creationDate": "2022-01-01",
    "company": {
      "id": 1
    },
    "arrivalLocation": {
      "id": 1
    },
    "personType": "CARRIER"
  }
}
```

