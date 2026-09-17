# InvoicePDFs\ComplianceApi

All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**downloadDocumentXml()**](ComplianceApi.md#downloadDocumentXml) | **GET** /api/v1/documents/{document_id}/xml | Download Document Xml |
| [**renderDocumentXml()**](ComplianceApi.md#renderDocumentXml) | **POST** /api/v1/documents/xml | Render Document Xml |
| [**validateCompliance()**](ComplianceApi.md#validateCompliance) | **POST** /api/v1/documents/validate-compliance | Validate Compliance |


## `downloadDocumentXml()`

```php
downloadDocumentXml($document_id, $profile): string
```

Download Document Xml

The e-invoicing XML for a document already stored here.  Reads `data_json` directly rather than going through the render path's reconstruction: the status, the logo and the source document's number are all attached there for the *PDF*, and none of them belong in the XML. The credit note's BG-3 reference is already in the stored payload, resolved when the document was written.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ComplianceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_id = 'document_id_example'; // string
$profile = peppol_bis_billing_3; // string | Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request.

try {
    $result = $apiInstance->downloadDocumentXml($document_id, $profile);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceApi->downloadDocumentXml: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_id** | **string**|  | |
| **profile** | **string**| Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request. | |

### Return type

**string**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `renderDocumentXml()`

```php
renderDocumentXml($document_compliance_request): string
```

Render Document Xml

The e-invoicing XML for a document, without storing anything.  Takes the same body as `/validate-compliance`, and the pairing is the point: check first, then take the XML once it passes. Nothing here validates against the ruleset — a document missing mandatory fields serialises to XML missing those elements, which is a more useful artefact to look at than a refusal, and `/validate-compliance` is where the refusal belongs.  The syntax is not a parameter. It follows from the profile, because a profile already is a syntax plus a ruleset, and asking a caller for both is asking them to know that Peppol means UBL.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ComplianceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_compliance_request = new \InvoicePDFs\Model\DocumentComplianceRequest(); // \InvoicePDFs\Model\DocumentComplianceRequest

try {
    $result = $apiInstance->renderDocumentXml($document_compliance_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceApi->renderDocumentXml: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_compliance_request** | [**\InvoicePDFs\Model\DocumentComplianceRequest**](../Model/DocumentComplianceRequest.md)|  | |

### Return type

**string**

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/xml`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `validateCompliance()`

```php
validateCompliance($document_compliance_request): \InvoicePDFs\Model\DocumentComplianceResponse
```

Validate Compliance

Check a document against an e-invoicing ruleset without rendering it.  Costs no renders: nothing is stored and no PDF is produced, so a caller can check every invoice they are about to send rather than discovering the problem from a rejection weeks later.  Two tiers run, and both are reported. The mandatory-field check names a field of the request you can go and change. Schematron then serializes the document and runs the **published rules at a pinned version** over the result — the same artefacts an access point runs — so a finding here quotes the rule id a rejection notice would quote.  Read `valid` together with `fully_checked`: `valid` says nothing fatal was found, and `rulesets` says what actually ran to find it.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer authorization: HTTPBearer
$config = InvoicePDFs\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new InvoicePDFs\Api\ComplianceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$document_compliance_request = new \InvoicePDFs\Model\DocumentComplianceRequest(); // \InvoicePDFs\Model\DocumentComplianceRequest

try {
    $result = $apiInstance->validateCompliance($document_compliance_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceApi->validateCompliance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **document_compliance_request** | [**\InvoicePDFs\Model\DocumentComplianceRequest**](../Model/DocumentComplianceRequest.md)|  | |

### Return type

[**\InvoicePDFs\Model\DocumentComplianceResponse**](../Model/DocumentComplianceResponse.md)

### Authorization

[HTTPBearer](../../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
