# # ComplianceViolationOut

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rule** | **string** | The identifier the standard uses — a business term from the mandatory-field check, a rule id from Schematron. A rule id is what a rejection notice from an access point quotes. |
**path** | **string** | Where the problem is. The mandatory-field check names a field of the request; Schematron names the node in the generated XML. |
**message** | **string** |  |
**severity** | **string** | &#x60;fatal&#x60; would get the document rejected. &#x60;warning&#x60; is a recommendation — both EN 16931 and Peppol grade a large share of their rules as advisory, and &#x60;valid&#x60; ignores those. | [optional] [default to 'fatal']
**ruleset** | **string** | Which ruleset found it — matches an &#x60;id&#x60; in &#x60;rulesets&#x60;. | [optional] [default to 'semantic']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
