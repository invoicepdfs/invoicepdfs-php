# # DocumentInvoiceDataInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_number** | **string** |  |
**issue_date** | **\DateTime** |  |
**due_date** | **\DateTime** |  | [optional]
**currency** | **string** |  |
**seller** | [**\OpenAPI\Client\Model\DocumentPartyInput**](DocumentPartyInput.md) |  |
**buyer** | [**\OpenAPI\Client\Model\DocumentPartyInput**](DocumentPartyInput.md) |  |
**ship_to** | [**\OpenAPI\Client\Model\DocumentPartyInput**](DocumentPartyInput.md) |  | [optional]
**line_items** | [**\OpenAPI\Client\Model\DocumentLineItemInput[]**](DocumentLineItemInput.md) |  |
**discounts** | [**\OpenAPI\Client\Model\DocumentDiscountInput[]**](DocumentDiscountInput.md) |  | [optional]
**shipping** | [**\OpenAPI\Client\Model\DocumentShippingInput**](DocumentShippingInput.md) |  | [optional]
**custom_fields** | [**\OpenAPI\Client\Model\DocumentCustomFieldInput[]**](DocumentCustomFieldInput.md) |  | [optional]
**payment** | [**\OpenAPI\Client\Model\DocumentPaymentInput**](DocumentPaymentInput.md) |  | [optional]
**branding** | [**\OpenAPI\Client\Model\DocumentBrandingInput**](DocumentBrandingInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
