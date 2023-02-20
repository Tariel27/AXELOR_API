[Back](../../Readme.md)

# One to Many

При сохранении one to many связей нужно всего лишь добавить объекты в массив

> POST || PUT http://172.104.142.164:8080/sanarip-tamga/ws/rest/:model

Пример
> POST http://172.104.142.164:8080/sanarip-tamga/ws/rest/com.axelor.apps.sale.db.Declaration

`Тело запроса:`

```json
{
  "data": {
    "piType": 1,
    "creationDate": "2022-01-01",
    "company": {
      "id": 1
    },
    "declarationLineList": [
      {
        "goodsMeasureTotalGrossMassMeasure": "3242",
        "companyExTaxTotal": "0.00",
        "consignee": {
          "id": 16
        }
      },
      {
        "goodsMeasureTotalGrossMassMeasure": "3242",
        "companyExTaxTotal": "0.00",
        "consignee": {
          "id": 16
        }
      },
      {
        "goodsMeasureTotalGrossMassMeasure": "3242",
        "companyExTaxTotal": "0.00",
        "consignee": {
          "id": 16
        }
      }
    ]
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
      "updatedOn": null,
      "version": 0,
      "isToPrintLineSubTotal": false,
      "$wkfStatus": null,
      "externalReference": null,
      "deliveredPartner": null,
      "countCargoSpaces": 0,
      "publicVET": false,
      "signOfAvailability": false,
      "confirmationDateTime": null,
      "routePointId": null,
      "stockLocation": null,
      "computationDate": null,
      "advancePaymentList": null,
      "createdByInterco": false,
      "proformaComments": null,
      "piCreateDate": null,
      "declarationLineList": [
        {
          "id": 4,
          "$version": 0
        },
        {
          "id": 5,
          "$version": 0
        },
        {
          "id": 6,
          "$version": 0
        }
      ],
      "timetableList": null,
      "cancelReasonStr": null,
      "currency": null,
      "cancelReason": null,
      "countProducts": 0,
      "personType": null,
      "countShippingSpecifications": 0,
      "trailedVehicleId": null,
      "toInvoiceViaTask": false,
      "blockedOnCustCreditExceed": false,
      "attachmentFileMinTrans": null,
      "stockMoveList": null,
      "team": null,
      "broker": null,
      "statusSelect": 0,
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
      "permissionToCarryOutCargoTransportationId": null,
      "customsTransitEnforcementMeasure": null,
      "countryCodeId": null,
      "isTacitAgreement": false,
      "inTaxTotal": "0.00",
      "declarationLineTaxList": null,
      "subscriptionText": null,
      "nextInvoicingDate": null,
      "attachmentFileGTS": null,
      "arrivalLocation": null,
      "advancePaymentAmountNeeded": "0",
      "templateUser": null,
      "electronicSignature": null,
      "carrierReps": null,
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
      "fullName": null,
      "salespersonUser": null,
      "vehicleModelName": null,
      "amountInvoiced": "0",
      "salespersonUserMinTrans": null,
      "createdBy": {
        "code": "admin",
        "fullName": "Admin",
        "id": 1,
        "$version": 5
      },
      "advancePaymentNeeded": false,
      "deliveryState": 1,
      "salespersonUserVet": null,
      "interco": false,
      "deliveryComments": null,
      "declarationScheduleLineList": null,
      "expectedRealisationDate": null,
      "vehicleBodyId": null,
      "customsTransitDeclaration": null,
      "statusMinTransView": 2,
      "deliveryAddress": null,
      "railwayStationCalendarStamp": null,
      "id": 42,
      "companyCostTotal": "0",
      "attrs": null,
      "salespersonUserFito": null,
      "cargoOperations": null,
      "vehicleChassisId": null,
      "motivatedGsen": null,
      "invoicedFirstDate": null,
      "template": false,
      "currentContractPeriodEndDate": null,
      "otherPersonText": null,
      "numberOfPeriods": 1,
      "contractPeriodInMonths": 0,
      "createdOn": "2023-02-20T11:23:20.328Z",
      "statusGts": 0,
      "publicMinTrans": false,
      "statusFito": 0,
      "motivatedMinTrans": null,
      "registrationNumberPreliminaryInformation": null,
      "isIspmRequired": false,
      "contactPartner": null,
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
      "importId": null,
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
      "updatedBy": null,
      "codeFeaturesTransitTransportMeans": null,
      "markup": "0",
      "contractStartDate": null,
      "creationDate": "2022-01-01",
      "mainInvoicingAddress": null,
      "sparePartsId": null,
      "clientPartner": null,
      "containerIndicator": false,
      "incoterm": null,
      "attachmentFileFito": null,
      "timetableTemplate": null,
      "publicGTS": false,
      "amountToBeSpreadOverTheTimetable": "0.00",
      "importOrigin": null,
      "declarationTypeSelect": 1,
      "forwarderPartner": null,
      "batchSet": null,
      "infoIdentificationMeans": null,
      "printingSettings": null,
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