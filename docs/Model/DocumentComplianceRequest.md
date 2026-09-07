# # DocumentComplianceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_type** | **string** |  | [optional] [default to 'invoice']
**data** | [**\InvoicePDFs\Model\DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  |
**profile** | **string** | Which ruleset to hold the document to. Rulesets differ: a document valid under one can be rejected by another, so there is no default. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
