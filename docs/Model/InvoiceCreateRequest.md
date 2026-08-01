# # InvoiceCreateRequest

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
**ship_to** | [**\InvoicePDFs\Model\PostalAddress**](PostalAddress.md) |  | [optional]
**line_items** | [**\InvoicePDFs\Model\InvoiceLineItemInput[]**](InvoiceLineItemInput.md) |  |
**discounts** | [**\InvoicePDFs\Model\InvoiceDiscountInput[]**](InvoiceDiscountInput.md) |  | [optional]
**shipping** | [**\InvoicePDFs\Model\InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional]
**notes** | [**\InvoicePDFs\Model\InvoiceNoteInput[]**](InvoiceNoteInput.md) |  | [optional]
**terms** | [**\InvoicePDFs\Model\InvoiceTermInput[]**](InvoiceTermInput.md) |  | [optional]
**custom_fields** | [**\InvoicePDFs\Model\InvoiceCustomFieldInput[]**](InvoiceCustomFieldInput.md) |  | [optional]
**payment** | [**\InvoicePDFs\Model\InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional]
**branding** | [**\InvoicePDFs\Model\InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
