# # DocumentInvoiceDataInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_number** | **string** |  |
**issue_date** | **\DateTime** |  |
**due_date** | **\DateTime** |  | [optional]
**currency** | **string** |  |
**seller** | [**\InvoicePDFs\Model\DocumentPartyInput**](DocumentPartyInput.md) |  |
**buyer** | [**\InvoicePDFs\Model\DocumentPartyInput**](DocumentPartyInput.md) |  |
**ship_to** | [**\InvoicePDFs\Model\DocumentPartyInput**](DocumentPartyInput.md) |  | [optional]
**line_items** | [**\InvoicePDFs\Model\DocumentLineItemInput[]**](DocumentLineItemInput.md) |  |
**discounts** | [**\InvoicePDFs\Model\DocumentDiscountInput[]**](DocumentDiscountInput.md) |  | [optional]
**shipping** | [**\InvoicePDFs\Model\DocumentShippingInput**](DocumentShippingInput.md) |  | [optional]
**custom_fields** | [**\InvoicePDFs\Model\DocumentCustomFieldInput[]**](DocumentCustomFieldInput.md) |  | [optional]
**payment** | [**\InvoicePDFs\Model\DocumentPaymentInput**](DocumentPaymentInput.md) |  | [optional]
**branding** | [**\InvoicePDFs\Model\DocumentBrandingInput**](DocumentBrandingInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
