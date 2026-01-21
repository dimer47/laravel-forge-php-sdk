# Dimer47\DatabasesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersDatabasePasswordUpdate()**](DatabasesApi.md#organizationsServersDatabasePasswordUpdate) | **PUT** /orgs/{organization}/servers/{server}/database/password | Update the password for the database |
| [**organizationsServersDatabaseSchemasDestroy()**](DatabasesApi.md#organizationsServersDatabaseSchemasDestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/schemas/{database} | Delete database schema |
| [**organizationsServersDatabaseSchemasIndex()**](DatabasesApi.md#organizationsServersDatabaseSchemasIndex) | **GET** /orgs/{organization}/servers/{server}/database/schemas | List database schemas |
| [**organizationsServersDatabaseSchemasShow()**](DatabasesApi.md#organizationsServersDatabaseSchemasShow) | **GET** /orgs/{organization}/servers/{server}/database/schemas/{database} | Get database schema |
| [**organizationsServersDatabaseSchemasStore()**](DatabasesApi.md#organizationsServersDatabaseSchemasStore) | **POST** /orgs/{organization}/servers/{server}/database/schemas | Create database schema |
| [**organizationsServersDatabaseSchemasSynchronizationsStore()**](DatabasesApi.md#organizationsServersDatabaseSchemasSynchronizationsStore) | **POST** /orgs/{organization}/servers/{server}/database/schemas/synchronizations | Update database schemas |
| [**organizationsServersDatabaseUsersDestroy()**](DatabasesApi.md#organizationsServersDatabaseUsersDestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/users/{databaseUser} | Delete database user |
| [**organizationsServersDatabaseUsersIndex()**](DatabasesApi.md#organizationsServersDatabaseUsersIndex) | **GET** /orgs/{organization}/servers/{server}/database/users | List database users |
| [**organizationsServersDatabaseUsersShow()**](DatabasesApi.md#organizationsServersDatabaseUsersShow) | **GET** /orgs/{organization}/servers/{server}/database/users/{databaseUser} | Get database user |
| [**organizationsServersDatabaseUsersStore()**](DatabasesApi.md#organizationsServersDatabaseUsersStore) | **POST** /orgs/{organization}/servers/{server}/database/users | Create database user |
| [**organizationsServersDatabaseUsersUpdate()**](DatabasesApi.md#organizationsServersDatabaseUsersUpdate) | **PUT** /orgs/{organization}/servers/{server}/database/users/{databaseUser} | Update database user |


## `organizationsServersDatabasePasswordUpdate()`

```php
organizationsServersDatabasePasswordUpdate($organization, $server, $update_database_password_request)
```

Update the password for the database

Update the password for the database on the server. It will only update the password Forge thinks is the password, it will not change the password on the server itself. This should only be used if you have changed the password on the server itself and want to update Forge.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$update_database_password_request = new \Dimer47\Model\UpdateDatabasePasswordRequest(); // \Dimer47\Model\UpdateDatabasePasswordRequest

try {
    $apiInstance->organizationsServersDatabasePasswordUpdate($organization, $server, $update_database_password_request);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabasePasswordUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **update_database_password_request** | [**\Dimer47\Model\UpdateDatabasePasswordRequest**](../Model/UpdateDatabasePasswordRequest.md)|  | |

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

## `organizationsServersDatabaseSchemasDestroy()`

```php
organizationsServersDatabaseSchemasDestroy($organization, $server, $database)
```

Delete database schema

Remove a database schema from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$database = 56; // int | The database ID

try {
    $apiInstance->organizationsServersDatabaseSchemasDestroy($organization, $server, $database);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseSchemasDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **database** | **int**| The database ID | |

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

## `organizationsServersDatabaseSchemasIndex()`

```php
organizationsServersDatabaseSchemasIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status): \Dimer47\Model\OrganizationsServersDatabaseSchemasIndex200Response
```

List database schemas

List all database schemas associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
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
$filter_name = 'filter_name_example'; // string | The name of the database schema.
$filter_status = 'filter_status_example'; // string | The status of the database schema.

try {
    $result = $apiInstance->organizationsServersDatabaseSchemasIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseSchemasIndex: ', $e->getMessage(), PHP_EOL;
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
| **filter_name** | **string**| The name of the database schema. | [optional] |
| **filter_status** | **string**| The status of the database schema. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseSchemasIndex200Response**](../Model/OrganizationsServersDatabaseSchemasIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseSchemasShow()`

```php
organizationsServersDatabaseSchemasShow($organization, $server, $database): \Dimer47\Model\OrganizationsServersDatabaseSchemasStore202Response
```

Get database schema

Get a specific database schema associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$database = 56; // int | The database ID

try {
    $result = $apiInstance->organizationsServersDatabaseSchemasShow($organization, $server, $database);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseSchemasShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **database** | **int**| The database ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseSchemasStore202Response**](../Model/OrganizationsServersDatabaseSchemasStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseSchemasStore()`

```php
organizationsServersDatabaseSchemasStore($organization, $server, $create_database_request): \Dimer47\Model\OrganizationsServersDatabaseSchemasStore202Response
```

Create database schema

Add a new database schema to the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_database_request = new \Dimer47\Model\CreateDatabaseRequest(); // \Dimer47\Model\CreateDatabaseRequest

try {
    $result = $apiInstance->organizationsServersDatabaseSchemasStore($organization, $server, $create_database_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseSchemasStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_database_request** | [**\Dimer47\Model\CreateDatabaseRequest**](../Model/CreateDatabaseRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseSchemasStore202Response**](../Model/OrganizationsServersDatabaseSchemasStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseSchemasSynchronizationsStore()`

```php
organizationsServersDatabaseSchemasSynchronizationsStore($organization, $server)
```

Update database schemas

Synchronize all database schemas on the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $apiInstance->organizationsServersDatabaseSchemasSynchronizationsStore($organization, $server);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseSchemasSynchronizationsStore: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersDatabaseUsersDestroy()`

```php
organizationsServersDatabaseUsersDestroy($organization, $server, $database_user)
```

Delete database user

Remove a database user from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$database_user = 56; // int | The database user ID

try {
    $apiInstance->organizationsServersDatabaseUsersDestroy($organization, $server, $database_user);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseUsersDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **database_user** | **int**| The database user ID | |

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

## `organizationsServersDatabaseUsersIndex()`

```php
organizationsServersDatabaseUsersIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status): \Dimer47\Model\OrganizationsServersDatabaseUsersIndex200Response
```

List database users

List all database users associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
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
$filter_name = 'filter_name_example'; // string | The name of the database user.
$filter_status = 'filter_status_example'; // string | The status of the database user.

try {
    $result = $apiInstance->organizationsServersDatabaseUsersIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseUsersIndex: ', $e->getMessage(), PHP_EOL;
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
| **filter_name** | **string**| The name of the database user. | [optional] |
| **filter_status** | **string**| The status of the database user. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseUsersIndex200Response**](../Model/OrganizationsServersDatabaseUsersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseUsersShow()`

```php
organizationsServersDatabaseUsersShow($organization, $server, $database_user): \Dimer47\Model\OrganizationsServersDatabaseUsersStore202Response
```

Get database user

Get a specific database user associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$database_user = 56; // int | The database user ID

try {
    $result = $apiInstance->organizationsServersDatabaseUsersShow($organization, $server, $database_user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseUsersShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **database_user** | **int**| The database user ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseUsersStore202Response**](../Model/OrganizationsServersDatabaseUsersStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseUsersStore()`

```php
organizationsServersDatabaseUsersStore($organization, $server, $create_database_user_request): \Dimer47\Model\OrganizationsServersDatabaseUsersStore202Response
```

Create database user

Add a new database user to the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_database_user_request = new \Dimer47\Model\CreateDatabaseUserRequest(); // \Dimer47\Model\CreateDatabaseUserRequest

try {
    $result = $apiInstance->organizationsServersDatabaseUsersStore($organization, $server, $create_database_user_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseUsersStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_database_user_request** | [**\Dimer47\Model\CreateDatabaseUserRequest**](../Model/CreateDatabaseUserRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersDatabaseUsersStore202Response**](../Model/OrganizationsServersDatabaseUsersStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersDatabaseUsersUpdate()`

```php
organizationsServersDatabaseUsersUpdate($organization, $server, $database_user, $update_database_user_request)
```

Update database user

Update a database user on the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DatabasesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$database_user = 56; // int | The database user ID
$update_database_user_request = new \Dimer47\Model\UpdateDatabaseUserRequest(); // \Dimer47\Model\UpdateDatabaseUserRequest

try {
    $apiInstance->organizationsServersDatabaseUsersUpdate($organization, $server, $database_user, $update_database_user_request);
} catch (Exception $e) {
    echo 'Exception when calling DatabasesApi->organizationsServersDatabaseUsersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **database_user** | **int**| The database user ID | |
| **update_database_user_request** | [**\Dimer47\Model\UpdateDatabaseUserRequest**](../Model/UpdateDatabaseUserRequest.md)|  | [optional] |

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
