# cloudmersive_security_api_client
The security APIs help you detect and block security threats.

[Cloudmersive Security API](https://www.cloudmersive.com/security-threat-detection-api) helps you detect and block security threats.

- API version: v1
- Package version: 1.2.0


## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/cloudmersive/cloudmersive_security_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_security_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_security_api_client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ContentThreatDetectionApi* | [**contentThreatDetectionAutomaticThreatDetectionString**](docs/Api/ContentThreatDetectionApi.md#contentthreatdetectionautomaticthreatdetectionstring) | **POST** /security/threat-detection/content/automatic/detect/string | Automatically detect threats in an input string
*ContentThreatDetectionApi* | [**contentThreatDetectionCheckSqlInjectionString**](docs/Api/ContentThreatDetectionApi.md#contentthreatdetectionchecksqlinjectionstring) | **POST** /security/threat-detection/content/sql-injection/detect/string | Check text input for SQL Injection (SQLI) attacks
*ContentThreatDetectionApi* | [**contentThreatDetectionCheckXxe**](docs/Api/ContentThreatDetectionApi.md#contentthreatdetectioncheckxxe) | **POST** /security/threat-detection/content/xxe/detect/xml/string | Protect text input from XML External Entity (XXE) attacks
*ContentThreatDetectionApi* | [**contentThreatDetectionDetectInsecureDeserializationJsonString**](docs/Api/ContentThreatDetectionApi.md#contentthreatdetectiondetectinsecuredeserializationjsonstring) | **POST** /security/threat-detection/content/insecure-deserialization/json/detect/string | Detect Insecure Deserialization JSON (JID) attacks in a string
*ContentThreatDetectionApi* | [**contentThreatDetectionProtectXss**](docs/Api/ContentThreatDetectionApi.md#contentthreatdetectionprotectxss) | **POST** /security/threat-detection/content/xss/detect/string | Protect text input from Cross-Site-Scripting (XSS) attacks through normalization
*NetworkThreatDetectionApi* | [**networkThreatDetectionDetectSsrfUrl**](docs/Api/NetworkThreatDetectionApi.md#networkthreatdetectiondetectssrfurl) | **POST** /security/threat-detection/network/url/ssrf/detect | Check a URL for Server-side Request Forgery (SSRF) threats
*NetworkThreatDetectionApi* | [**networkThreatDetectionIsBot**](docs/Api/NetworkThreatDetectionApi.md#networkthreatdetectionisbot) | **POST** /security/threat-detection/network/ip/is-bot | Check if IP address is a Bot client threat
*NetworkThreatDetectionApi* | [**networkThreatDetectionIsThreat**](docs/Api/NetworkThreatDetectionApi.md#networkthreatdetectionisthreat) | **POST** /security/threat-detection/network/ip/is-threat | Check if IP address is a known threat
*NetworkThreatDetectionApi* | [**networkThreatDetectionIsTorNode**](docs/Api/NetworkThreatDetectionApi.md#networkthreatdetectionistornode) | **POST** /security/threat-detection/network/ip/is-tor-node | Check if IP address is a Tor node server


## Documentation For Models

 - [IPThreatDetectionResponse](docs/Model/IPThreatDetectionResponse.md)
 - [StringAutomaticThreatDetection](docs/Model/StringAutomaticThreatDetection.md)
 - [StringInsecureDeserializationJsonDetection](docs/Model/StringInsecureDeserializationJsonDetection.md)
 - [StringSqlInjectionDetectionResult](docs/Model/StringSqlInjectionDetectionResult.md)
 - [StringXssProtectionResult](docs/Model/StringXssProtectionResult.md)
 - [StringXxeDetectionResult](docs/Model/StringXxeDetectionResult.md)
 - [ThreatDetectionBotCheckResponse](docs/Model/ThreatDetectionBotCheckResponse.md)
 - [ThreatDetectionTorNodeResponse](docs/Model/ThreatDetectionTorNodeResponse.md)
 - [UrlSsrfThreatDetectionRequestFull](docs/Model/UrlSsrfThreatDetectionRequestFull.md)
 - [UrlSsrfThreatDetectionResponseFull](docs/Model/UrlSsrfThreatDetectionResponseFull.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




