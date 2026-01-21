# Dimer47\OrganizationsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsIndex()**](OrganizationsApi.md#organizationsIndex) | **GET** /orgs | List organizations |
| [**organizationsServerCredentialsIndex()**](OrganizationsApi.md#organizationsServerCredentialsIndex) | **GET** /orgs/{organization}/server-credentials | List server credentials |
| [**organizationsServerCredentialsShow()**](OrganizationsApi.md#organizationsServerCredentialsShow) | **GET** /orgs/{organization}/server-credentials/{credential} | Get server credential |
| [**organizationsServerCredentialsVpcsIndex()**](OrganizationsApi.md#organizationsServerCredentialsVpcsIndex) | **GET** /orgs/{organization}/server-credentials/{credential}/regions/{region}/vpcs | List VPCs |
| [**organizationsServerCredentialsVpcsShow()**](OrganizationsApi.md#organizationsServerCredentialsVpcsShow) | **GET** /orgs/{organization}/server-credentials/{credential}/regions/{region}/vpcs/{vpcId} | Get VPC |
| [**organizationsServerCredentialsVpcsStore()**](OrganizationsApi.md#organizationsServerCredentialsVpcsStore) | **POST** /orgs/{organization}/server-credentials/{credential}/regions/{region}/vpcs | Create a new VPC |
| [**organizationsShow()**](OrganizationsApi.md#organizationsShow) | **GET** /orgs/{organization} | Get organization |


## `organizationsIndex()`

```php
organizationsIndex($page_size, $page_cursor): \Dimer47\Model\OrganizationsIndex200Response
```

List organizations

Show all organizations the user has access to.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsIndex($page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsIndex200Response**](../Model/OrganizationsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServerCredentialsIndex()`

```php
organizationsServerCredentialsIndex($organization, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServerCredentialsIndex200Response
```

List server credentials

Show all server credentials for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsServerCredentialsIndex($organization, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsServerCredentialsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServerCredentialsIndex200Response**](../Model/OrganizationsServerCredentialsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServerCredentialsShow()`

```php
organizationsServerCredentialsShow($organization, $credential): \Dimer47\Model\OrganizationsServerCredentialsShow200Response
```

Get server credential

Show a specific server credential for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$credential = 56; // int | The credential ID

try {
    $result = $apiInstance->organizationsServerCredentialsShow($organization, $credential);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsServerCredentialsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **credential** | **int**| The credential ID | |

### Return type

[**\Dimer47\Model\OrganizationsServerCredentialsShow200Response**](../Model/OrganizationsServerCredentialsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServerCredentialsVpcsIndex()`

```php
organizationsServerCredentialsVpcsIndex($organization, $credential, $region): \Dimer47\Model\OrganizationsServerCredentialsVpcsIndex200Response
```

List VPCs

List VPCs for the provider.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$credential = 56; // int | The credential ID
$region = 'region_example'; // string

try {
    $result = $apiInstance->organizationsServerCredentialsVpcsIndex($organization, $credential, $region);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsServerCredentialsVpcsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **credential** | **int**| The credential ID | |
| **region** | **string**|  | |

### Return type

[**\Dimer47\Model\OrganizationsServerCredentialsVpcsIndex200Response**](../Model/OrganizationsServerCredentialsVpcsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServerCredentialsVpcsShow()`

```php
organizationsServerCredentialsVpcsShow($organization, $credential, $region, $vpc_id): \Dimer47\Model\OrganizationsServerCredentialsVpcsStore201Response
```

Get VPC

Get a VPC for the provider.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$credential = 56; // int | The credential ID
$region = 'region_example'; // string
$vpc_id = 'vpc_id_example'; // string

try {
    $result = $apiInstance->organizationsServerCredentialsVpcsShow($organization, $credential, $region, $vpc_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsServerCredentialsVpcsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **credential** | **int**| The credential ID | |
| **region** | **string**|  | |
| **vpc_id** | **string**|  | |

### Return type

[**\Dimer47\Model\OrganizationsServerCredentialsVpcsStore201Response**](../Model/OrganizationsServerCredentialsVpcsStore201Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServerCredentialsVpcsStore()`

```php
organizationsServerCredentialsVpcsStore($organization, $credential, $region, $create_server_provider_network_request): object
```

Create a new VPC

Create a private network for the provider.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$credential = 56; // int | The credential ID
$region = 'region_example'; // string
$create_server_provider_network_request = new \Dimer47\Model\CreateServerProviderNetworkRequest(); // \Dimer47\Model\CreateServerProviderNetworkRequest

try {
    $result = $apiInstance->organizationsServerCredentialsVpcsStore($organization, $credential, $region, $create_server_provider_network_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsServerCredentialsVpcsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **credential** | **int**| The credential ID | |
| **region** | **string**|  | |
| **create_server_provider_network_request** | [**\Dimer47\Model\CreateServerProviderNetworkRequest**](../Model/CreateServerProviderNetworkRequest.md)|  | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/vnd.api+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsShow()`

```php
organizationsShow($organization): \Dimer47\Model\OrganizationsShow200Response
```

Get organization

Show a specific organization for the user.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\OrganizationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug

try {
    $result = $apiInstance->organizationsShow($organization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrganizationsApi->organizationsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |

### Return type

[**\Dimer47\Model\OrganizationsShow200Response**](../Model/OrganizationsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
