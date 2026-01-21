# Dimer47\LogsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersLogsDestroy()**](LogsApi.md#organizationsServersLogsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/logs/{key} | Delete server log content |
| [**organizationsServersLogsShow()**](LogsApi.md#organizationsServersLogsShow) | **GET** /orgs/{organization}/servers/{server}/logs/{key} | Get server log content |


## `organizationsServersLogsDestroy()`

```php
organizationsServersLogsDestroy($organization, $server, $key)
```

Delete server log content

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\LogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$key = 'key_example'; // string

try {
    $apiInstance->organizationsServersLogsDestroy($organization, $server, $key);
} catch (Exception $e) {
    echo 'Exception when calling LogsApi->organizationsServersLogsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **key** | **string**|  | |

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

## `organizationsServersLogsShow()`

```php
organizationsServersLogsShow($organization, $server, $key): \Dimer47\Model\OrganizationsServersLogsShow200Response
```

Get server log content

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\LogsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$key = 'key_example'; // string

try {
    $result = $apiInstance->organizationsServersLogsShow($organization, $server, $key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LogsApi->organizationsServersLogsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **key** | **string**|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersLogsShow200Response**](../Model/OrganizationsServersLogsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
