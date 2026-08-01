# # InvoicePatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invoice_number** | **string** |  | [optional]
**document_type** | **string** |  | [optional]
**issue_date** | **\DateTime** |  | [optional]
**due_date** | **\DateTime** |  | [optional]
**currency** | **string** |  | [optional]
**locale** | **string** |  | [optional]
**business_profile_id** | **string** |  | [optional]
**customer_id** | **string** |  | [optional]
**ship_to** | [**\OpenAPI\Client\Model\PostalAddress**](PostalAddress.md) |  | [optional]
**line_items** | [**\OpenAPI\Client\Model\InvoiceLineItemInput[]**](InvoiceLineItemInput.md) |  | [optional]
**discounts** | [**\OpenAPI\Client\Model\InvoiceDiscountInput[]**](InvoiceDiscountInput.md) |  | [optional]
**shipping** | [**\OpenAPI\Client\Model\InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional]
**notes** | [**\OpenAPI\Client\Model\InvoiceNoteInput[]**](InvoiceNoteInput.md) |  | [optional]
**terms** | [**\OpenAPI\Client\Model\InvoiceTermInput[]**](InvoiceTermInput.md) |  | [optional]
**custom_fields** | [**\OpenAPI\Client\Model\InvoiceCustomFieldInput[]**](InvoiceCustomFieldInput.md) |  | [optional]
**payment** | [**\OpenAPI\Client\Model\InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional]
**branding** | [**\OpenAPI\Client\Model\InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
