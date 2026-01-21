# Dimer47\NginxApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersNginxTemplatesDestroy()**](NginxApi.md#organizationsServersNginxTemplatesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/nginx/templates/{nginxTemplate} | Delete Nginx template |
| [**organizationsServersNginxTemplatesIndex()**](NginxApi.md#organizationsServersNginxTemplatesIndex) | **GET** /orgs/{organization}/servers/{server}/nginx/templates | List Nginx templates |
| [**organizationsServersNginxTemplatesShow()**](NginxApi.md#organizationsServersNginxTemplatesShow) | **GET** /orgs/{organization}/servers/{server}/nginx/templates/{nginxTemplate} | Get Nginx template |
| [**organizationsServersNginxTemplatesStore()**](NginxApi.md#organizationsServersNginxTemplatesStore) | **POST** /orgs/{organization}/servers/{server}/nginx/templates | Create Nginx template |
| [**organizationsServersNginxTemplatesUpdate()**](NginxApi.md#organizationsServersNginxTemplatesUpdate) | **PUT** /orgs/{organization}/servers/{server}/nginx/templates/{nginxTemplate} | Update Nginx template |


## `organizationsServersNginxTemplatesDestroy()`

```php
organizationsServersNginxTemplatesDestroy($organization, $server, $nginx_template)
```

Delete Nginx template

Delete the specified nginx template from the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\NginxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$nginx_template = 56; // int | The nginx template ID

try {
    $apiInstance->organizationsServersNginxTemplatesDestroy($organization, $server, $nginx_template);
} catch (Exception $e) {
    echo 'Exception when calling NginxApi->organizationsServersNginxTemplatesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **nginx_template** | **int**| The nginx template ID | |

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

## `organizationsServersNginxTemplatesIndex()`

```php
organizationsServersNginxTemplatesIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name): \Dimer47\Model\OrganizationsServersNginxTemplatesIndex200Response
```

List Nginx templates

List all nginx templates for the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\NginxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`, `name`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string | The name of the template.

try {
    $result = $apiInstance->organizationsServersNginxTemplatesIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NginxApi->organizationsServersNginxTemplatesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;, &#x60;name&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**| The name of the template. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersNginxTemplatesIndex200Response**](../Model/OrganizationsServersNginxTemplatesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersNginxTemplatesShow()`

```php
organizationsServersNginxTemplatesShow($organization, $server, $nginx_template): \Dimer47\Model\OrganizationsServersNginxTemplatesStore200Response
```

Get Nginx template

Get a specific nginx template associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\NginxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$nginx_template = 56; // int | The nginx template ID

try {
    $result = $apiInstance->organizationsServersNginxTemplatesShow($organization, $server, $nginx_template);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NginxApi->organizationsServersNginxTemplatesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **nginx_template** | **int**| The nginx template ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersNginxTemplatesStore200Response**](../Model/OrganizationsServersNginxTemplatesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersNginxTemplatesStore()`

```php
organizationsServersNginxTemplatesStore($organization, $server, $create_nginx_template_request): \Dimer47\Model\OrganizationsServersNginxTemplatesStore200Response
```

Create Nginx template

Create a new nginx template on the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\NginxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_nginx_template_request = new \Dimer47\Model\CreateNginxTemplateRequest(); // \Dimer47\Model\CreateNginxTemplateRequest

try {
    $result = $apiInstance->organizationsServersNginxTemplatesStore($organization, $server, $create_nginx_template_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NginxApi->organizationsServersNginxTemplatesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_nginx_template_request** | [**\Dimer47\Model\CreateNginxTemplateRequest**](../Model/CreateNginxTemplateRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersNginxTemplatesStore200Response**](../Model/OrganizationsServersNginxTemplatesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersNginxTemplatesUpdate()`

```php
organizationsServersNginxTemplatesUpdate($organization, $server, $nginx_template, $update_nginx_template_request): \Dimer47\Model\OrganizationsServersNginxTemplatesStore200Response
```

Update Nginx template

Update the specified nginx template on the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\NginxApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$nginx_template = 56; // int | The nginx template ID
$update_nginx_template_request = new \Dimer47\Model\UpdateNginxTemplateRequest(); // \Dimer47\Model\UpdateNginxTemplateRequest

try {
    $result = $apiInstance->organizationsServersNginxTemplatesUpdate($organization, $server, $nginx_template, $update_nginx_template_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NginxApi->organizationsServersNginxTemplatesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **nginx_template** | **int**| The nginx template ID | |
| **update_nginx_template_request** | [**\Dimer47\Model\UpdateNginxTemplateRequest**](../Model/UpdateNginxTemplateRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersNginxTemplatesStore200Response**](../Model/OrganizationsServersNginxTemplatesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
