# # RenderComplianceOut

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile** | **string** | The ruleset this document was built and validated against. |
**ruleset_version** | **string** | The artefact versions the check actually ran. A profile is held to more than one ruleset, and they are regenerated over time, so this is what makes &#39;which rules did this pass?&#39; answerable later. |
**fully_checked** | **bool** | False when a ruleset could not run. The document still satisfied everything that did, but the authoritative Schematron tier being absent is a materially weaker statement than it passing. |
**advisories** | [**\InvoicePDFs\Model\ComplianceViolationOut[]**](ComplianceViolationOut.md) | Non-fatal findings the render proceeded past. Both rulesets grade a large share of their rules as advisory, so these are worth reading and are not a rejection. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
