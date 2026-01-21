# Dimer47\ScheduledJobsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersScheduledJobsDestroy()**](ScheduledJobsApi.md#organizationsServersScheduledJobsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/scheduled-jobs/{job} | Delete scheduled job |
| [**organizationsServersScheduledJobsIndex()**](ScheduledJobsApi.md#organizationsServersScheduledJobsIndex) | **GET** /orgs/{organization}/servers/{server}/scheduled-jobs | List server scheduled jobs |
| [**organizationsServersScheduledJobsOutputsShow()**](ScheduledJobsApi.md#organizationsServersScheduledJobsOutputsShow) | **GET** /orgs/{organization}/servers/{server}/scheduled-jobs/{job}/output | Get scheduled job output |
| [**organizationsServersScheduledJobsShow()**](ScheduledJobsApi.md#organizationsServersScheduledJobsShow) | **GET** /orgs/{organization}/servers/{server}/scheduled-jobs/{job} | Get scheduled job |
| [**organizationsServersScheduledJobsStore()**](ScheduledJobsApi.md#organizationsServersScheduledJobsStore) | **POST** /orgs/{organization}/servers/{server}/scheduled-jobs | Create scheduled job |
| [**organizationsServersSitesScheduledJobsDestroy()**](ScheduledJobsApi.md#organizationsServersSitesScheduledJobsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/scheduled-jobs/{job} | Delete site scheduled job |
| [**organizationsServersSitesScheduledJobsIndex()**](ScheduledJobsApi.md#organizationsServersSitesScheduledJobsIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/scheduled-jobs | List site scheduled jobs |
| [**organizationsServersSitesScheduledJobsOutputsShow()**](ScheduledJobsApi.md#organizationsServersSitesScheduledJobsOutputsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/scheduled-jobs/{job}/output | Get site scheduled job output |
| [**organizationsServersSitesScheduledJobsShow()**](ScheduledJobsApi.md#organizationsServersSitesScheduledJobsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/scheduled-jobs/{job} | Get site scheduled job |
| [**organizationsServersSitesScheduledJobsStore()**](ScheduledJobsApi.md#organizationsServersSitesScheduledJobsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/scheduled-jobs | Create site scheduled job |


## `organizationsServersScheduledJobsDestroy()`

```php
organizationsServersScheduledJobsDestroy($organization, $server, $job)
```

Delete scheduled job

Delete a specific scheduled job.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$job = 56; // int | The job ID

try {
    $apiInstance->organizationsServersScheduledJobsDestroy($organization, $server, $job);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersScheduledJobsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **job** | **int**| The job ID | |

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

## `organizationsServersScheduledJobsIndex()`

```php
organizationsServersScheduledJobsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_status, $filter_user): \Dimer47\Model\OrganizationsServersScheduledJobsIndex200Response
```

List server scheduled jobs

List all scheduled jobs associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`, `status`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_status = 'filter_status_example'; // string
$filter_user = 'filter_user_example'; // string

try {
    $result = $apiInstance->organizationsServersScheduledJobsIndex($organization, $server, $sort, $page_size, $page_cursor, $filter_status, $filter_user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersScheduledJobsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;, &#x60;status&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_status** | **string**|  | [optional] |
| **filter_user** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsIndex200Response**](../Model/OrganizationsServersScheduledJobsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersScheduledJobsOutputsShow()`

```php
organizationsServersScheduledJobsOutputsShow($organization, $server, $job): \Dimer47\Model\OrganizationsServersScheduledJobsOutputsShow200Response
```

Get scheduled job output

Show a specific scheduled job output.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$job = 56; // int | The job ID

try {
    $result = $apiInstance->organizationsServersScheduledJobsOutputsShow($organization, $server, $job);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersScheduledJobsOutputsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **job** | **int**| The job ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsOutputsShow200Response**](../Model/OrganizationsServersScheduledJobsOutputsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersScheduledJobsShow()`

```php
organizationsServersScheduledJobsShow($organization, $server, $job): \Dimer47\Model\OrganizationsServersScheduledJobsStore202Response
```

Get scheduled job

Show a specific scheduled job.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$job = 56; // int | The job ID

try {
    $result = $apiInstance->organizationsServersScheduledJobsShow($organization, $server, $job);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersScheduledJobsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **job** | **int**| The job ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsStore202Response**](../Model/OrganizationsServersScheduledJobsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersScheduledJobsStore()`

```php
organizationsServersScheduledJobsStore($organization, $server, $create_scheduled_job_request): \Dimer47\Model\OrganizationsServersScheduledJobsStore202Response
```

Create scheduled job

Create a specific scheduled job.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_scheduled_job_request = new \Dimer47\Model\CreateScheduledJobRequest(); // \Dimer47\Model\CreateScheduledJobRequest

try {
    $result = $apiInstance->organizationsServersScheduledJobsStore($organization, $server, $create_scheduled_job_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersScheduledJobsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_scheduled_job_request** | [**\Dimer47\Model\CreateScheduledJobRequest**](../Model/CreateScheduledJobRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsStore202Response**](../Model/OrganizationsServersScheduledJobsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesScheduledJobsDestroy()`

```php
organizationsServersSitesScheduledJobsDestroy($organization, $server, $site, $job)
```

Delete site scheduled job

Delete a specific scheduled job associated with the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$job = 56; // int | The job ID

try {
    $apiInstance->organizationsServersSitesScheduledJobsDestroy($organization, $server, $site, $job);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersSitesScheduledJobsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **job** | **int**| The job ID | |

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

## `organizationsServersSitesScheduledJobsIndex()`

```php
organizationsServersSitesScheduledJobsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_status, $filter_user): \Dimer47\Model\OrganizationsServersScheduledJobsIndex200Response
```

List site scheduled jobs

List all scheduled jobs associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `created_at`, `updated_at`, `status`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_status = 'filter_status_example'; // string
$filter_user = 'filter_user_example'; // string

try {
    $result = $apiInstance->organizationsServersSitesScheduledJobsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_status, $filter_user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersSitesScheduledJobsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;, &#x60;updated_at&#x60;, &#x60;status&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_status** | **string**|  | [optional] |
| **filter_user** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsIndex200Response**](../Model/OrganizationsServersScheduledJobsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesScheduledJobsOutputsShow()`

```php
organizationsServersSitesScheduledJobsOutputsShow($organization, $server, $site, $job): \Dimer47\Model\OrganizationsServersScheduledJobsOutputsShow200Response
```

Get site scheduled job output

Show a specific scheduled job output associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$job = 56; // int | The job ID

try {
    $result = $apiInstance->organizationsServersSitesScheduledJobsOutputsShow($organization, $server, $site, $job);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersSitesScheduledJobsOutputsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **job** | **int**| The job ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsOutputsShow200Response**](../Model/OrganizationsServersScheduledJobsOutputsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesScheduledJobsShow()`

```php
organizationsServersSitesScheduledJobsShow($organization, $server, $site, $job): \Dimer47\Model\OrganizationsServersScheduledJobsStore202Response
```

Get site scheduled job

Show a specific scheduled job.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$job = 56; // int | The job ID

try {
    $result = $apiInstance->organizationsServersSitesScheduledJobsShow($organization, $server, $site, $job);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersSitesScheduledJobsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **job** | **int**| The job ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsStore202Response**](../Model/OrganizationsServersScheduledJobsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesScheduledJobsStore()`

```php
organizationsServersSitesScheduledJobsStore($organization, $server, $site, $create_scheduled_job_request): \Dimer47\Model\OrganizationsServersScheduledJobsStore202Response
```

Create site scheduled job

Create a specific scheduled job for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ScheduledJobsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_scheduled_job_request = new \Dimer47\Model\CreateScheduledJobRequest(); // \Dimer47\Model\CreateScheduledJobRequest

try {
    $result = $apiInstance->organizationsServersSitesScheduledJobsStore($organization, $server, $site, $create_scheduled_job_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ScheduledJobsApi->organizationsServersSitesScheduledJobsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_scheduled_job_request** | [**\Dimer47\Model\CreateScheduledJobRequest**](../Model/CreateScheduledJobRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersScheduledJobsStore202Response**](../Model/OrganizationsServersScheduledJobsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
