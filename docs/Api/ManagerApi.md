# KeyStack\Manager\ManagerApi

All URIs are relative to http://localhost.

Method | HTTP request | Description
------------- | ------------- | -------------
[**addManifestRecord()**](ManagerApi.md#addManifestRecord) | **POST** /v1/manifest | 
[**createLicense()**](ManagerApi.md#createLicense) | **POST** /v1/licenses | 
[**deleteActivation()**](ManagerApi.md#deleteActivation) | **DELETE** /v1/licenses/{internalLicenseId}/activations/{activationId} | 
[**deleteLicense()**](ManagerApi.md#deleteLicense) | **DELETE** /v1/licenses/{internalLicenseId} | 
[**deleteManifestRecord()**](ManagerApi.md#deleteManifestRecord) | **DELETE** /v1/manifest/{cacheKey} | 
[**getActivations()**](ManagerApi.md#getActivations) | **GET** /v1/licenses/{internalLicenseId}/activations | 
[**getAllLicenses()**](ManagerApi.md#getAllLicenses) | **GET** /v1/licenses | 
[**getLicense()**](ManagerApi.md#getLicense) | **GET** /v1/licenses/{internalLicenseId} | 
[**updateLicense()**](ManagerApi.md#updateLicense) | **PATCH** /v1/licenses/{internalLicenseId} | 


## `addManifestRecord()`

```php
addManifestRecord($manifestAddSchema): \KeyStack\Manager\Model\AddManifestRecord200Response
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$manifestAddSchema = new \KeyStack\Manager\Model\ManifestAddSchema(); // \KeyStack\Manager\Model\ManifestAddSchema

try {
    $result = $apiInstance->addManifestRecord($manifestAddSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->addManifestRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **manifestAddSchema** | [**\KeyStack\Manager\Model\ManifestAddSchema**](../Model/ManifestAddSchema.md)|  | [optional]

### Return type

[**\KeyStack\Manager\Model\AddManifestRecord200Response**](../Model/AddManifestRecord200Response.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createLicense()`

```php
createLicense($licenseCreateInput): \KeyStack\Manager\Model\LicenseRecord
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$licenseCreateInput = new \KeyStack\Manager\Model\LicenseCreateInput(); // \KeyStack\Manager\Model\LicenseCreateInput

try {
    $result = $apiInstance->createLicense($licenseCreateInput);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->createLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **licenseCreateInput** | [**\KeyStack\Manager\Model\LicenseCreateInput**](../Model/LicenseCreateInput.md)|  | [optional]

### Return type

[**\KeyStack\Manager\Model\LicenseRecord**](../Model/LicenseRecord.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteActivation()`

```php
deleteActivation($internalLicenseId, $activationId): \KeyStack\Manager\Model\ActivationDelete
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$internalLicenseId = 'internalLicenseId_example'; // string
$activationId = 'activationId_example'; // string

try {
    $result = $apiInstance->deleteActivation($internalLicenseId, $activationId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->deleteActivation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internalLicenseId** | **string**|  |
 **activationId** | **string**|  |

### Return type

[**\KeyStack\Manager\Model\ActivationDelete**](../Model/ActivationDelete.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteLicense()`

```php
deleteLicense($internalLicenseId): \KeyStack\Manager\Model\LicenseDelete
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$internalLicenseId = 'internalLicenseId_example'; // string

try {
    $result = $apiInstance->deleteLicense($internalLicenseId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->deleteLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internalLicenseId** | **string**|  |

### Return type

[**\KeyStack\Manager\Model\LicenseDelete**](../Model/LicenseDelete.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteManifestRecord()`

```php
deleteManifestRecord($cacheKey)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$cacheKey = 'cacheKey_example'; // string

try {
    $apiInstance->deleteManifestRecord($cacheKey);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->deleteManifestRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cacheKey** | **string**|  |

### Return type

void (empty response body)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getActivations()`

```php
getActivations($internalLicenseId): \KeyStack\Manager\Model\ActivationList
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$internalLicenseId = 'internalLicenseId_example'; // string

try {
    $result = $apiInstance->getActivations($internalLicenseId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->getActivations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internalLicenseId** | **string**|  |

### Return type

[**\KeyStack\Manager\Model\ActivationList**](../Model/ActivationList.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getAllLicenses()`

```php
getAllLicenses(): \KeyStack\Manager\Model\LicenseList
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getAllLicenses();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->getAllLicenses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\KeyStack\Manager\Model\LicenseList**](../Model/LicenseList.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getLicense()`

```php
getLicense($internalLicenseId): \KeyStack\Manager\Model\LicenseRecord
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$internalLicenseId = 'internalLicenseId_example'; // string

try {
    $result = $apiInstance->getLicense($internalLicenseId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->getLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internalLicenseId** | **string**|  |

### Return type

[**\KeyStack\Manager\Model\LicenseRecord**](../Model/LicenseRecord.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateLicense()`

```php
updateLicense($internalLicenseId, $licenseUpdateInput): \KeyStack\Manager\Model\LicenseRecord
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: Bearer
$config = KeyStack\Manager\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new KeyStack\Manager\Api\ManagerApi(
    // If you want use custom http client, pass your client which implements `Psr\Http\Client\ClientInterface`.
    // This is optional, `Psr18ClientDiscovery` will be used to find http client. For instance `GuzzleHttp\Client` implements that interface
    new GuzzleHttp\Client(),
    $config
);
$internalLicenseId = 'internalLicenseId_example'; // string
$licenseUpdateInput = new \KeyStack\Manager\Model\LicenseUpdateInput(); // \KeyStack\Manager\Model\LicenseUpdateInput

try {
    $result = $apiInstance->updateLicense($internalLicenseId, $licenseUpdateInput);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ManagerApi->updateLicense: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **internalLicenseId** | **string**|  |
 **licenseUpdateInput** | [**\KeyStack\Manager\Model\LicenseUpdateInput**](../Model/LicenseUpdateInput.md)|  | [optional]

### Return type

[**\KeyStack\Manager\Model\LicenseRecord**](../Model/LicenseRecord.md)

### Authorization

[Bearer](../../README.md#Bearer)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
