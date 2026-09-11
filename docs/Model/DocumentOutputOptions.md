# # DocumentOutputOptions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | **string** |  | [optional] [default to 'pdf']
**delivery** | **string** |  | [optional] [default to 'url']
**expires_in** | **int** | How long the render stays downloadable, in seconds (1 minute to 7 days). It is also the lifetime of the signature in &#x60;download_url&#x60;, which is why it is bounded: an unbounded value meant an unbounded grant. A value below the floor used to be accepted and produced a render that had already expired. | [optional] [default to 3600]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
