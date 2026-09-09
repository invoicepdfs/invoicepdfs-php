# # ComplianceRulesetOut

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  |
**label** | **string** |  |
**version** | **string** | The upstream release of the rules. Empty for checks with no version of their own. | [optional] [default to '']
**ran** | **bool** | False when this ruleset could not be run at all. A ruleset that did not run is not a pass — &#x60;valid&#x60; only reports what was checked. |
**reason** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
