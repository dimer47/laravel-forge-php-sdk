# Dimer47\SecurityRulesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersSitesSecurityRulesDestroy()**](SecurityRulesApi.md#organizationsServersSitesSecurityRulesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/security-rules/{securityRule} | Delete site security rule |
| [**organizationsServersSitesSecurityRulesIndex()**](SecurityRulesApi.md#organizationsServersSitesSecurityRulesIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/security-rules | List site security rules |
| [**organizationsServersSitesSecurityRulesShow()**](SecurityRulesApi.md#organizationsServersSitesSecurityRulesShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/security-rules/{securityRule} | Get site security rule |
| [**organizationsServersSitesSecurityRulesStore()**](SecurityRulesApi.md#organizationsServersSitesSecurityRulesStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/security-rules | Create site security rule |
| [**organizationsServersSitesSecurityRulesUpdate()**](SecurityRulesApi.md#organizationsServersSitesSecurityRulesUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/security-rules/{securityRule} | Update site security rule |


## `organizationsServersSitesSecurityRulesDestroy()`

```php
organizationsServersSitesSecurityRulesDestroy($organization, $server, $site, $security_rule)
```

Delete site security rule

Remove a security rule from the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SecurityRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$security_rule = 56; // int | The security rule ID

try {
    $apiInstance->organizationsServersSitesSecurityRulesDestroy($organization, $server, $site, $security_rule);
} catch (Exception $e) {
    echo 'Exception when calling SecurityRulesApi->organizationsServersSitesSecurityRulesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **security_rule** | **int**| The security rule ID | |

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

## `organizationsServersSitesSecurityRulesIndex()`

```php
organizationsServersSitesSecurityRulesIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_path, $filter_status): \Dimer47\Model\OrganizationsServersSitesSecurityRulesIndex200Response
```

List site security rules

List all security rules associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SecurityRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `path`, `status`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-path`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_path = 'filter_path_example'; // string | The path for the security rule.
$filter_status = 'filter_status_example'; // string | The status of the security rule.

try {
    $result = $apiInstance->organizationsServersSitesSecurityRulesIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_path, $filter_status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecurityRulesApi->organizationsServersSitesSecurityRulesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;path&#x60;, &#x60;status&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-path&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_path** | **string**| The path for the security rule. | [optional] |
| **filter_status** | **string**| The status of the security rule. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesSecurityRulesIndex200Response**](../Model/OrganizationsServersSitesSecurityRulesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesSecurityRulesShow()`

```php
organizationsServersSitesSecurityRulesShow($organization, $server, $site, $security_rule): \Dimer47\Model\OrganizationsServersSitesSecurityRulesStore202Response
```

Get site security rule

Get a specific security rule associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SecurityRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$security_rule = 56; // int | The security rule ID

try {
    $result = $apiInstance->organizationsServersSitesSecurityRulesShow($organization, $server, $site, $security_rule);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecurityRulesApi->organizationsServersSitesSecurityRulesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **security_rule** | **int**| The security rule ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesSecurityRulesStore202Response**](../Model/OrganizationsServersSitesSecurityRulesStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesSecurityRulesStore()`

```php
organizationsServersSitesSecurityRulesStore($organization, $server, $site, $create_security_rule_request): \Dimer47\Model\OrganizationsServersSitesSecurityRulesStore202Response
```

Create site security rule

Add a new security rule to the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SecurityRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_security_rule_request = new \Dimer47\Model\CreateSecurityRuleRequest(); // \Dimer47\Model\CreateSecurityRuleRequest

try {
    $result = $apiInstance->organizationsServersSitesSecurityRulesStore($organization, $server, $site, $create_security_rule_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecurityRulesApi->organizationsServersSitesSecurityRulesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_security_rule_request** | [**\Dimer47\Model\CreateSecurityRuleRequest**](../Model/CreateSecurityRuleRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesSecurityRulesStore202Response**](../Model/OrganizationsServersSitesSecurityRulesStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesSecurityRulesUpdate()`

```php
organizationsServersSitesSecurityRulesUpdate($organization, $server, $site, $security_rule, $update_security_rule_request)
```

Update site security rule

Update an existing security rule for a site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SecurityRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$security_rule = 56; // int | The security rule ID
$update_security_rule_request = new \Dimer47\Model\UpdateSecurityRuleRequest(); // \Dimer47\Model\UpdateSecurityRuleRequest

try {
    $apiInstance->organizationsServersSitesSecurityRulesUpdate($organization, $server, $site, $security_rule, $update_security_rule_request);
} catch (Exception $e) {
    echo 'Exception when calling SecurityRulesApi->organizationsServersSitesSecurityRulesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **security_rule** | **int**| The security rule ID | |
| **update_security_rule_request** | [**\Dimer47\Model\UpdateSecurityRuleRequest**](../Model/UpdateSecurityRuleRequest.md)|  | |

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
