# # DocumentRenderOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **string** |  | [optional] [default to 'tpl_modern']
**template_version** | **int** |  | [optional]
**page_size** | **string** |  | [optional] [default to 'LETTER']
**expires_in** | **int** | How long the render stays downloadable, in seconds (1 minute to 7 days). It is also the lifetime of the signature in &#x60;download_url&#x60;, which is why it is bounded: an unbounded value meant an unbounded grant. A value below the floor used to be accepted and produced a render that had already expired. | [optional] [default to 3600]
**format** | **string** | &#x60;facturx_pdf&#x60; embeds the EN 16931 CII XML in a PDF/A-3, which is what a French or German counterparty means by Factur-X or ZUGFeRD. | [optional] [default to 'pdf']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
