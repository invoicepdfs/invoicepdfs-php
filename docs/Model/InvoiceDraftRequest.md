# # InvoiceDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_number** | **string** |  |
**document_type** | **string** |  | [optional] [default to 'invoice']
**issue_date** | **\DateTime** |  |
**due_date** | **\DateTime** |  | [optional]
**currency** | **string** |  |
**locale** | **string** |  | [optional]
**business_profile_id** | **string** |  |
**customer_id** | **string** |  |
**ship_to** | [**\OpenAPI\Client\Model\PostalAddress**](PostalAddress.md) |  | [optional]
**line_items** | [**\OpenAPI\Client\Model\InvoiceLineItemInput[]**](InvoiceLineItemInput.md) |  |
**discounts** | [**\OpenAPI\Client\Model\InvoiceDiscountInput[]**](InvoiceDiscountInput.md) |  | [optional]
**shipping** | [**\OpenAPI\Client\Model\InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional]
**notes** | [**\OpenAPI\Client\Model\InvoiceNoteInput[]**](InvoiceNoteInput.md) |  | [optional]
**terms** | [**\OpenAPI\Client\Model\InvoiceTermInput[]**](InvoiceTermInput.md) |  | [optional]
**custom_fields** | [**\OpenAPI\Client\Model\InvoiceCustomFieldInput[]**](InvoiceCustomFieldInput.md) |  | [optional]
**payment** | [**\OpenAPI\Client\Model\InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional]
**branding** | [**\OpenAPI\Client\Model\InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
