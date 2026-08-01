# # DocumentCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**document_type** | **string** |  | [optional] [default to 'invoice']
**number** | **string** |  |
**issue_date** | **\DateTime** |  |
**due_date** | **\DateTime** |  | [optional]
**currency** | **string** |  |
**locale** | **string** |  | [optional]
**business_profile_id** | **string** |  |
**customer_id** | **string** |  |
**source_document_id** | **string** |  | [optional]
**reason** | **string** |  | [optional]
**ship_to** | [**\InvoicePDFs\Model\PostalAddress**](PostalAddress.md) |  | [optional]
**line_items** | [**\InvoicePDFs\Model\StandardLineItemInput[]**](StandardLineItemInput.md) |  |
**discounts** | [**\InvoicePDFs\Model\LineItemDiscountInput[]**](LineItemDiscountInput.md) |  | [optional]
**shipping** | [**\InvoicePDFs\Model\InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional]
**notes** | [**\InvoicePDFs\Model\InvoiceNoteInput[]**](InvoiceNoteInput.md) |  | [optional]
**terms** | [**\InvoicePDFs\Model\InvoiceTermInput[]**](InvoiceTermInput.md) |  | [optional]
**custom_fields** | [**\InvoicePDFs\Model\InvoiceCustomFieldInput[]**](InvoiceCustomFieldInput.md) |  | [optional]
**payment** | [**\InvoicePDFs\Model\InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional]
**branding** | [**\InvoicePDFs\Model\InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
