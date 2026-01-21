# Dimer47\StorageProvidersApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsStorageProvidersDestroy()**](StorageProvidersApi.md#organizationsStorageProvidersDestroy) | **DELETE** /orgs/{organization}/storage-providers/{storageConfiguration} | Delete storage provider |
| [**organizationsStorageProvidersIndex()**](StorageProvidersApi.md#organizationsStorageProvidersIndex) | **GET** /orgs/{organization}/storage-providers | List storage providers |
| [**organizationsStorageProvidersShow()**](StorageProvidersApi.md#organizationsStorageProvidersShow) | **GET** /orgs/{organization}/storage-providers/{storageConfiguration} | Get storage provider |
| [**organizationsStorageProvidersStore()**](StorageProvidersApi.md#organizationsStorageProvidersStore) | **POST** /orgs/{organization}/storage-providers | Create storage provider |
| [**organizationsStorageProvidersUpdate()**](StorageProvidersApi.md#organizationsStorageProvidersUpdate) | **PUT** /orgs/{organization}/storage-providers/{storageConfiguration} | Update storage provider |


## `organizationsStorageProvidersDestroy()`

```php
organizationsStorageProvidersDestroy($organization, $storage_configuration)
```

Delete storage provider

Delete a storage provider from the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\StorageProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$storage_configuration = 56; // int | The storage configuration ID

try {
    $apiInstance->organizationsStorageProvidersDestroy($organization, $storage_configuration);
} catch (Exception $e) {
    echo 'Exception when calling StorageProvidersApi->organizationsStorageProvidersDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **storage_configuration** | **int**| The storage configuration ID | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsStorageProvidersIndex()`

```php
organizationsStorageProvidersIndex($organization, $sort, $page_size, $page_cursor, $filter_provider): \Dimer47\Model\OrganizationsStorageProvidersIndex200Response
```

List storage providers

Show all storage providers for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\StorageProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$sort = 'sort_example'; // string | Available sorts are `name`, `provider`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-name`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_provider = 'filter_provider_example'; // string | The storage provider type.

try {
    $result = $apiInstance->organizationsStorageProvidersIndex($organization, $sort, $page_size, $page_cursor, $filter_provider);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageProvidersApi->organizationsStorageProvidersIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **sort** | **string**| Available sorts are &#x60;name&#x60;, &#x60;provider&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-name&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_provider** | **string**| The storage provider type. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsStorageProvidersIndex200Response**](../Model/OrganizationsStorageProvidersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsStorageProvidersShow()`

```php
organizationsStorageProvidersShow($organization, $storage_configuration): \Dimer47\Model\OrganizationsStorageProvidersStore201Response
```

Get storage provider

Show a specific storage provider for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\StorageProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$storage_configuration = 56; // int | The storage configuration ID

try {
    $result = $apiInstance->organizationsStorageProvidersShow($organization, $storage_configuration);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageProvidersApi->organizationsStorageProvidersShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **storage_configuration** | **int**| The storage configuration ID | |

### Return type

[**\Dimer47\Model\OrganizationsStorageProvidersStore201Response**](../Model/OrganizationsStorageProvidersStore201Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsStorageProvidersStore()`

```php
organizationsStorageProvidersStore($organization, $create_storage_configuration_request): \Dimer47\Model\OrganizationsStorageProvidersStore201Response
```

Create storage provider

Create a new storage provider for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\StorageProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$create_storage_configuration_request = new \Dimer47\Model\CreateStorageConfigurationRequest(); // \Dimer47\Model\CreateStorageConfigurationRequest

try {
    $result = $apiInstance->organizationsStorageProvidersStore($organization, $create_storage_configuration_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageProvidersApi->organizationsStorageProvidersStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **create_storage_configuration_request** | [**\Dimer47\Model\CreateStorageConfigurationRequest**](../Model/CreateStorageConfigurationRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsStorageProvidersStore201Response**](../Model/OrganizationsStorageProvidersStore201Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsStorageProvidersUpdate()`

```php
organizationsStorageProvidersUpdate($organization, $storage_configuration, $organizations_storage_providers_update_request): \Dimer47\Model\OrganizationsStorageProvidersStore201Response
```

Update storage provider

Update a storage provider for the organization.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\StorageProvidersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$storage_configuration = 56; // int | The storage configuration ID
$organizations_storage_providers_update_request = new \Dimer47\Model\OrganizationsStorageProvidersUpdateRequest(); // \Dimer47\Model\OrganizationsStorageProvidersUpdateRequest

try {
    $result = $apiInstance->organizationsStorageProvidersUpdate($organization, $storage_configuration, $organizations_storage_providers_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StorageProvidersApi->organizationsStorageProvidersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **storage_configuration** | **int**| The storage configuration ID | |
| **organizations_storage_providers_update_request** | [**\Dimer47\Model\OrganizationsStorageProvidersUpdateRequest**](../Model/OrganizationsStorageProvidersUpdateRequest.md)|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsStorageProvidersStore201Response**](../Model/OrganizationsStorageProvidersStore201Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
