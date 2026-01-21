# Dimer47\DeploymentsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersSitesDeploymentsDeployHookShow()**](DeploymentsApi.md#organizationsServersSitesDeploymentsDeployHookShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/deploy-hook | Get the deployment trigger URL |
| [**organizationsServersSitesDeploymentsDeployHookUpdate()**](DeploymentsApi.md#organizationsServersSitesDeploymentsDeployHookUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/deployments/deploy-hook | Update deployment trigger URL |
| [**organizationsServersSitesDeploymentsIndex()**](DeploymentsApi.md#organizationsServersSitesDeploymentsIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments | List deployments |
| [**organizationsServersSitesDeploymentsLogShow()**](DeploymentsApi.md#organizationsServersSitesDeploymentsLogShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/{deployment}/log | Get deployment output |
| [**organizationsServersSitesDeploymentsPushToDeployDestroy()**](DeploymentsApi.md#organizationsServersSitesDeploymentsPushToDeployDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/deployments/push-to-deploy | Delete push to deploy configuration |
| [**organizationsServersSitesDeploymentsPushToDeployStore()**](DeploymentsApi.md#organizationsServersSitesDeploymentsPushToDeployStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/deployments/push-to-deploy | Create push to deploy configuration |
| [**organizationsServersSitesDeploymentsScriptShow()**](DeploymentsApi.md#organizationsServersSitesDeploymentsScriptShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/script | Get deployment script |
| [**organizationsServersSitesDeploymentsScriptUpdate()**](DeploymentsApi.md#organizationsServersSitesDeploymentsScriptUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/deployments/script | Update deployment script |
| [**organizationsServersSitesDeploymentsShow()**](DeploymentsApi.md#organizationsServersSitesDeploymentsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/{deployment} | Get deployment |
| [**organizationsServersSitesDeploymentsStatusDestroy()**](DeploymentsApi.md#organizationsServersSitesDeploymentsStatusDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/deployments/status | Update deployment state |
| [**organizationsServersSitesDeploymentsStatusShow()**](DeploymentsApi.md#organizationsServersSitesDeploymentsStatusShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/status | Get deployment status |
| [**organizationsServersSitesDeploymentsStore()**](DeploymentsApi.md#organizationsServersSitesDeploymentsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/deployments | Create deployment |
| [**organizationsServersSitesWebhooksDestroy()**](DeploymentsApi.md#organizationsServersSitesWebhooksDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/webhooks/{deploymentWebhook} | Delete site webhook |
| [**organizationsServersSitesWebhooksIndex()**](DeploymentsApi.md#organizationsServersSitesWebhooksIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/webhooks | List site webhooks |
| [**organizationsServersSitesWebhooksShow()**](DeploymentsApi.md#organizationsServersSitesWebhooksShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/webhooks/{deploymentWebhook} | Get site webhook |
| [**organizationsServersSitesWebhooksStore()**](DeploymentsApi.md#organizationsServersSitesWebhooksStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/webhooks | Create site webhook |


## `organizationsServersSitesDeploymentsDeployHookShow()`

```php
organizationsServersSitesDeploymentsDeployHookShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesDeploymentsDeployHookShow200Response
```

Get the deployment trigger URL

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsDeployHookShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsDeployHookShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsDeployHookShow200Response**](../Model/OrganizationsServersSitesDeploymentsDeployHookShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsDeployHookUpdate()`

```php
organizationsServersSitesDeploymentsDeployHookUpdate($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesDeploymentsDeployHookShow200Response
```

Update deployment trigger URL

Regenerate the deployment hook token used for triggering deployment on the deployment URL.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsDeployHookUpdate($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsDeployHookUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsDeployHookShow200Response**](../Model/OrganizationsServersSitesDeploymentsDeployHookShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsIndex()`

```php
organizationsServersSitesDeploymentsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_commit_hash, $filter_commit_message, $filter_commit_author): \Dimer47\Model\OrganizationsServersSitesDeploymentsIndex200Response
```

List deployments

Show all recent deployments for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `created_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-created_at`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_commit_hash = 'filter_commit_hash_example'; // string | The commit hash of the deployment.
$filter_commit_message = 'filter_commit_message_example'; // string | The commit message of the deployment.
$filter_commit_author = 'filter_commit_author_example'; // string | The commit author of the deployment.

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_commit_hash, $filter_commit_message, $filter_commit_author);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;created_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-created_at&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_commit_hash** | **string**| The commit hash of the deployment. | [optional] |
| **filter_commit_message** | **string**| The commit message of the deployment. | [optional] |
| **filter_commit_author** | **string**| The commit author of the deployment. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsIndex200Response**](../Model/OrganizationsServersSitesDeploymentsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsLogShow()`

```php
organizationsServersSitesDeploymentsLogShow($organization, $server, $site, $deployment): \Dimer47\Model\OrganizationsServersSitesDeploymentsLogShow200Response
```

Get deployment output

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$deployment = 56; // int | The deployment ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsLogShow($organization, $server, $site, $deployment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsLogShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **deployment** | **int**| The deployment ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsLogShow200Response**](../Model/OrganizationsServersSitesDeploymentsLogShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsPushToDeployDestroy()`

```php
organizationsServersSitesDeploymentsPushToDeployDestroy($organization, $server, $site)
```

Delete push to deploy configuration

Disable push to deploy for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesDeploymentsPushToDeployDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsPushToDeployDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

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

## `organizationsServersSitesDeploymentsPushToDeployStore()`

```php
organizationsServersSitesDeploymentsPushToDeployStore($organization, $server, $site)
```

Create push to deploy configuration

Enable push to deploy for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesDeploymentsPushToDeployStore($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsPushToDeployStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

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

## `organizationsServersSitesDeploymentsScriptShow()`

```php
organizationsServersSitesDeploymentsScriptShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesDeploymentsScriptShow200Response
```

Get deployment script

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsScriptShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsScriptShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsScriptShow200Response**](../Model/OrganizationsServersSitesDeploymentsScriptShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsScriptUpdate()`

```php
organizationsServersSitesDeploymentsScriptUpdate($organization, $server, $site, $update_deployment_script_request): \Dimer47\Model\OrganizationsServersSitesDeploymentsScriptShow200Response
```

Update deployment script

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$update_deployment_script_request = new \Dimer47\Model\UpdateDeploymentScriptRequest(); // \Dimer47\Model\UpdateDeploymentScriptRequest

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsScriptUpdate($organization, $server, $site, $update_deployment_script_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsScriptUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **update_deployment_script_request** | [**\Dimer47\Model\UpdateDeploymentScriptRequest**](../Model/UpdateDeploymentScriptRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsScriptShow200Response**](../Model/OrganizationsServersSitesDeploymentsScriptShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsShow()`

```php
organizationsServersSitesDeploymentsShow($organization, $server, $site, $deployment): \Dimer47\Model\OrganizationsServersSitesDeploymentsStore202Response
```

Get deployment

Show a specific deployment.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$deployment = 56; // int | The deployment ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsShow($organization, $server, $site, $deployment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **deployment** | **int**| The deployment ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsStore202Response**](../Model/OrganizationsServersSitesDeploymentsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsStatusDestroy()`

```php
organizationsServersSitesDeploymentsStatusDestroy($organization, $server, $site)
```

Update deployment state

Reset the deployment state for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesDeploymentsStatusDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsStatusDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

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

## `organizationsServersSitesDeploymentsStatusShow()`

```php
organizationsServersSitesDeploymentsStatusShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesDeploymentsStatusShow200Response
```

Get deployment status

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsStatusShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsStatusShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsStatusShow200Response**](../Model/OrganizationsServersSitesDeploymentsStatusShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDeploymentsStore()`

```php
organizationsServersSitesDeploymentsStore($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesDeploymentsStore202Response
```

Create deployment

Trigger a new deployment for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesDeploymentsStore($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesDeploymentsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDeploymentsStore202Response**](../Model/OrganizationsServersSitesDeploymentsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesWebhooksDestroy()`

```php
organizationsServersSitesWebhooksDestroy($organization, $server, $site, $deployment_webhook)
```

Delete site webhook

Delete a specific webhook from the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$deployment_webhook = 56; // int | The deployment webhook ID

try {
    $apiInstance->organizationsServersSitesWebhooksDestroy($organization, $server, $site, $deployment_webhook);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesWebhooksDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **deployment_webhook** | **int**| The deployment webhook ID | |

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

## `organizationsServersSitesWebhooksIndex()`

```php
organizationsServersSitesWebhooksIndex($organization, $server, $site, $sort, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServersSitesWebhooksIndex200Response
```

List site webhooks

List all webhooks for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
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

try {
    $result = $apiInstance->organizationsServersSitesWebhooksIndex($organization, $server, $site, $sort, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesWebhooksIndex: ', $e->getMessage(), PHP_EOL;
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

### Return type

[**\Dimer47\Model\OrganizationsServersSitesWebhooksIndex200Response**](../Model/OrganizationsServersSitesWebhooksIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesWebhooksShow()`

```php
organizationsServersSitesWebhooksShow($organization, $server, $site, $deployment_webhook): \Dimer47\Model\OrganizationsServersSitesWebhooksShow200Response
```

Get site webhook

Get a specific webhook associated with the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$deployment_webhook = 56; // int | The deployment webhook ID

try {
    $result = $apiInstance->organizationsServersSitesWebhooksShow($organization, $server, $site, $deployment_webhook);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesWebhooksShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **deployment_webhook** | **int**| The deployment webhook ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesWebhooksShow200Response**](../Model/OrganizationsServersSitesWebhooksShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesWebhooksStore()`

```php
organizationsServersSitesWebhooksStore($organization, $server, $site, $create_deployment_webhook_request)
```

Create site webhook

Create a new webhook for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\DeploymentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_deployment_webhook_request = new \Dimer47\Model\CreateDeploymentWebhookRequest(); // \Dimer47\Model\CreateDeploymentWebhookRequest

try {
    $apiInstance->organizationsServersSitesWebhooksStore($organization, $server, $site, $create_deployment_webhook_request);
} catch (Exception $e) {
    echo 'Exception when calling DeploymentsApi->organizationsServersSitesWebhooksStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_deployment_webhook_request** | [**\Dimer47\Model\CreateDeploymentWebhookRequest**](../Model/CreateDeploymentWebhookRequest.md)|  | |

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
