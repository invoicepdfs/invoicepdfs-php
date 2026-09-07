# # ComplianceCheckOut

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile** | **string** |  |
**ruleset_version** | **string** | The version these rules came from. Worth recording alongside any document you file — rulesets revise, and &#39;which rules did this pass?&#39; is what an audit asks years later. |
**valid** | **bool** |  |
**violations** | [**\InvoicePDFs\Model\ComplianceViolationOut[]**](ComplianceViolationOut.md) | Every violation found, not the first — fixing one field per round trip is the experience this avoids. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
