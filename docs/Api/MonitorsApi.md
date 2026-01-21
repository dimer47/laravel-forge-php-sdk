# Dimer47\MonitorsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersMonitorsDestroy()**](MonitorsApi.md#organizationsServersMonitorsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/monitors/{monitor} | Delete server monitor |
| [**organizationsServersMonitorsIndex()**](MonitorsApi.md#organizationsServersMonitorsIndex) | **GET** /orgs/{organization}/servers/{server}/monitors | List server monitors |
| [**organizationsServersMonitorsShow()**](MonitorsApi.md#organizationsServersMonitorsShow) | **GET** /orgs/{organization}/servers/{server}/monitors/{monitor} | Get server monitor |
| [**organizationsServersMonitorsStore()**](MonitorsApi.md#organizationsServersMonitorsStore) | **POST** /orgs/{organization}/servers/{server}/monitors | Create server monitor |


## `organizationsServersMonitorsDestroy()`

```php
organizationsServersMonitorsDestroy($organization, $server, $monitor)
```

Delete server monitor

Remove a monitor from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\MonitorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$monitor = 56; // int | The monitor ID

try {
    $apiInstance->organizationsServersMonitorsDestroy($organization, $server, $monitor);
} catch (Exception $e) {
    echo 'Exception when calling MonitorsApi->organizationsServersMonitorsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **monitor** | **int**| The monitor ID | |

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

## `organizationsServersMonitorsIndex()`

```php
organizationsServersMonitorsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_status, $filter_state, $filter_type, $filter_notify): \Dimer47\Model\OrganizationsServersMonitorsIndex200Response
```

List server monitors

List all monitors associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\MonitorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `state`, `status`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-state`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_status = 'filter_status_example'; // string | The status of the monitor.
$filter_state = 'filter_state_example'; // string | The state of the monitor.
$filter_type = 'filter_type_example'; // string | The type of the monitor.
$filter_notify = 'filter_notify_example'; // string | The email address to notify when the monitor is in an alert state.

try {
    $result = $apiInstance->organizationsServersMonitorsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_status, $filter_state, $filter_type, $filter_notify);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MonitorsApi->organizationsServersMonitorsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;state&#x60;, &#x60;status&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-state&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_status** | **string**| The status of the monitor. | [optional] |
| **filter_state** | **string**| The state of the monitor. | [optional] |
| **filter_type** | **string**| The type of the monitor. | [optional] |
| **filter_notify** | **string**| The email address to notify when the monitor is in an alert state. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersMonitorsIndex200Response**](../Model/OrganizationsServersMonitorsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersMonitorsShow()`

```php
organizationsServersMonitorsShow($organization, $server, $monitor): \Dimer47\Model\OrganizationsServersMonitorsStore202Response
```

Get server monitor

Get a specific monitor associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\MonitorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$monitor = 56; // int | The monitor ID

try {
    $result = $apiInstance->organizationsServersMonitorsShow($organization, $server, $monitor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MonitorsApi->organizationsServersMonitorsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **monitor** | **int**| The monitor ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersMonitorsStore202Response**](../Model/OrganizationsServersMonitorsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersMonitorsStore()`

```php
organizationsServersMonitorsStore($organization, $server, $create_monitor_request): \Dimer47\Model\OrganizationsServersMonitorsStore202Response
```

Create server monitor

Add a new monitor to the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\MonitorsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_monitor_request = new \Dimer47\Model\CreateMonitorRequest(); // \Dimer47\Model\CreateMonitorRequest

try {
    $result = $apiInstance->organizationsServersMonitorsStore($organization, $server, $create_monitor_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MonitorsApi->organizationsServersMonitorsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_monitor_request** | [**\Dimer47\Model\CreateMonitorRequest**](../Model/CreateMonitorRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersMonitorsStore202Response**](../Model/OrganizationsServersMonitorsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
