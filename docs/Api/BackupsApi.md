# Dimer47\BackupsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersDatabaseBackupsDestroy()**](BackupsApi.md#organizationsServersDatabaseBackupsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration} | Delete backup configuration |
| [**organizationsServersDatabaseBackupsIndex()**](BackupsApi.md#organizationsServersDatabaseBackupsIndex) | **GET** /orgs/{organization}/servers/{server}/database/backups | List backup configurations |
| [**organizationsServersDatabaseBackupsInstancesDestroy()**](BackupsApi.md#organizationsServersDatabaseBackupsInstancesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances/{backup} | Delete backup |
| [**organizationsServersDatabaseBackupsInstancesIndex()**](BackupsApi.md#organizationsServersDatabaseBackupsInstancesIndex) | **GET** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances | List backups |
| [**organizationsServersDatabaseBackupsInstancesRestoresStore()**](BackupsApi.md#organizationsServersDatabaseBackupsInstancesRestoresStore) | **POST** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances/{backup}/restores | Create a database restore from backup |
| [**organizationsServersDatabaseBackupsInstancesShow()**](BackupsApi.md#organizationsServersDatabaseBackupsInstancesShow) | **GET** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances/{backup} | Get backup |
| [**organizationsServersDatabaseBackupsInstancesStore()**](BackupsApi.md#organizationsServersDatabaseBackupsInstancesStore) | **POST** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances | Create backup |
| [**organizationsServersDatabaseBackupsShow()**](BackupsApi.md#organizationsServersDatabaseBackupsShow) | **GET** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration} | Get backup configuration |
| [**organizationsServersDatabaseBackupsStore()**](BackupsApi.md#organizationsServersDatabaseBackupsStore) | **POST** /orgs/{organization}/servers/{server}/database/backups | Create backup configuration |
| [**organizationsServersDatabaseBackupsUpdate()**](BackupsApi.md#organizationsServersDatabaseBackupsUpdate) | **PUT** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration} | Update backup configuration |


## `organizationsServersDatabaseBackupsDestroy()`

```php
organizationsServersDatabaseBackupsDestroy($organization, $server, $backup_configuration)
```

Delete backup configuration

Delete a backup configuration from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID

try {
    $apiInstance->organizationsServersDatabaseBackupsDestroy($organization, $server, $backup_configuration);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |

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

## `organizationsServersDatabaseBackupsIndex()`

```php
organizationsServersDatabaseBackupsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status): \Dimer47\Model\OrganizationsServersDatabaseBackupsIndex200Response
```

List backup configurations

List all backup configurations for the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `name`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-name`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string | The name of the backup configuration.
$filter_status = 'filter_status_example'; // string | The status of the backup configuration.

try {
    $result = $apiInstance->organizationsServersDatabaseBackupsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;name&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-name&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**| The name of the backup configuration. | [optional] |
| **filter_status** | **string**| The status of the backup configuration. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseBackupsIndex200Response**](../Model/OrganizationsServersDatabaseBackupsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseBackupsInstancesDestroy()`

```php
organizationsServersDatabaseBackupsInstancesDestroy($organization, $server, $backup_configuration, $backup)
```

Delete backup

Delete a backup instance from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID
$backup = 56; // int | The backup ID

try {
    $apiInstance->organizationsServersDatabaseBackupsInstancesDestroy($organization, $server, $backup_configuration, $backup);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsInstancesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |
| **backup** | **int**| The backup ID | |

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

## `organizationsServersDatabaseBackupsInstancesIndex()`

```php
organizationsServersDatabaseBackupsInstancesIndex($organization, $server, $backup_configuration, $sort, $page_size, $page_cursor, $filter_status): \Dimer47\Model\OrganizationsServersDatabaseBackupsInstancesIndex200Response
```

List backups

List all backup instances for the backup configuration.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_status = 'filter_status_example'; // string | The status of the backup.

try {
    $result = $apiInstance->organizationsServersDatabaseBackupsInstancesIndex($organization, $server, $backup_configuration, $sort, $page_size, $page_cursor, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsInstancesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_status** | **string**| The status of the backup. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseBackupsInstancesIndex200Response**](../Model/OrganizationsServersDatabaseBackupsInstancesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseBackupsInstancesRestoresStore()`

```php
organizationsServersDatabaseBackupsInstancesRestoresStore($organization, $server, $backup_configuration, $backup, $restore_backup_request)
```

Create a database restore from backup

Restore the given database from the backup.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID
$backup = 56; // int | The backup ID
$restore_backup_request = new \Dimer47\Model\RestoreBackupRequest(); // \Dimer47\Model\RestoreBackupRequest

try {
    $apiInstance->organizationsServersDatabaseBackupsInstancesRestoresStore($organization, $server, $backup_configuration, $backup, $restore_backup_request);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsInstancesRestoresStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |
| **backup** | **int**| The backup ID | |
| **restore_backup_request** | [**\Dimer47\Model\RestoreBackupRequest**](../Model/RestoreBackupRequest.md)|  | |

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

## `organizationsServersDatabaseBackupsInstancesShow()`

```php
organizationsServersDatabaseBackupsInstancesShow($organization, $server, $backup_configuration, $backup): \Dimer47\Model\OrganizationsServersDatabaseBackupsInstancesShow200Response
```

Get backup

Get a specific backup instance associated with the backup configuration.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID
$backup = 56; // int | The backup ID

try {
    $result = $apiInstance->organizationsServersDatabaseBackupsInstancesShow($organization, $server, $backup_configuration, $backup);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsInstancesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |
| **backup** | **int**| The backup ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseBackupsInstancesShow200Response**](../Model/OrganizationsServersDatabaseBackupsInstancesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseBackupsInstancesStore()`

```php
organizationsServersDatabaseBackupsInstancesStore($organization, $server, $backup_configuration)
```

Create backup

Manually create a backup for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID

try {
    $apiInstance->organizationsServersDatabaseBackupsInstancesStore($organization, $server, $backup_configuration);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsInstancesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |

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

## `organizationsServersDatabaseBackupsShow()`

```php
organizationsServersDatabaseBackupsShow($organization, $server, $backup_configuration): \Dimer47\Model\OrganizationsServersDatabaseBackupsShow200Response
```

Get backup configuration

Get a specific backup configuration for the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID

try {
    $result = $apiInstance->organizationsServersDatabaseBackupsShow($organization, $server, $backup_configuration);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseBackupsShow200Response**](../Model/OrganizationsServersDatabaseBackupsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseBackupsStore()`

```php
organizationsServersDatabaseBackupsStore($organization, $server, $create_backup_configuration_request)
```

Create backup configuration

Create a new backup configuration for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_backup_configuration_request = new \Dimer47\Model\CreateBackupConfigurationRequest(); // \Dimer47\Model\CreateBackupConfigurationRequest

try {
    $apiInstance->organizationsServersDatabaseBackupsStore($organization, $server, $create_backup_configuration_request);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_backup_configuration_request** | [**\Dimer47\Model\CreateBackupConfigurationRequest**](../Model/CreateBackupConfigurationRequest.md)|  | |

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

## `organizationsServersDatabaseBackupsUpdate()`

```php
organizationsServersDatabaseBackupsUpdate($organization, $server, $backup_configuration, $update_backup_configuration_request)
```

Update backup configuration

Update an existing backup configuration for the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\BackupsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$backup_configuration = 56; // int | The backup configuration ID
$update_backup_configuration_request = new \Dimer47\Model\UpdateBackupConfigurationRequest(); // \Dimer47\Model\UpdateBackupConfigurationRequest

try {
    $apiInstance->organizationsServersDatabaseBackupsUpdate($organization, $server, $backup_configuration, $update_backup_configuration_request);
} catch (Exception $e) {
    echo 'Exception when calling BackupsApi->organizationsServersDatabaseBackupsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **backup_configuration** | **int**| The backup configuration ID | |
| **update_backup_configuration_request** | [**\Dimer47\Model\UpdateBackupConfigurationRequest**](../Model/UpdateBackupConfigurationRequest.md)|  | |

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
