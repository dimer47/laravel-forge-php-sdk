# Dimer47\RedirectRulesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersSitesRedirectRulesDestroy()**](RedirectRulesApi.md#organizationsServersSitesRedirectRulesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules/{redirectRule} | Delete site redirect rule |
| [**organizationsServersSitesRedirectRulesIndex()**](RedirectRulesApi.md#organizationsServersSitesRedirectRulesIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules | List site redirect rules |
| [**organizationsServersSitesRedirectRulesShow()**](RedirectRulesApi.md#organizationsServersSitesRedirectRulesShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules/{redirectRule} | Get site redirect rule |
| [**organizationsServersSitesRedirectRulesStore()**](RedirectRulesApi.md#organizationsServersSitesRedirectRulesStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules | Create site redirect rule |


## `organizationsServersSitesRedirectRulesDestroy()`

```php
organizationsServersSitesRedirectRulesDestroy($organization, $server, $site, $redirect_rule)
```

Delete site redirect rule

Remove a redirect rule from the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RedirectRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$redirect_rule = 56; // int | The redirect rule ID

try {
    $apiInstance->organizationsServersSitesRedirectRulesDestroy($organization, $server, $site, $redirect_rule);
} catch (Exception $e) {
    echo 'Exception when calling RedirectRulesApi->organizationsServersSitesRedirectRulesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **redirect_rule** | **int**| The redirect rule ID | |

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

## `organizationsServersSitesRedirectRulesIndex()`

```php
organizationsServersSitesRedirectRulesIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_from, $filter_to, $filter_type, $filter_status): \Dimer47\Model\OrganizationsServersSitesRedirectRulesIndex200Response
```

List site redirect rules

List all redirect rules associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RedirectRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_from = 'filter_from_example'; // string | The source URL path for the redirect rule.
$filter_to = 'filter_to_example'; // string | The destination URL path for the redirect rule.
$filter_type = 'filter_type_example'; // string | The type of the redirect rule.
$filter_status = 'filter_status_example'; // string | The status of the redirect rule.

try {
    $result = $apiInstance->organizationsServersSitesRedirectRulesIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_from, $filter_to, $filter_type, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedirectRulesApi->organizationsServersSitesRedirectRulesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_from** | **string**| The source URL path for the redirect rule. | [optional] |
| **filter_to** | **string**| The destination URL path for the redirect rule. | [optional] |
| **filter_type** | **string**| The type of the redirect rule. | [optional] |
| **filter_status** | **string**| The status of the redirect rule. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesRedirectRulesIndex200Response**](../Model/OrganizationsServersSitesRedirectRulesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesRedirectRulesShow()`

```php
organizationsServersSitesRedirectRulesShow($organization, $server, $site, $redirect_rule): \Dimer47\Model\OrganizationsServersSitesRedirectRulesShow200Response
```

Get site redirect rule

Get a specific redirect rule associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RedirectRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$redirect_rule = 56; // int | The redirect rule ID

try {
    $result = $apiInstance->organizationsServersSitesRedirectRulesShow($organization, $server, $site, $redirect_rule);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedirectRulesApi->organizationsServersSitesRedirectRulesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **redirect_rule** | **int**| The redirect rule ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesRedirectRulesShow200Response**](../Model/OrganizationsServersSitesRedirectRulesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesRedirectRulesStore()`

```php
organizationsServersSitesRedirectRulesStore($organization, $server, $site, $create_redirect_request)
```

Create site redirect rule

Add a new redirect rule to the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RedirectRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_redirect_request = new \Dimer47\Model\CreateRedirectRequest(); // \Dimer47\Model\CreateRedirectRequest

try {
    $apiInstance->organizationsServersSitesRedirectRulesStore($organization, $server, $site, $create_redirect_request);
} catch (Exception $e) {
    echo 'Exception when calling RedirectRulesApi->organizationsServersSitesRedirectRulesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_redirect_request** | [**\Dimer47\Model\CreateRedirectRequest**](../Model/CreateRedirectRequest.md)|  | |

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
