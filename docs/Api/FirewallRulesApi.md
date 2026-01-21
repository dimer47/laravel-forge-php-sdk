# Dimer47\FirewallRulesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersFirewallRulesDestroy()**](FirewallRulesApi.md#organizationsServersFirewallRulesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/firewall-rules/{rule} | Delete server firewall rule |
| [**organizationsServersFirewallRulesIndex()**](FirewallRulesApi.md#organizationsServersFirewallRulesIndex) | **GET** /orgs/{organization}/servers/{server}/firewall-rules | List server firewall rules |
| [**organizationsServersFirewallRulesShow()**](FirewallRulesApi.md#organizationsServersFirewallRulesShow) | **GET** /orgs/{organization}/servers/{server}/firewall-rules/{rule} | Get server firewall rule |
| [**organizationsServersFirewallRulesStore()**](FirewallRulesApi.md#organizationsServersFirewallRulesStore) | **POST** /orgs/{organization}/servers/{server}/firewall-rules | Create server firewall rule |


## `organizationsServersFirewallRulesDestroy()`

```php
organizationsServersFirewallRulesDestroy($organization, $server, $rule)
```

Delete server firewall rule

Remove a firewall rule from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\FirewallRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$rule = 56; // int | The rule ID

try {
    $apiInstance->organizationsServersFirewallRulesDestroy($organization, $server, $rule);
} catch (Exception $e) {
    echo 'Exception when calling FirewallRulesApi->organizationsServersFirewallRulesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **rule** | **int**| The rule ID | |

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

## `organizationsServersFirewallRulesIndex()`

```php
organizationsServersFirewallRulesIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status, $filter_ip_address, $filter_type, $filter_port): \Dimer47\Model\OrganizationsServersFirewallRulesIndex200Response
```

List server firewall rules

List all firewall rules associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\FirewallRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string | The name of the firewall rule.
$filter_status = 'filter_status_example'; // string | The status of the firewall rule.
$filter_ip_address = 'filter_ip_address_example'; // string | The IP address or subnet for the firewall rule.
$filter_type = 'filter_type_example'; // string | The type of the firewall rule.
$filter_port = 'filter_port_example'; // string | The port or port range for the firewall rule.

try {
    $result = $apiInstance->organizationsServersFirewallRulesIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_name, $filter_status, $filter_ip_address, $filter_type, $filter_port);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FirewallRulesApi->organizationsServersFirewallRulesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**| The name of the firewall rule. | [optional] |
| **filter_status** | **string**| The status of the firewall rule. | [optional] |
| **filter_ip_address** | **string**| The IP address or subnet for the firewall rule. | [optional] |
| **filter_type** | **string**| The type of the firewall rule. | [optional] |
| **filter_port** | **string**| The port or port range for the firewall rule. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersFirewallRulesIndex200Response**](../Model/OrganizationsServersFirewallRulesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersFirewallRulesShow()`

```php
organizationsServersFirewallRulesShow($organization, $server, $rule): \Dimer47\Model\OrganizationsServersFirewallRulesShow200Response
```

Get server firewall rule

Get a specific firewall rule associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\FirewallRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$rule = 56; // int | The rule ID

try {
    $result = $apiInstance->organizationsServersFirewallRulesShow($organization, $server, $rule);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FirewallRulesApi->organizationsServersFirewallRulesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **rule** | **int**| The rule ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersFirewallRulesShow200Response**](../Model/OrganizationsServersFirewallRulesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersFirewallRulesStore()`

```php
organizationsServersFirewallRulesStore($organization, $server, $create_firewall_rule_request)
```

Create server firewall rule

Add a new firewall rule to the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\FirewallRulesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_firewall_rule_request = new \Dimer47\Model\CreateFirewallRuleRequest(); // \Dimer47\Model\CreateFirewallRuleRequest

try {
    $apiInstance->organizationsServersFirewallRulesStore($organization, $server, $create_firewall_rule_request);
} catch (Exception $e) {
    echo 'Exception when calling FirewallRulesApi->organizationsServersFirewallRulesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_firewall_rule_request** | [**\Dimer47\Model\CreateFirewallRuleRequest**](../Model/CreateFirewallRuleRequest.md)|  | |

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
