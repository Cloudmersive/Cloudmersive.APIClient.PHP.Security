# Swagger\Client\ContentThreatDetectionApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contentThreatDetectionAutomaticThreatDetectionString**](ContentThreatDetectionApi.md#contentThreatDetectionAutomaticThreatDetectionString) | **POST** /security/threat-detection/content/automatic/detect/string | Automatically detect threats in an input string
[**contentThreatDetectionCheckSqlInjectionString**](ContentThreatDetectionApi.md#contentThreatDetectionCheckSqlInjectionString) | **POST** /security/threat-detection/content/sql-injection/detect/string | Check text input for SQL Injection (SQLI) attacks
[**contentThreatDetectionCheckXxe**](ContentThreatDetectionApi.md#contentThreatDetectionCheckXxe) | **POST** /security/threat-detection/content/xxe/detect/xml/string | Protect text input from XML External Entity (XXE) attacks
[**contentThreatDetectionDetectInsecureDeserializationJsonString**](ContentThreatDetectionApi.md#contentThreatDetectionDetectInsecureDeserializationJsonString) | **POST** /security/threat-detection/content/insecure-deserialization/json/detect/string | Detect Insecure Deserialization JSON (JID) attacks in a string
[**contentThreatDetectionProtectXss**](ContentThreatDetectionApi.md#contentThreatDetectionProtectXss) | **POST** /security/threat-detection/content/xss/detect/string | Protect text input from Cross-Site-Scripting (XSS) attacks through normalization


# **contentThreatDetectionAutomaticThreatDetectionString**
> \Swagger\Client\Model\StringAutomaticThreatDetection contentThreatDetectionAutomaticThreatDetectionString($value)

Automatically detect threats in an input string

Auto-detects a wide range of threat types in input string, including Cross-Site Scripting (XSS), SQL Injection (SQLI), XML External Entitites (XXE), Server-side Request Forgeries (SSRF), and JSON Insecure Deserialization (JID).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContentThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | User-facing text input.

try {
    $result = $apiInstance->contentThreatDetectionAutomaticThreatDetectionString($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentThreatDetectionApi->contentThreatDetectionAutomaticThreatDetectionString: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| User-facing text input. |

### Return type

[**\Swagger\Client\Model\StringAutomaticThreatDetection**](../Model/StringAutomaticThreatDetection.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contentThreatDetectionCheckSqlInjectionString**
> \Swagger\Client\Model\StringSqlInjectionDetectionResult contentThreatDetectionCheckSqlInjectionString($value)

Check text input for SQL Injection (SQLI) attacks

Detects SQL Injection (SQLI) attacks from text input.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContentThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | User-facing text input.

try {
    $result = $apiInstance->contentThreatDetectionCheckSqlInjectionString($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentThreatDetectionApi->contentThreatDetectionCheckSqlInjectionString: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| User-facing text input. |

### Return type

[**\Swagger\Client\Model\StringSqlInjectionDetectionResult**](../Model/StringSqlInjectionDetectionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contentThreatDetectionCheckXxe**
> \Swagger\Client\Model\StringXxeDetectionResult contentThreatDetectionCheckXxe($value)

Protect text input from XML External Entity (XXE) attacks

Detects XXE (XML External Entity) attacks from XML text input.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContentThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | User-facing text input.

try {
    $result = $apiInstance->contentThreatDetectionCheckXxe($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentThreatDetectionApi->contentThreatDetectionCheckXxe: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| User-facing text input. |

### Return type

[**\Swagger\Client\Model\StringXxeDetectionResult**](../Model/StringXxeDetectionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contentThreatDetectionDetectInsecureDeserializationJsonString**
> \Swagger\Client\Model\StringInsecureDeserializationJsonDetection contentThreatDetectionDetectInsecureDeserializationJsonString($value)

Detect Insecure Deserialization JSON (JID) attacks in a string

Detects Insecure Deserialization JSON (JID) attacks from text input.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContentThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | User-facing text input.

try {
    $result = $apiInstance->contentThreatDetectionDetectInsecureDeserializationJsonString($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentThreatDetectionApi->contentThreatDetectionDetectInsecureDeserializationJsonString: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| User-facing text input. |

### Return type

[**\Swagger\Client\Model\StringInsecureDeserializationJsonDetection**](../Model/StringInsecureDeserializationJsonDetection.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **contentThreatDetectionProtectXss**
> \Swagger\Client\Model\StringXssProtectionResult contentThreatDetectionProtectXss($value)

Protect text input from Cross-Site-Scripting (XSS) attacks through normalization

Detects and removes XSS (Cross-Site-Scripting) attacks from text input through normalization.  Returns the normalized result, as well as information on whether the original input contained an XSS risk.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ContentThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | User-facing text input.

try {
    $result = $apiInstance->contentThreatDetectionProtectXss($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContentThreatDetectionApi->contentThreatDetectionProtectXss: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| User-facing text input. |

### Return type

[**\Swagger\Client\Model\StringXssProtectionResult**](../Model/StringXssProtectionResult.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

