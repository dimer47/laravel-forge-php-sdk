# Dimer47\ServersApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersActionsStore()**](ServersApi.md#organizationsServersActionsStore) | **POST** /orgs/{organization}/servers/{server}/actions | Create server action |
| [**organizationsServersArchivesDestroy()**](ServersApi.md#organizationsServersArchivesDestroy) | **DELETE** /orgs/{organization}/servers/archives/{server} | Delete archived server |
| [**organizationsServersArchivesIndex()**](ServersApi.md#organizationsServersArchivesIndex) | **GET** /orgs/{organization}/servers/archives | List archived servers |
| [**organizationsServersArchivesStore()**](ServersApi.md#organizationsServersArchivesStore) | **POST** /orgs/{organization}/servers/archives | Create an archived server |
| [**organizationsServersBackgroundProcessesActionsStore()**](ServersApi.md#organizationsServersBackgroundProcessesActionsStore) | **POST** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess}/actions | Perform an action on a server background process |
| [**organizationsServersDestroy()**](ServersApi.md#organizationsServersDestroy) | **DELETE** /orgs/{organization}/servers/{server} | Delete server |
| [**organizationsServersEventsIndex()**](ServersApi.md#organizationsServersEventsIndex) | **GET** /orgs/{organization}/servers/{server}/events | List server events |
| [**organizationsServersEventsOutputShow()**](ServersApi.md#organizationsServersEventsOutputShow) | **GET** /orgs/{organization}/servers/{server}/events/{event}/output | Get server event output |
| [**organizationsServersEventsShow()**](ServersApi.md#organizationsServersEventsShow) | **GET** /orgs/{organization}/servers/{server}/events/{event} | Get server event |
| [**organizationsServersIndex()**](ServersApi.md#organizationsServersIndex) | **GET** /orgs/{organization}/servers | List servers |
| [**organizationsServersPhpCliVersionShow()**](ServersApi.md#organizationsServersPhpCliVersionShow) | **GET** /orgs/{organization}/servers/{server}/php/cli-version | Get PHP CLI version |
| [**organizationsServersPhpCliVersionUpdate()**](ServersApi.md#organizationsServersPhpCliVersionUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/cli-version | Update PHP CLI version |
| [**organizationsServersPhpMaxExecutionTimeShow()**](ServersApi.md#organizationsServersPhpMaxExecutionTimeShow) | **GET** /orgs/{organization}/servers/{server}/php/max-execution-time | Get server PHP max execution time |
| [**organizationsServersPhpMaxExecutionTimeUpdate()**](ServersApi.md#organizationsServersPhpMaxExecutionTimeUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/max-execution-time | Update server PHP max execution time |
| [**organizationsServersPhpMaxUploadSizeShow()**](ServersApi.md#organizationsServersPhpMaxUploadSizeShow) | **GET** /orgs/{organization}/servers/{server}/php/max-upload-size | Get server PHP max upload size |
| [**organizationsServersPhpMaxUploadSizeUpdate()**](ServersApi.md#organizationsServersPhpMaxUploadSizeUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/max-upload-size | Update server PHP max upload size |
| [**organizationsServersPhpOpcacheDestroy()**](ServersApi.md#organizationsServersPhpOpcacheDestroy) | **DELETE** /orgs/{organization}/servers/{server}/php/opcache | Delete PHP OPcache config |
| [**organizationsServersPhpOpcacheShow()**](ServersApi.md#organizationsServersPhpOpcacheShow) | **GET** /orgs/{organization}/servers/{server}/php/opcache | Get server PHP OPcache status |
| [**organizationsServersPhpOpcacheStore()**](ServersApi.md#organizationsServersPhpOpcacheStore) | **POST** /orgs/{organization}/servers/{server}/php/opcache | Create PHP OPcache config |
| [**organizationsServersPhpSiteVersionShow()**](ServersApi.md#organizationsServersPhpSiteVersionShow) | **GET** /orgs/{organization}/servers/{server}/php/site-version | Get PHP site version |
| [**organizationsServersPhpSiteVersionUpdate()**](ServersApi.md#organizationsServersPhpSiteVersionUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/site-version | Update PHP site version |
| [**organizationsServersPhpVersionsConfigsCliShow()**](ServersApi.md#organizationsServersPhpVersionsConfigsCliShow) | **GET** /orgs/{organization}/servers/{server}/php/versions/{phpVersion}/configs/cli | Get PHP version CLI config |
| [**organizationsServersPhpVersionsConfigsCliUpdate()**](ServersApi.md#organizationsServersPhpVersionsConfigsCliUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/versions/{phpVersion}/configs/cli | Update PHP version CLI config |
| [**organizationsServersPhpVersionsConfigsFpmShow()**](ServersApi.md#organizationsServersPhpVersionsConfigsFpmShow) | **GET** /orgs/{organization}/servers/{server}/php/versions/{phpVersion}/configs/fpm | Get PHP version FPM config |
| [**organizationsServersPhpVersionsConfigsFpmUpdate()**](ServersApi.md#organizationsServersPhpVersionsConfigsFpmUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/versions/{phpVersion}/configs/fpm | Update PHP version FPM config |
| [**organizationsServersPhpVersionsConfigsPoolShow()**](ServersApi.md#organizationsServersPhpVersionsConfigsPoolShow) | **GET** /orgs/{organization}/servers/{server}/php/versions/{phpVersion}/configs/pool | Get PHP version pool config |
| [**organizationsServersPhpVersionsConfigsPoolUpdate()**](ServersApi.md#organizationsServersPhpVersionsConfigsPoolUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/versions/{phpVersion}/configs/pool | Update PHP version pool config |
| [**organizationsServersPhpVersionsDestroy()**](ServersApi.md#organizationsServersPhpVersionsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/php/versions/{phpVersion} | Delete installed PHP version |
| [**organizationsServersPhpVersionsIndex()**](ServersApi.md#organizationsServersPhpVersionsIndex) | **GET** /orgs/{organization}/servers/{server}/php/versions | List PHP versions for server |
| [**organizationsServersPhpVersionsShow()**](ServersApi.md#organizationsServersPhpVersionsShow) | **GET** /orgs/{organization}/servers/{server}/php/versions/{phpVersion} | Get PHP version |
| [**organizationsServersPhpVersionsStore()**](ServersApi.md#organizationsServersPhpVersionsStore) | **POST** /orgs/{organization}/servers/{server}/php/versions | Install new PHP version |
| [**organizationsServersPhpVersionsUpdate()**](ServersApi.md#organizationsServersPhpVersionsUpdate) | **PUT** /orgs/{organization}/servers/{server}/php/versions/{phpVersion} | Update installed PHP version |
| [**organizationsServersServicesMysqlActionsStore()**](ServersApi.md#organizationsServersServicesMysqlActionsStore) | **POST** /orgs/{organization}/servers/{server}/services/mysql/actions | Perform MySQL action |
| [**organizationsServersServicesNginxActionsStore()**](ServersApi.md#organizationsServersServicesNginxActionsStore) | **POST** /orgs/{organization}/servers/{server}/services/nginx/actions | Perform Nginx action |
| [**organizationsServersServicesPhpActionsStore()**](ServersApi.md#organizationsServersServicesPhpActionsStore) | **POST** /orgs/{organization}/servers/{server}/services/php/actions | Perform PHP action |
| [**organizationsServersServicesPostgresActionsStore()**](ServersApi.md#organizationsServersServicesPostgresActionsStore) | **POST** /orgs/{organization}/servers/{server}/services/postgres/actions | Perform Postgres action |
| [**organizationsServersServicesRedisActionsStore()**](ServersApi.md#organizationsServersServicesRedisActionsStore) | **POST** /orgs/{organization}/servers/{server}/services/redis/actions | Perform Redis action |
| [**organizationsServersServicesSupervisorActionsStore()**](ServersApi.md#organizationsServersServicesSupervisorActionsStore) | **POST** /orgs/{organization}/servers/{server}/services/supervisor/actions | Perform Supervisor action |
| [**organizationsServersShow()**](ServersApi.md#organizationsServersShow) | **GET** /orgs/{organization}/servers/{server} | Get server |
| [**organizationsServersStore()**](ServersApi.md#organizationsServersStore) | **POST** /orgs/{organization}/servers | Create server |
| [**organizationsTeamsServersDestroy()**](ServersApi.md#organizationsTeamsServersDestroy) | **DELETE** /orgs/{organization}/teams/{team}/servers/{server} | Delete a server share |
| [**organizationsTeamsServersIndex()**](ServersApi.md#organizationsTeamsServersIndex) | **GET** /orgs/{organization}/teams/{team}/servers | List team servers |
| [**organizationsTeamsServersStore()**](ServersApi.md#organizationsTeamsServersStore) | **POST** /orgs/{organization}/teams/{team}/servers | Create a new server share |


## `organizationsServersActionsStore()`

```php
organizationsServersActionsStore($organization, $server, $server_action_request)
```

Create server action

Run an action on a server, defined by the action type parameter.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$server_action_request = new \Dimer47\Model\ServerActionRequest(); // \Dimer47\Model\ServerActionRequest

try {
    $apiInstance->organizationsServersActionsStore($organization, $server, $server_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **server_action_request** | [**\Dimer47\Model\ServerActionRequest**](../Model/ServerActionRequest.md)|  | |

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

## `organizationsServersArchivesDestroy()`

```php
organizationsServersArchivesDestroy($organization, $server)
```

Delete archived server

Unarchive a server. Make sure you have regenerated the server key and added it to the server before unarchiving.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $apiInstance->organizationsServersArchivesDestroy($organization, $server);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersArchivesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

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

## `organizationsServersArchivesIndex()`

```php
organizationsServersArchivesIndex($organization, $sort, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServersIndex200Response
```

List archived servers

Get all archived servers for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsServersArchivesIndex($organization, $sort, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersArchivesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersIndex200Response**](../Model/OrganizationsServersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersArchivesStore()`

```php
organizationsServersArchivesStore($organization, $archive_request)
```

Create an archived server

Archive a server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$archive_request = new \Dimer47\Model\ArchiveRequest(); // \Dimer47\Model\ArchiveRequest

try {
    $apiInstance->organizationsServersArchivesStore($organization, $archive_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersArchivesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **archive_request** | [**\Dimer47\Model\ArchiveRequest**](../Model/ArchiveRequest.md)|  | |

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

## `organizationsServersBackgroundProcessesActionsStore()`

```php
organizationsServersBackgroundProcessesActionsStore($organization, $server, $background_process, $background_process_action_request)
```

Perform an action on a server background process

Run an action on a server-level background process.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$background_process = 56; // int | The background process ID
$background_process_action_request = new \Dimer47\Model\BackgroundProcessActionRequest(); // \Dimer47\Model\BackgroundProcessActionRequest

try {
    $apiInstance->organizationsServersBackgroundProcessesActionsStore($organization, $server, $background_process, $background_process_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersBackgroundProcessesActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **background_process** | **int**| The background process ID | |
| **background_process_action_request** | [**\Dimer47\Model\BackgroundProcessActionRequest**](../Model/BackgroundProcessActionRequest.md)|  | |

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

## `organizationsServersDestroy()`

```php
organizationsServersDestroy($organization, $server)
```

Delete server

Delete a server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $apiInstance->organizationsServersDestroy($organization, $server);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

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

## `organizationsServersEventsIndex()`

```php
organizationsServersEventsIndex($organization, $server, $sort, $include, $page_size, $page_cursor, $filter_initiated_by, $filter_ran_as): \Dimer47\Model\OrganizationsServersEventsIndex200Response
```

List server events

List all events associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$include = 'include_example'; // string | Available includes are `initiator`, `initiatorCount`, `initiatorExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_initiated_by = 'filter_initiated_by_example'; // string | The user ID of the event initiator.
$filter_ran_as = 'filter_ran_as_example'; // string | The server user that the event was run as.

try {
    $result = $apiInstance->organizationsServersEventsIndex($organization, $server, $sort, $include, $page_size, $page_cursor, $filter_initiated_by, $filter_ran_as);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersEventsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **include** | **string**| Available includes are &#x60;initiator&#x60;, &#x60;initiatorCount&#x60;, &#x60;initiatorExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_initiated_by** | **string**| The user ID of the event initiator. | [optional] |
| **filter_ran_as** | **string**| The server user that the event was run as. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersEventsIndex200Response**](../Model/OrganizationsServersEventsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersEventsOutputShow()`

```php
organizationsServersEventsOutputShow($organization, $server, $event): \Dimer47\Model\OrganizationsServersEventsOutputShow200Response
```

Get server event output

Get the output for a specific event associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$event = 56; // int | The event ID

try {
    $result = $apiInstance->organizationsServersEventsOutputShow($organization, $server, $event);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersEventsOutputShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **event** | **int**| The event ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersEventsOutputShow200Response**](../Model/OrganizationsServersEventsOutputShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersEventsShow()`

```php
organizationsServersEventsShow($organization, $server, $event): \Dimer47\Model\OrganizationsServersEventsShow200Response
```

Get server event

Get a specific event associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$event = 56; // int | The event ID

try {
    $result = $apiInstance->organizationsServersEventsShow($organization, $server, $event);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersEventsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **event** | **int**| The event ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersEventsShow200Response**](../Model/OrganizationsServersEventsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersIndex()`

```php
organizationsServersIndex($organization, $sort, $page_size, $page_cursor, $filter_ip_address, $filter_name, $filter_region, $filter_size, $filter_provider, $filter_ubuntu_version, $filter_php_version, $filter_database_type): \Dimer47\Model\OrganizationsServersIndex200Response
```

List servers

Show all servers for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$sort = 'sort_example'; // string | Available sorts are `name`, `provider`, `ubuntu_version`, `region`, `php_version`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-name`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_ip_address = 'filter_ip_address_example'; // string | The IP address of the server.
$filter_name = 'filter_name_example'; // string | The name of the server.
$filter_region = 'filter_region_example'; // string | The region where the server is located.
$filter_size = 'filter_size_example'; // string | The size of the server.
$filter_provider = 'filter_provider_example'; // string | The provider of the server.
$filter_ubuntu_version = 'filter_ubuntu_version_example'; // string | The Ubuntu version of the server.
$filter_php_version = 'filter_php_version_example'; // string | The PHP version of the server.
$filter_database_type = 'filter_database_type_example'; // string | The database type of the server.

try {
    $result = $apiInstance->organizationsServersIndex($organization, $sort, $page_size, $page_cursor, $filter_ip_address, $filter_name, $filter_region, $filter_size, $filter_provider, $filter_ubuntu_version, $filter_php_version, $filter_database_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **sort** | **string**| Available sorts are &#x60;name&#x60;, &#x60;provider&#x60;, &#x60;ubuntu_version&#x60;, &#x60;region&#x60;, &#x60;php_version&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-name&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_ip_address** | **string**| The IP address of the server. | [optional] |
| **filter_name** | **string**| The name of the server. | [optional] |
| **filter_region** | **string**| The region where the server is located. | [optional] |
| **filter_size** | **string**| The size of the server. | [optional] |
| **filter_provider** | **string**| The provider of the server. | [optional] |
| **filter_ubuntu_version** | **string**| The Ubuntu version of the server. | [optional] |
| **filter_php_version** | **string**| The PHP version of the server. | [optional] |
| **filter_database_type** | **string**| The database type of the server. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersIndex200Response**](../Model/OrganizationsServersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpCliVersionShow()`

```php
organizationsServersPhpCliVersionShow($organization, $server): \Dimer47\Model\OrganizationsServersPhpCliVersionShow200Response
```

Get PHP CLI version

Show the PHP CLI version which has been set for the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersPhpCliVersionShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpCliVersionShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpCliVersionShow200Response**](../Model/OrganizationsServersPhpCliVersionShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpCliVersionUpdate()`

```php
organizationsServersPhpCliVersionUpdate($organization, $server, $update_php_cli_version_request)
```

Update PHP CLI version

Update the PHP CLI version for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$update_php_cli_version_request = new \Dimer47\Model\UpdatePhpCliVersionRequest(); // \Dimer47\Model\UpdatePhpCliVersionRequest

try {
    $apiInstance->organizationsServersPhpCliVersionUpdate($organization, $server, $update_php_cli_version_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpCliVersionUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **update_php_cli_version_request** | [**\Dimer47\Model\UpdatePhpCliVersionRequest**](../Model/UpdatePhpCliVersionRequest.md)|  | |

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

## `organizationsServersPhpMaxExecutionTimeShow()`

```php
organizationsServersPhpMaxExecutionTimeShow($organization, $server): \Dimer47\Model\OrganizationsServersPhpMaxExecutionTimeShow200Response
```

Get server PHP max execution time

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersPhpMaxExecutionTimeShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpMaxExecutionTimeShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpMaxExecutionTimeShow200Response**](../Model/OrganizationsServersPhpMaxExecutionTimeShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpMaxExecutionTimeUpdate()`

```php
organizationsServersPhpMaxExecutionTimeUpdate($organization, $server, $update_php_settings_request)
```

Update server PHP max execution time

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$update_php_settings_request = new \Dimer47\Model\UpdatePhpSettingsRequest(); // \Dimer47\Model\UpdatePhpSettingsRequest

try {
    $apiInstance->organizationsServersPhpMaxExecutionTimeUpdate($organization, $server, $update_php_settings_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpMaxExecutionTimeUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **update_php_settings_request** | [**\Dimer47\Model\UpdatePhpSettingsRequest**](../Model/UpdatePhpSettingsRequest.md)|  | [optional] |

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

## `organizationsServersPhpMaxUploadSizeShow()`

```php
organizationsServersPhpMaxUploadSizeShow($organization, $server): \Dimer47\Model\OrganizationsServersPhpMaxUploadSizeShow200Response
```

Get server PHP max upload size

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersPhpMaxUploadSizeShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpMaxUploadSizeShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpMaxUploadSizeShow200Response**](../Model/OrganizationsServersPhpMaxUploadSizeShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpMaxUploadSizeUpdate()`

```php
organizationsServersPhpMaxUploadSizeUpdate($organization, $server, $update_php_settings_request)
```

Update server PHP max upload size

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$update_php_settings_request = new \Dimer47\Model\UpdatePhpSettingsRequest(); // \Dimer47\Model\UpdatePhpSettingsRequest

try {
    $apiInstance->organizationsServersPhpMaxUploadSizeUpdate($organization, $server, $update_php_settings_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpMaxUploadSizeUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **update_php_settings_request** | [**\Dimer47\Model\UpdatePhpSettingsRequest**](../Model/UpdatePhpSettingsRequest.md)|  | [optional] |

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

## `organizationsServersPhpOpcacheDestroy()`

```php
organizationsServersPhpOpcacheDestroy($organization, $server)
```

Delete PHP OPcache config

Disable PHP OPcache for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $apiInstance->organizationsServersPhpOpcacheDestroy($organization, $server);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpOpcacheDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

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

## `organizationsServersPhpOpcacheShow()`

```php
organizationsServersPhpOpcacheShow($organization, $server): \Dimer47\Model\OrganizationsServersPhpOpcacheShow200Response
```

Get server PHP OPcache status

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersPhpOpcacheShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpOpcacheShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpOpcacheShow200Response**](../Model/OrganizationsServersPhpOpcacheShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpOpcacheStore()`

```php
organizationsServersPhpOpcacheStore($organization, $server)
```

Create PHP OPcache config

Enable PHP OPcache for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $apiInstance->organizationsServersPhpOpcacheStore($organization, $server);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpOpcacheStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

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

## `organizationsServersPhpSiteVersionShow()`

```php
organizationsServersPhpSiteVersionShow($organization, $server): \Dimer47\Model\OrganizationsServersPhpCliVersionShow200Response
```

Get PHP site version

Show the PHP site version which has been set for the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersPhpSiteVersionShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpSiteVersionShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpCliVersionShow200Response**](../Model/OrganizationsServersPhpCliVersionShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpSiteVersionUpdate()`

```php
organizationsServersPhpSiteVersionUpdate($organization, $server, $update_php_cli_version_request)
```

Update PHP site version

Update the PHP site version for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$update_php_cli_version_request = new \Dimer47\Model\UpdatePhpCliVersionRequest(); // \Dimer47\Model\UpdatePhpCliVersionRequest

try {
    $apiInstance->organizationsServersPhpSiteVersionUpdate($organization, $server, $update_php_cli_version_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpSiteVersionUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **update_php_cli_version_request** | [**\Dimer47\Model\UpdatePhpCliVersionRequest**](../Model/UpdatePhpCliVersionRequest.md)|  | |

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

## `organizationsServersPhpVersionsConfigsCliShow()`

```php
organizationsServersPhpVersionsConfigsCliShow($organization, $server, $php_version): \Dimer47\Model\OrganizationsServersPhpVersionsConfigsCliShow200Response
```

Get PHP version CLI config

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID

try {
    $result = $apiInstance->organizationsServersPhpVersionsConfigsCliShow($organization, $server, $php_version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsConfigsCliShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpVersionsConfigsCliShow200Response**](../Model/OrganizationsServersPhpVersionsConfigsCliShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpVersionsConfigsCliUpdate()`

```php
organizationsServersPhpVersionsConfigsCliUpdate($organization, $server, $php_version, $update_php_cli_request)
```

Update PHP version CLI config

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID
$update_php_cli_request = new \Dimer47\Model\UpdatePhpCliRequest(); // \Dimer47\Model\UpdatePhpCliRequest

try {
    $apiInstance->organizationsServersPhpVersionsConfigsCliUpdate($organization, $server, $php_version, $update_php_cli_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsConfigsCliUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |
| **update_php_cli_request** | [**\Dimer47\Model\UpdatePhpCliRequest**](../Model/UpdatePhpCliRequest.md)|  | |

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

## `organizationsServersPhpVersionsConfigsFpmShow()`

```php
organizationsServersPhpVersionsConfigsFpmShow($organization, $server, $php_version): \Dimer47\Model\OrganizationsServersPhpVersionsConfigsFpmShow200Response
```

Get PHP version FPM config

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID

try {
    $result = $apiInstance->organizationsServersPhpVersionsConfigsFpmShow($organization, $server, $php_version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsConfigsFpmShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpVersionsConfigsFpmShow200Response**](../Model/OrganizationsServersPhpVersionsConfigsFpmShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpVersionsConfigsFpmUpdate()`

```php
organizationsServersPhpVersionsConfigsFpmUpdate($organization, $server, $php_version, $update_php_fpm_request)
```

Update PHP version FPM config

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID
$update_php_fpm_request = new \Dimer47\Model\UpdatePhpFpmRequest(); // \Dimer47\Model\UpdatePhpFpmRequest

try {
    $apiInstance->organizationsServersPhpVersionsConfigsFpmUpdate($organization, $server, $php_version, $update_php_fpm_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsConfigsFpmUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |
| **update_php_fpm_request** | [**\Dimer47\Model\UpdatePhpFpmRequest**](../Model/UpdatePhpFpmRequest.md)|  | |

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

## `organizationsServersPhpVersionsConfigsPoolShow()`

```php
organizationsServersPhpVersionsConfigsPoolShow($organization, $server, $php_version, $user): \Dimer47\Model\OrganizationsServersPhpVersionsConfigsPoolShow200Response
```

Get PHP version pool config

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID
$user = 'user_example'; // string

try {
    $result = $apiInstance->organizationsServersPhpVersionsConfigsPoolShow($organization, $server, $php_version, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsConfigsPoolShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |
| **user** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpVersionsConfigsPoolShow200Response**](../Model/OrganizationsServersPhpVersionsConfigsPoolShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpVersionsConfigsPoolUpdate()`

```php
organizationsServersPhpVersionsConfigsPoolUpdate($organization, $server, $php_version, $update_php_pool_request)
```

Update PHP version pool config

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID
$update_php_pool_request = new \Dimer47\Model\UpdatePhpPoolRequest(); // \Dimer47\Model\UpdatePhpPoolRequest

try {
    $apiInstance->organizationsServersPhpVersionsConfigsPoolUpdate($organization, $server, $php_version, $update_php_pool_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsConfigsPoolUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |
| **update_php_pool_request** | [**\Dimer47\Model\UpdatePhpPoolRequest**](../Model/UpdatePhpPoolRequest.md)|  | |

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

## `organizationsServersPhpVersionsDestroy()`

```php
organizationsServersPhpVersionsDestroy($organization, $server, $php_version)
```

Delete installed PHP version

Uninstall the PHP version from the server  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID

try {
    $apiInstance->organizationsServersPhpVersionsDestroy($organization, $server, $php_version);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |

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

## `organizationsServersPhpVersionsIndex()`

```php
organizationsServersPhpVersionsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_status, $filter_version): \Dimer47\Model\OrganizationsServersPhpVersionsIndex200Response
```

List PHP versions for server

List all PHP versions installed on the server  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`, `status`, `version`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_status = 'filter_status_example'; // string
$filter_version = 'filter_version_example'; // string

try {
    $result = $apiInstance->organizationsServersPhpVersionsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_status, $filter_version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;, &#x60;status&#x60;, &#x60;version&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_status** | **string**|  | [optional] |
| **filter_version** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpVersionsIndex200Response**](../Model/OrganizationsServersPhpVersionsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpVersionsShow()`

```php
organizationsServersPhpVersionsShow($organization, $server, $php_version): \Dimer47\Model\OrganizationsServersPhpCliVersionShow200Response
```

Get PHP version

Show the PHP version which has been installed on the server  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID

try {
    $result = $apiInstance->organizationsServersPhpVersionsShow($organization, $server, $php_version);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersPhpCliVersionShow200Response**](../Model/OrganizationsServersPhpCliVersionShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersPhpVersionsStore()`

```php
organizationsServersPhpVersionsStore($organization, $server, $create_php_version_request)
```

Install new PHP version

Install a new PHP version on the server  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_php_version_request = new \Dimer47\Model\CreatePhpVersionRequest(); // \Dimer47\Model\CreatePhpVersionRequest

try {
    $apiInstance->organizationsServersPhpVersionsStore($organization, $server, $create_php_version_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_php_version_request** | [**\Dimer47\Model\CreatePhpVersionRequest**](../Model/CreatePhpVersionRequest.md)|  | |

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

## `organizationsServersPhpVersionsUpdate()`

```php
organizationsServersPhpVersionsUpdate($organization, $server, $php_version)
```

Update installed PHP version

Update PHP version to the latest patch release  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_version = 56; // int | The php version ID

try {
    $apiInstance->organizationsServersPhpVersionsUpdate($organization, $server, $php_version);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersPhpVersionsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_version** | **int**| The php version ID | |

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

## `organizationsServersServicesMysqlActionsStore()`

```php
organizationsServersServicesMysqlActionsStore($organization, $server, $mysql_service_action_request)
```

Perform MySQL action

Run an action on the MySQL service.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$mysql_service_action_request = new \Dimer47\Model\MysqlServiceActionRequest(); // \Dimer47\Model\MysqlServiceActionRequest

try {
    $apiInstance->organizationsServersServicesMysqlActionsStore($organization, $server, $mysql_service_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersServicesMysqlActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **mysql_service_action_request** | [**\Dimer47\Model\MysqlServiceActionRequest**](../Model/MysqlServiceActionRequest.md)|  | |

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

## `organizationsServersServicesNginxActionsStore()`

```php
organizationsServersServicesNginxActionsStore($organization, $server, $nginx_service_action_request)
```

Perform Nginx action

Run an action on the Nginx service.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$nginx_service_action_request = new \Dimer47\Model\NginxServiceActionRequest(); // \Dimer47\Model\NginxServiceActionRequest

try {
    $apiInstance->organizationsServersServicesNginxActionsStore($organization, $server, $nginx_service_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersServicesNginxActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **nginx_service_action_request** | [**\Dimer47\Model\NginxServiceActionRequest**](../Model/NginxServiceActionRequest.md)|  | |

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

## `organizationsServersServicesPhpActionsStore()`

```php
organizationsServersServicesPhpActionsStore($organization, $server, $php_service_action_request)
```

Perform PHP action

Run an action on a specific PHP version.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$php_service_action_request = new \Dimer47\Model\PhpServiceActionRequest(); // \Dimer47\Model\PhpServiceActionRequest

try {
    $apiInstance->organizationsServersServicesPhpActionsStore($organization, $server, $php_service_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersServicesPhpActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **php_service_action_request** | [**\Dimer47\Model\PhpServiceActionRequest**](../Model/PhpServiceActionRequest.md)|  | |

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

## `organizationsServersServicesPostgresActionsStore()`

```php
organizationsServersServicesPostgresActionsStore($organization, $server, $postgres_service_action_request)
```

Perform Postgres action

Run an action on the Postgres service.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$postgres_service_action_request = new \Dimer47\Model\PostgresServiceActionRequest(); // \Dimer47\Model\PostgresServiceActionRequest

try {
    $apiInstance->organizationsServersServicesPostgresActionsStore($organization, $server, $postgres_service_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersServicesPostgresActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **postgres_service_action_request** | [**\Dimer47\Model\PostgresServiceActionRequest**](../Model/PostgresServiceActionRequest.md)|  | |

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

## `organizationsServersServicesRedisActionsStore()`

```php
organizationsServersServicesRedisActionsStore($organization, $server, $redis_service_action_request)
```

Perform Redis action

Run an action on the Redis service.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$redis_service_action_request = new \Dimer47\Model\RedisServiceActionRequest(); // \Dimer47\Model\RedisServiceActionRequest

try {
    $apiInstance->organizationsServersServicesRedisActionsStore($organization, $server, $redis_service_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersServicesRedisActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **redis_service_action_request** | [**\Dimer47\Model\RedisServiceActionRequest**](../Model/RedisServiceActionRequest.md)|  | |

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

## `organizationsServersServicesSupervisorActionsStore()`

```php
organizationsServersServicesSupervisorActionsStore($organization, $server, $supervisor_service_action_request)
```

Perform Supervisor action

Run an action on the Supervisor service.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$supervisor_service_action_request = new \Dimer47\Model\SupervisorServiceActionRequest(); // \Dimer47\Model\SupervisorServiceActionRequest

try {
    $apiInstance->organizationsServersServicesSupervisorActionsStore($organization, $server, $supervisor_service_action_request);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersServicesSupervisorActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **supervisor_service_action_request** | [**\Dimer47\Model\SupervisorServiceActionRequest**](../Model/SupervisorServiceActionRequest.md)|  | |

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

## `organizationsServersShow()`

```php
organizationsServersShow($organization, $server): \Dimer47\Model\OrganizationsServersShow200Response
```

Get server

Show a specific server for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersShow200Response**](../Model/OrganizationsServersShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersStore()`

```php
organizationsServersStore($organization, $organizations_servers_store_request): object
```

Create server

Create a new server in the organization. Supports both standard cloud providers and custom VPS configurations.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$organizations_servers_store_request = new \Dimer47\Model\OrganizationsServersStoreRequest(); // \Dimer47\Model\OrganizationsServersStoreRequest

try {
    $result = $apiInstance->organizationsServersStore($organization, $organizations_servers_store_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsServersStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **organizations_servers_store_request** | [**\Dimer47\Model\OrganizationsServersStoreRequest**](../Model/OrganizationsServersStoreRequest.md)|  | [optional] |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsServersDestroy()`

```php
organizationsTeamsServersDestroy($organization, $team, $server)
```

Delete a server share

Unshare a server with a team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$server = 56; // int | The server ID

try {
    $apiInstance->organizationsTeamsServersDestroy($organization, $team, $server);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsTeamsServersDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **server** | **int**| The server ID | |

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

## `organizationsTeamsServersIndex()`

```php
organizationsTeamsServersIndex($organization, $team, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServersIndex200Response
```

List team servers

Show all servers for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsTeamsServersIndex($organization, $team, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsTeamsServersIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersIndex200Response**](../Model/OrganizationsServersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsServersStore()`

```php
organizationsTeamsServersStore($organization, $team, $share_server_request): \Dimer47\Model\OrganizationsServersShow200Response
```

Create a new server share

Share a server with a team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$share_server_request = new \Dimer47\Model\ShareServerRequest(); // \Dimer47\Model\ShareServerRequest

try {
    $result = $apiInstance->organizationsTeamsServersStore($organization, $team, $share_server_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServersApi->organizationsTeamsServersStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **share_server_request** | [**\Dimer47\Model\ShareServerRequest**](../Model/ShareServerRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersShow200Response**](../Model/OrganizationsServersShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
