# # RecurringInvoiceCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**business_profile_id** | **string** |  |
**customer_id** | **string** |  |
**frequency** | **string** | daily, weekly, monthly, quarterly, or yearly |
**interval** | **int** | Every N periods | [optional] [default to 1]
**start_date** | **\DateTime** | Date of the first invoice |
**end_date** | **\DateTime** |  | [optional]
**max_occurrences** | **int** |  | [optional]
**numbering_sequence_id** | **string** |  | [optional]
**auto_finalize** | **bool** | Automatically finalize generated invoices | [optional] [default to false]
**invoice_template** | [**\InvoicePDFs\Model\InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
