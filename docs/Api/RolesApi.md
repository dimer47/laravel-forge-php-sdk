# Dimer47\RolesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsRolesDestroy()**](RolesApi.md#organizationsRolesDestroy) | **DELETE** /orgs/{organization}/roles/{role} | Delete role |
| [**organizationsRolesIndex()**](RolesApi.md#organizationsRolesIndex) | **GET** /orgs/{organization}/roles | List roles |
| [**organizationsRolesPermissionsIndex()**](RolesApi.md#organizationsRolesPermissionsIndex) | **GET** /orgs/{organization}/roles/{role}/permissions | List role permissions |
| [**organizationsRolesShow()**](RolesApi.md#organizationsRolesShow) | **GET** /orgs/{organization}/roles/{role} | Get role |
| [**organizationsRolesStore()**](RolesApi.md#organizationsRolesStore) | **POST** /orgs/{organization}/roles | Create role |
| [**organizationsRolesUpdate()**](RolesApi.md#organizationsRolesUpdate) | **PUT** /orgs/{organization}/roles/{role} | Update role |
| [**permissionsIndex()**](RolesApi.md#permissionsIndex) | **GET** /permissions | List permissions |
| [**permissionsShow()**](RolesApi.md#permissionsShow) | **GET** /permissions/{permission} | Get permission |
| [**predefinedRolesIndex()**](RolesApi.md#predefinedRolesIndex) | **GET** /predefined-roles | List predefined roles |
| [**predefinedRolesShow()**](RolesApi.md#predefinedRolesShow) | **GET** /predefined-roles/{role} | Get predefined role |


## `organizationsRolesDestroy()`

```php
organizationsRolesDestroy($organization, $role)
```

Delete role

Delete a role from the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$role = 56; // int | The role ID

try {
    $apiInstance->organizationsRolesDestroy($organization, $role);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->organizationsRolesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **role** | **int**| The role ID | |

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

## `organizationsRolesIndex()`

```php
organizationsRolesIndex($organization, $include, $page_size, $page_cursor, $filter_name, $filter_permissions_name): \Dimer47\Model\OrganizationsRolesIndex200Response
```

List roles

Show all roles for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$include = 'include_example'; // string | Available includes are `permissions`, `permissionsCount`, `permissionsExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string
$filter_permissions_name = 'filter_permissions_name_example'; // string

try {
    $result = $apiInstance->organizationsRolesIndex($organization, $include, $page_size, $page_cursor, $filter_name, $filter_permissions_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->organizationsRolesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **include** | **string**| Available includes are &#x60;permissions&#x60;, &#x60;permissionsCount&#x60;, &#x60;permissionsExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |
| **filter_permissions_name** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsRolesIndex200Response**](../Model/OrganizationsRolesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRolesPermissionsIndex()`

```php
organizationsRolesPermissionsIndex($organization, $role, $page_size, $page_cursor, $filter_name): \Dimer47\Model\PermissionsIndex200Response
```

List role permissions

Show all permissions for the role.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$role = 56; // int | The role ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string

try {
    $result = $apiInstance->organizationsRolesPermissionsIndex($organization, $role, $page_size, $page_cursor, $filter_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->organizationsRolesPermissionsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **role** | **int**| The role ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\PermissionsIndex200Response**](../Model/PermissionsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRolesShow()`

```php
organizationsRolesShow($organization, $role): \Dimer47\Model\OrganizationsRolesStore200Response
```

Get role

Show a specific role for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$role = 56; // int | The role ID

try {
    $result = $apiInstance->organizationsRolesShow($organization, $role);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->organizationsRolesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **role** | **int**| The role ID | |

### Return type

[**\Dimer47\Model\OrganizationsRolesStore200Response**](../Model/OrganizationsRolesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRolesStore()`

```php
organizationsRolesStore($organization, $create_role_request): \Dimer47\Model\OrganizationsRolesStore200Response
```

Create role

Create a new role for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$create_role_request = new \Dimer47\Model\CreateRoleRequest(); // \Dimer47\Model\CreateRoleRequest

try {
    $result = $apiInstance->organizationsRolesStore($organization, $create_role_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->organizationsRolesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **create_role_request** | [**\Dimer47\Model\CreateRoleRequest**](../Model/CreateRoleRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsRolesStore200Response**](../Model/OrganizationsRolesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRolesUpdate()`

```php
organizationsRolesUpdate($organization, $role, $organizations_roles_update_request): \Dimer47\Model\OrganizationsRolesStore200Response
```

Update role

Update a role for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$role = 56; // int | The role ID
$organizations_roles_update_request = new \Dimer47\Model\OrganizationsRolesUpdateRequest(); // \Dimer47\Model\OrganizationsRolesUpdateRequest

try {
    $result = $apiInstance->organizationsRolesUpdate($organization, $role, $organizations_roles_update_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->organizationsRolesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **role** | **int**| The role ID | |
| **organizations_roles_update_request** | [**\Dimer47\Model\OrganizationsRolesUpdateRequest**](../Model/OrganizationsRolesUpdateRequest.md)|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsRolesStore200Response**](../Model/OrganizationsRolesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `permissionsIndex()`

```php
permissionsIndex($page_size, $page_cursor, $filter_name): \Dimer47\Model\PermissionsIndex200Response
```

List permissions

Show all permissions.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string

try {
    $result = $apiInstance->permissionsIndex($page_size, $page_cursor, $filter_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->permissionsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\PermissionsIndex200Response**](../Model/PermissionsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `permissionsShow()`

```php
permissionsShow($permission): \Dimer47\Model\PermissionsShow200Response
```

Get permission

Show a specific permission.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$permission = 56; // int | The permission ID

try {
    $result = $apiInstance->permissionsShow($permission);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->permissionsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **permission** | **int**| The permission ID | |

### Return type

[**\Dimer47\Model\PermissionsShow200Response**](../Model/PermissionsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `predefinedRolesIndex()`

```php
predefinedRolesIndex($include, $page_size, $page_cursor, $filter_name, $filter_permissions_name): \Dimer47\Model\PredefinedRolesIndex200Response
```

List predefined roles

Show all predefined roles.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include = 'include_example'; // string | Available includes are `permissions`, `permissionsCount`, `permissionsExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string
$filter_permissions_name = 'filter_permissions_name_example'; // string

try {
    $result = $apiInstance->predefinedRolesIndex($include, $page_size, $page_cursor, $filter_name, $filter_permissions_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->predefinedRolesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **include** | **string**| Available includes are &#x60;permissions&#x60;, &#x60;permissionsCount&#x60;, &#x60;permissionsExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |
| **filter_permissions_name** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\PredefinedRolesIndex200Response**](../Model/PredefinedRolesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `predefinedRolesShow()`

```php
predefinedRolesShow($role): \Dimer47\Model\PredefinedRolesShow200Response
```

Get predefined role

Show a specific predefined role.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RolesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$role = 56; // int | The role ID

try {
    $result = $apiInstance->predefinedRolesShow($role);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RolesApi->predefinedRolesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **role** | **int**| The role ID | |

### Return type

[**\Dimer47\Model\PredefinedRolesShow200Response**](../Model/PredefinedRolesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
