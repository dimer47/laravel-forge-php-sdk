# Dimer47\BackgroundProcessesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersBackgroundProcessesDestroy()**](BackgroundProcessesApi.md#organizationsServersBackgroundProcessesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess} | Delete background process |
| [**organizationsServersBackgroundProcessesIndex()**](BackgroundProcessesApi.md#organizationsServersBackgroundProcessesIndex) | **GET** /orgs/{organization}/servers/{server}/background-processes | List background processes |
| [**organizationsServersBackgroundProcessesLogShow()**](BackgroundProcessesApi.md#organizationsServersBackgroundProcessesLogShow) | **GET** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess}/log | Get background process log |
| [**organizationsServersBackgroundProcessesShow()**](BackgroundProcessesApi.md#organizationsServersBackgroundProcessesShow) | **GET** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess} | Get background process |
| [**organizationsServersBackgroundProcessesStore()**](BackgroundProcessesApi.md#organizationsServersBackgroundProcessesStore) | **POST** /orgs/{organization}/servers/{server}/background-processes | Create background process |
| [**organizationsServersBackgroundProcessesUpdate()**](BackgroundProcessesApi.md#organizationsServersBackgroundProcessesUpdate) | **PUT** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess} | Update background process |


## `organizationsServersBackgroundProcessesDestroy()`

```php
organizationsServersBackgroundProcessesDestroy($organization, $server, $background_process)
```

Delete background process

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackgroundProcessesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$background_process = 56; // int | The background process ID

try {
    $apiInstance->organizationsServersBackgroundProcessesDestroy($organization, $server, $background_process);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundProcessesApi->organizationsServersBackgroundProcessesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **background_process** | **int**| The background process ID | |

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

## `organizationsServersBackgroundProcessesIndex()`

```php
organizationsServersBackgroundProcessesIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_user, $filter_site_id, $filter_directory): \Dimer47\Model\OrganizationsServersBackgroundProcessesIndex200Response
```

List background processes

List all background processes on the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackgroundProcessesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `user`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-user`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_user = 'filter_user_example'; // string | The user that the process is running as.
$filter_site_id = 'filter_site_id_example'; // string | The site ID that the process is running for.
$filter_directory = 'filter_directory_example'; // string | The directory that the process is running in.

try {
    $result = $apiInstance->organizationsServersBackgroundProcessesIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_user, $filter_site_id, $filter_directory);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundProcessesApi->organizationsServersBackgroundProcessesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;user&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-user&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_user** | **string**| The user that the process is running as. | [optional] |
| **filter_site_id** | **string**| The site ID that the process is running for. | [optional] |
| **filter_directory** | **string**| The directory that the process is running in. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersBackgroundProcessesIndex200Response**](../Model/OrganizationsServersBackgroundProcessesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersBackgroundProcessesLogShow()`

```php
organizationsServersBackgroundProcessesLogShow($organization, $server, $background_process): \Dimer47\Model\OrganizationsServersBackgroundProcessesLogShow200Response
```

Get background process log

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackgroundProcessesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$background_process = 56; // int | The background process ID

try {
    $result = $apiInstance->organizationsServersBackgroundProcessesLogShow($organization, $server, $background_process);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundProcessesApi->organizationsServersBackgroundProcessesLogShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **background_process** | **int**| The background process ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersBackgroundProcessesLogShow200Response**](../Model/OrganizationsServersBackgroundProcessesLogShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersBackgroundProcessesShow()`

```php
organizationsServersBackgroundProcessesShow($organization, $server, $background_process): \Dimer47\Model\OrganizationsServersBackgroundProcessesStore202Response
```

Get background process

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackgroundProcessesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$background_process = 56; // int | The background process ID

try {
    $result = $apiInstance->organizationsServersBackgroundProcessesShow($organization, $server, $background_process);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundProcessesApi->organizationsServersBackgroundProcessesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **background_process** | **int**| The background process ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersBackgroundProcessesStore202Response**](../Model/OrganizationsServersBackgroundProcessesStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersBackgroundProcessesStore()`

```php
organizationsServersBackgroundProcessesStore($organization, $server, $create_background_process_request): \Dimer47\Model\OrganizationsServersBackgroundProcessesStore202Response
```

Create background process

Create a new background process from a template.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackgroundProcessesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_background_process_request = new \Dimer47\Model\CreateBackgroundProcessRequest(); // \Dimer47\Model\CreateBackgroundProcessRequest

try {
    $result = $apiInstance->organizationsServersBackgroundProcessesStore($organization, $server, $create_background_process_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundProcessesApi->organizationsServersBackgroundProcessesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_background_process_request** | [**\Dimer47\Model\CreateBackgroundProcessRequest**](../Model/CreateBackgroundProcessRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersBackgroundProcessesStore202Response**](../Model/OrganizationsServersBackgroundProcessesStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersBackgroundProcessesUpdate()`

```php
organizationsServersBackgroundProcessesUpdate($organization, $server, $background_process, $update_background_process_request)
```

Update background process

Update the supervisor configuration for a background process.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackgroundProcessesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$background_process = 56; // int | The background process ID
$update_background_process_request = new \Dimer47\Model\UpdateBackgroundProcessRequest(); // \Dimer47\Model\UpdateBackgroundProcessRequest

try {
    $apiInstance->organizationsServersBackgroundProcessesUpdate($organization, $server, $background_process, $update_background_process_request);
} catch (Exception $e) {
    echo 'Exception when calling BackgroundProcessesApi->organizationsServersBackgroundProcessesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **background_process** | **int**| The background process ID | |
| **update_background_process_request** | [**\Dimer47\Model\UpdateBackgroundProcessRequest**](../Model/UpdateBackgroundProcessRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
