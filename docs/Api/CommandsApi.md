# Dimer47\CommandsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersSitesCommandsDestroy()**](CommandsApi.md#organizationsServersSitesCommandsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/commands/{command} | Delete command |
| [**organizationsServersSitesCommandsIndex()**](CommandsApi.md#organizationsServersSitesCommandsIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/commands | List commands |
| [**organizationsServersSitesCommandsOutputShow()**](CommandsApi.md#organizationsServersSitesCommandsOutputShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/commands/{command}/output | Get command output |
| [**organizationsServersSitesCommandsShow()**](CommandsApi.md#organizationsServersSitesCommandsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/commands/{command} | Get command |
| [**organizationsServersSitesCommandsStore()**](CommandsApi.md#organizationsServersSitesCommandsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/commands | Create command |


## `organizationsServersSitesCommandsDestroy()`

```php
organizationsServersSitesCommandsDestroy($organization, $server, $site, $command)
```

Delete command

Delete a command history.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\CommandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$command = 56; // int | The command ID

try {
    $apiInstance->organizationsServersSitesCommandsDestroy($organization, $server, $site, $command);
} catch (Exception $e) {
    echo 'Exception when calling CommandsApi->organizationsServersSitesCommandsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **command** | **int**| The command ID | |

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

## `organizationsServersSitesCommandsIndex()`

```php
organizationsServersSitesCommandsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_user_id, $filter_status, $filter_command): \Dimer47\Model\OrganizationsServersSitesCommandsIndex200Response
```

List commands

List all command runs for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\CommandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `status`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-status`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_user_id = 'filter_user_id_example'; // string | The user ID of the command initiator.
$filter_status = 'filter_status_example'; // string | The status of the command.
$filter_command = 'filter_command_example'; // string | The command it ran.

try {
    $result = $apiInstance->organizationsServersSitesCommandsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_user_id, $filter_status, $filter_command);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommandsApi->organizationsServersSitesCommandsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;status&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-status&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_user_id** | **string**| The user ID of the command initiator. | [optional] |
| **filter_status** | **string**| The status of the command. | [optional] |
| **filter_command** | **string**| The command it ran. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesCommandsIndex200Response**](../Model/OrganizationsServersSitesCommandsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesCommandsOutputShow()`

```php
organizationsServersSitesCommandsOutputShow($organization, $server, $site, $command): \Dimer47\Model\OrganizationsServersSitesCommandsOutputShow200Response
```

Get command output

Get the output of a specific command run.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\CommandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$command = 56; // int | The command ID

try {
    $result = $apiInstance->organizationsServersSitesCommandsOutputShow($organization, $server, $site, $command);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommandsApi->organizationsServersSitesCommandsOutputShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **command** | **int**| The command ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesCommandsOutputShow200Response**](../Model/OrganizationsServersSitesCommandsOutputShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesCommandsShow()`

```php
organizationsServersSitesCommandsShow($organization, $server, $site, $command): \Dimer47\Model\OrganizationsServersSitesCommandsShow200Response
```

Get command

Get a specific command run.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\CommandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$command = 56; // int | The command ID

try {
    $result = $apiInstance->organizationsServersSitesCommandsShow($organization, $server, $site, $command);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CommandsApi->organizationsServersSitesCommandsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **command** | **int**| The command ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesCommandsShow200Response**](../Model/OrganizationsServersSitesCommandsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesCommandsStore()`

```php
organizationsServersSitesCommandsStore($organization, $server, $site, $run_site_command_request)
```

Create command

Run a command on the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\CommandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$run_site_command_request = new \Dimer47\Model\RunSiteCommandRequest(); // \Dimer47\Model\RunSiteCommandRequest

try {
    $apiInstance->organizationsServersSitesCommandsStore($organization, $server, $site, $run_site_command_request);
} catch (Exception $e) {
    echo 'Exception when calling CommandsApi->organizationsServersSitesCommandsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **run_site_command_request** | [**\Dimer47\Model\RunSiteCommandRequest**](../Model/RunSiteCommandRequest.md)|  | |

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
