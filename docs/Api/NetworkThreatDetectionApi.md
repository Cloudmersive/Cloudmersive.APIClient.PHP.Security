# Swagger\Client\NetworkThreatDetectionApi

All URIs are relative to *https://api.cloudmersive.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**networkThreatDetectionDetectSsrfUrl**](NetworkThreatDetectionApi.md#networkThreatDetectionDetectSsrfUrl) | **POST** /security/threat-detection/network/url/ssrf/detect | Check a URL for Server-side Request Forgery (SSRF) threats
[**networkThreatDetectionIsBot**](NetworkThreatDetectionApi.md#networkThreatDetectionIsBot) | **POST** /security/threat-detection/network/ip/is-bot | Check if IP address is a Bot client threat
[**networkThreatDetectionIsThreat**](NetworkThreatDetectionApi.md#networkThreatDetectionIsThreat) | **POST** /security/threat-detection/network/ip/is-threat | Check if IP address is a known threat
[**networkThreatDetectionIsTorNode**](NetworkThreatDetectionApi.md#networkThreatDetectionIsTorNode) | **POST** /security/threat-detection/network/ip/is-tor-node | Check if IP address is a Tor node server


# **networkThreatDetectionDetectSsrfUrl**
> \Swagger\Client\Model\UrlSsrfThreatDetectionResponseFull networkThreatDetectionDetectSsrfUrl($request)

Check a URL for Server-side Request Forgery (SSRF) threats

Checks if an input URL is at risk of being an SSRF (Server-side request forgery) threat or attack.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NetworkThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \Swagger\Client\Model\UrlSsrfThreatDetectionRequestFull(); // \Swagger\Client\Model\UrlSsrfThreatDetectionRequestFull | Input URL request

try {
    $result = $apiInstance->networkThreatDetectionDetectSsrfUrl($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NetworkThreatDetectionApi->networkThreatDetectionDetectSsrfUrl: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **request** | [**\Swagger\Client\Model\UrlSsrfThreatDetectionRequestFull**](../Model/UrlSsrfThreatDetectionRequestFull.md)| Input URL request |

### Return type

[**\Swagger\Client\Model\UrlSsrfThreatDetectionResponseFull**](../Model/UrlSsrfThreatDetectionResponseFull.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **networkThreatDetectionIsBot**
> \Swagger\Client\Model\ThreatDetectionBotCheckResponse networkThreatDetectionIsBot($value)

Check if IP address is a Bot client threat

Check if the input IP address is a Bot, robot, or otherwise a non-user entity.  Leverages real-time signals to check against known high-probability bots..

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NetworkThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | IP address to check, e.g. \"55.55.55.55\".  The input is a string so be sure to enclose it in double-quotes.

try {
    $result = $apiInstance->networkThreatDetectionIsBot($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NetworkThreatDetectionApi->networkThreatDetectionIsBot: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| IP address to check, e.g. \&quot;55.55.55.55\&quot;.  The input is a string so be sure to enclose it in double-quotes. |

### Return type

[**\Swagger\Client\Model\ThreatDetectionBotCheckResponse**](../Model/ThreatDetectionBotCheckResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **networkThreatDetectionIsThreat**
> \Swagger\Client\Model\IPThreatDetectionResponse networkThreatDetectionIsThreat($value)

Check if IP address is a known threat

Check if the input IP address is a known threat IP address.  Checks against known bad IPs, botnets, compromised servers, and other lists of threats.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NetworkThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | IP address to check, e.g. \"55.55.55.55\".  The input is a string so be sure to enclose it in double-quotes.

try {
    $result = $apiInstance->networkThreatDetectionIsThreat($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NetworkThreatDetectionApi->networkThreatDetectionIsThreat: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| IP address to check, e.g. \&quot;55.55.55.55\&quot;.  The input is a string so be sure to enclose it in double-quotes. |

### Return type

[**\Swagger\Client\Model\IPThreatDetectionResponse**](../Model/IPThreatDetectionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **networkThreatDetectionIsTorNode**
> \Swagger\Client\Model\ThreatDetectionTorNodeResponse networkThreatDetectionIsTorNode($value)

Check if IP address is a Tor node server

Check if the input IP address is a Tor exit node server.  Tor servers are a type of privacy-preserving technology that can hide the original IP address who makes a request.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\NetworkThreatDetectionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$value = "value_example"; // string | IP address to check, e.g. \"55.55.55.55\".  The input is a string so be sure to enclose it in double-quotes.

try {
    $result = $apiInstance->networkThreatDetectionIsTorNode($value);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NetworkThreatDetectionApi->networkThreatDetectionIsTorNode: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **value** | **string**| IP address to check, e.g. \&quot;55.55.55.55\&quot;.  The input is a string so be sure to enclose it in double-quotes. |

### Return type

[**\Swagger\Client\Model\ThreatDetectionTorNodeResponse**](../Model/ThreatDetectionTorNodeResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json
 - **Accept**: application/json, text/json, application/xml, text/xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

