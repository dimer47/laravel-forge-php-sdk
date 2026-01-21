# Dimer47\SSHKeysApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersKeyShow()**](SSHKeysApi.md#organizationsServersKeyShow) | **GET** /orgs/{organization}/servers/{server}/key | Get server public SSH key |
| [**organizationsServersKeyUpdate()**](SSHKeysApi.md#organizationsServersKeyUpdate) | **PUT** /orgs/{organization}/servers/{server}/key | Update server public SSH key |
| [**organizationsServersSshKeysDestroy()**](SSHKeysApi.md#organizationsServersSshKeysDestroy) | **DELETE** /orgs/{organization}/servers/{server}/ssh-keys/{key} | Delete server SSH key |
| [**organizationsServersSshKeysIndex()**](SSHKeysApi.md#organizationsServersSshKeysIndex) | **GET** /orgs/{organization}/servers/{server}/ssh-keys | List server SSH keys |
| [**organizationsServersSshKeysShow()**](SSHKeysApi.md#organizationsServersSshKeysShow) | **GET** /orgs/{organization}/servers/{server}/ssh-keys/{key} | Get server SSH key |
| [**organizationsServersSshKeysStore()**](SSHKeysApi.md#organizationsServersSshKeysStore) | **POST** /orgs/{organization}/servers/{server}/ssh-keys | Create server SSH key |


## `organizationsServersKeyShow()`

```php
organizationsServersKeyShow($organization, $server): \Dimer47\Model\OrganizationsServersKeyShow200Response
```

Get server public SSH key

Get the public SSH key for the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SSHKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersKeyShow($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSHKeysApi->organizationsServersKeyShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersKeyShow200Response**](../Model/OrganizationsServersKeyShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersKeyUpdate()`

```php
organizationsServersKeyUpdate($organization, $server): \Dimer47\Model\OrganizationsServersKeyShow200Response
```

Update server public SSH key

Regenerate the SSH key pair for the server and return the new public key.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SSHKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID

try {
    $result = $apiInstance->organizationsServersKeyUpdate($organization, $server);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSHKeysApi->organizationsServersKeyUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersKeyShow200Response**](../Model/OrganizationsServersKeyShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSshKeysDestroy()`

```php
organizationsServersSshKeysDestroy($organization, $server, $key)
```

Delete server SSH key

Remove an SSH key from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SSHKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$key = 56; // int | The key ID

try {
    $apiInstance->organizationsServersSshKeysDestroy($organization, $server, $key);
} catch (Exception $e) {
    echo 'Exception when calling SSHKeysApi->organizationsServersSshKeysDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **key** | **int**| The key ID | |

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

## `organizationsServersSshKeysIndex()`

```php
organizationsServersSshKeysIndex($organization, $server, $page_size, $page_cursor, $filter_name, $filter_user): \Dimer47\Model\OrganizationsServersSshKeysIndex200Response
```

List server SSH keys

List all SSH keys associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SSHKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string
$filter_user = 'filter_user_example'; // string

try {
    $result = $apiInstance->organizationsServersSshKeysIndex($organization, $server, $page_size, $page_cursor, $filter_name, $filter_user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSHKeysApi->organizationsServersSshKeysIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |
| **filter_user** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSshKeysIndex200Response**](../Model/OrganizationsServersSshKeysIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSshKeysShow()`

```php
organizationsServersSshKeysShow($organization, $server, $key): \Dimer47\Model\OrganizationsServersSshKeysShow200Response
```

Get server SSH key

Get a specific SSH key associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SSHKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$key = 56; // int | The key ID

try {
    $result = $apiInstance->organizationsServersSshKeysShow($organization, $server, $key);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SSHKeysApi->organizationsServersSshKeysShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **key** | **int**| The key ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSshKeysShow200Response**](../Model/OrganizationsServersSshKeysShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSshKeysStore()`

```php
organizationsServersSshKeysStore($organization, $server, $create_ssh_key_request)
```

Create server SSH key

Add a new SSH key to the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SSHKeysApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_ssh_key_request = new \Dimer47\Model\CreateSshKeyRequest(); // \Dimer47\Model\CreateSshKeyRequest

try {
    $apiInstance->organizationsServersSshKeysStore($organization, $server, $create_ssh_key_request);
} catch (Exception $e) {
    echo 'Exception when calling SSHKeysApi->organizationsServersSshKeysStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_ssh_key_request** | [**\Dimer47\Model\CreateSshKeyRequest**](../Model/CreateSshKeyRequest.md)|  | |

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
