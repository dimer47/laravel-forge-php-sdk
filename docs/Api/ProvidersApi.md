# Dimer47\ProvidersApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**providersIndex()**](ProvidersApi.md#providersIndex) | **GET** /providers | List providers |
| [**providersRegionsIndex()**](ProvidersApi.md#providersRegionsIndex) | **GET** /providers/{provider}/regions | List provider regions |
| [**providersRegionsShow()**](ProvidersApi.md#providersRegionsShow) | **GET** /providers/{provider}/regions/{providerRegion} | Get provider region |
| [**providersRegionsSizesIndex()**](ProvidersApi.md#providersRegionsSizesIndex) | **GET** /providers/{provider}/regions/{providerRegion}/sizes | List provider region sizes |
| [**providersRegionsSizesShow()**](ProvidersApi.md#providersRegionsSizesShow) | **GET** /providers/{provider}/regions/{providerRegion}/sizes/{providerSize} | Get provider region size |
| [**providersShow()**](ProvidersApi.md#providersShow) | **GET** /providers/{provider} | Get provider |
| [**providersSizesIndex()**](ProvidersApi.md#providersSizesIndex) | **GET** /providers/{provider}/sizes | List provider sizes |
| [**providersSizesShow()**](ProvidersApi.md#providersSizesShow) | **GET** /providers/{provider}/sizes/{providerSize} | Get provider size |


## `providersIndex()`

```php
providersIndex($page_size, $page_cursor): \Dimer47\Model\ProvidersIndex200Response
```

List providers

Show all providers  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->providersIndex($page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\ProvidersIndex200Response**](../Model/ProvidersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersRegionsIndex()`

```php
providersRegionsIndex($provider, $page_size, $page_cursor): \Dimer47\Model\ProvidersRegionsIndex200Response
```

List provider regions

Show all provider regions  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->providersRegionsIndex($provider, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersRegionsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\ProvidersRegionsIndex200Response**](../Model/ProvidersRegionsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersRegionsShow()`

```php
providersRegionsShow($provider, $provider_region): \Dimer47\Model\ProvidersRegionsShow200Response
```

Get provider region

Show the provider region.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID
$provider_region = 56; // int | The provider region ID

try {
    $result = $apiInstance->providersRegionsShow($provider, $provider_region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersRegionsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |
| **provider_region** | **int**| The provider region ID | |

### Return type

[**\Dimer47\Model\ProvidersRegionsShow200Response**](../Model/ProvidersRegionsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersRegionsSizesIndex()`

```php
providersRegionsSizesIndex($provider, $provider_region, $page_size, $page_cursor): \Dimer47\Model\ProvidersRegionsSizesIndex200Response
```

List provider region sizes

Show all provider region sizes  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID
$provider_region = 56; // int | The provider region ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->providersRegionsSizesIndex($provider, $provider_region, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersRegionsSizesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |
| **provider_region** | **int**| The provider region ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\ProvidersRegionsSizesIndex200Response**](../Model/ProvidersRegionsSizesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersRegionsSizesShow()`

```php
providersRegionsSizesShow($provider, $provider_region, $provider_size): \Dimer47\Model\ProvidersRegionsSizesShow200Response
```

Get provider region size

Show the provider region size.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID
$provider_region = 56; // int | The provider region ID
$provider_size = 56; // int | The provider size ID

try {
    $result = $apiInstance->providersRegionsSizesShow($provider, $provider_region, $provider_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersRegionsSizesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |
| **provider_region** | **int**| The provider region ID | |
| **provider_size** | **int**| The provider size ID | |

### Return type

[**\Dimer47\Model\ProvidersRegionsSizesShow200Response**](../Model/ProvidersRegionsSizesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersShow()`

```php
providersShow($provider): \Dimer47\Model\ProvidersShow200Response
```

Get provider

Show the provider.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID

try {
    $result = $apiInstance->providersShow($provider);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |

### Return type

[**\Dimer47\Model\ProvidersShow200Response**](../Model/ProvidersShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersSizesIndex()`

```php
providersSizesIndex($provider, $page_size, $page_cursor): \Dimer47\Model\ProvidersSizesIndex200Response
```

List provider sizes

Show all providers  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->providersSizesIndex($provider, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersSizesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\ProvidersSizesIndex200Response**](../Model/ProvidersSizesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `providersSizesShow()`

```php
providersSizesShow($provider, $provider_size): \Dimer47\Model\ProvidersSizesShow200Response
```

Get provider size

Show the provider size.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$provider = 56; // int | The provider ID
$provider_size = 56; // int | The provider size ID

try {
    $result = $apiInstance->providersSizesShow($provider, $provider_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProvidersApi->providersSizesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **provider** | **int**| The provider ID | |
| **provider_size** | **int**| The provider size ID | |

### Return type

[**\Dimer47\Model\ProvidersSizesShow200Response**](../Model/ProvidersSizesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
