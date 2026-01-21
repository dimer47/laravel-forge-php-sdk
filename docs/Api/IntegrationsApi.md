# Dimer47\IntegrationsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersSitesIntegrationsHorizonDestroy()**](IntegrationsApi.md#organizationsServersSitesIntegrationsHorizonDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/horizon | Delete Laravel Horizon integration |
| [**organizationsServersSitesIntegrationsHorizonShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsHorizonShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/horizon | Get Laravel Horizon integration status |
| [**organizationsServersSitesIntegrationsHorizonStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsHorizonStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/horizon | Create Laravel Horizon integration |
| [**organizationsServersSitesIntegrationsInertiaShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsInertiaShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/inertia | Get Inertia integration status |
| [**organizationsServersSitesIntegrationsInertiaStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsInertiaStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/inertia | Create Inertia integration |
| [**organizationsServersSitesIntegrationsLaravelMaintenanceDestroy()**](IntegrationsApi.md#organizationsServersSitesIntegrationsLaravelMaintenanceDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-maintenance | Delete Laravel Maintenance integration |
| [**organizationsServersSitesIntegrationsLaravelMaintenanceShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsLaravelMaintenanceShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-maintenance | Get Laravel Maintenance integration status |
| [**organizationsServersSitesIntegrationsLaravelMaintenanceStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsLaravelMaintenanceStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-maintenance | Create Laravel Maintenance integration |
| [**organizationsServersSitesIntegrationsLaravelSchedulerDestroy()**](IntegrationsApi.md#organizationsServersSitesIntegrationsLaravelSchedulerDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-scheduler | Delete Laravel Scheduler integration job |
| [**organizationsServersSitesIntegrationsLaravelSchedulerShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsLaravelSchedulerShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-scheduler | Get Laravel Scheduler integration job |
| [**organizationsServersSitesIntegrationsLaravelSchedulerStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsLaravelSchedulerStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-scheduler | Create Laravel Scheduler integration job |
| [**organizationsServersSitesIntegrationsOctaneDestroy()**](IntegrationsApi.md#organizationsServersSitesIntegrationsOctaneDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/octane | Delete Laravel Octane integration |
| [**organizationsServersSitesIntegrationsOctaneShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsOctaneShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/octane | Get Laravel Octane integration status |
| [**organizationsServersSitesIntegrationsOctaneStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsOctaneStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/octane | Create Laravel Octane integration |
| [**organizationsServersSitesIntegrationsPulseDestroy()**](IntegrationsApi.md#organizationsServersSitesIntegrationsPulseDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/pulse | Delete Laravel Pulse integration |
| [**organizationsServersSitesIntegrationsPulseShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsPulseShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/pulse | Get Laravel Pulse integration status |
| [**organizationsServersSitesIntegrationsPulseStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsPulseStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/pulse | Create Laravel Pulse integration |
| [**organizationsServersSitesIntegrationsReverbDestroy()**](IntegrationsApi.md#organizationsServersSitesIntegrationsReverbDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/reverb | Delete Laravel Reverb integration |
| [**organizationsServersSitesIntegrationsReverbShow()**](IntegrationsApi.md#organizationsServersSitesIntegrationsReverbShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/reverb | Get Laravel Reverb integration status |
| [**organizationsServersSitesIntegrationsReverbStore()**](IntegrationsApi.md#organizationsServersSitesIntegrationsReverbStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/reverb | Create Laravel Reverb integration |


## `organizationsServersSitesIntegrationsHorizonDestroy()`

```php
organizationsServersSitesIntegrationsHorizonDestroy($organization, $server, $site)
```

Delete Laravel Horizon integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesIntegrationsHorizonDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsHorizonDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesIntegrationsHorizonShow()`

```php
organizationsServersSitesIntegrationsHorizonShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsHorizonShow200Response
```

Get Laravel Horizon integration status

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsHorizonShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsHorizonShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsHorizonShow200Response**](../Model/OrganizationsServersSitesIntegrationsHorizonShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsHorizonStore()`

```php
organizationsServersSitesIntegrationsHorizonStore($organization, $server, $site): object
```

Create Laravel Horizon integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsHorizonStore($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsHorizonStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsInertiaShow()`

```php
organizationsServersSitesIntegrationsInertiaShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsInertiaShow200Response
```

Get Inertia integration status

Show whether Inertia SSR integration is enabled.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsInertiaShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsInertiaShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsInertiaShow200Response**](../Model/OrganizationsServersSitesIntegrationsInertiaShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsInertiaStore()`

```php
organizationsServersSitesIntegrationsInertiaStore($organization, $server, $site): object
```

Create Inertia integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsInertiaStore($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsInertiaStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsLaravelMaintenanceDestroy()`

```php
organizationsServersSitesIntegrationsLaravelMaintenanceDestroy($organization, $server, $site)
```

Delete Laravel Maintenance integration

Disable maintenance mode for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesIntegrationsLaravelMaintenanceDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsLaravelMaintenanceDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesIntegrationsLaravelMaintenanceShow()`

```php
organizationsServersSitesIntegrationsLaravelMaintenanceShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsLaravelMaintenanceShow200Response
```

Get Laravel Maintenance integration status

Show whether Laravel Maintenance integration is enabled.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsLaravelMaintenanceShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsLaravelMaintenanceShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsLaravelMaintenanceShow200Response**](../Model/OrganizationsServersSitesIntegrationsLaravelMaintenanceShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsLaravelMaintenanceStore()`

```php
organizationsServersSitesIntegrationsLaravelMaintenanceStore($organization, $server, $site, $enable_maintenance_mode_request)
```

Create Laravel Maintenance integration

Enable maintenance mode for the site.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$enable_maintenance_mode_request = new \Dimer47\Model\EnableMaintenanceModeRequest(); // \Dimer47\Model\EnableMaintenanceModeRequest

try {
    $apiInstance->organizationsServersSitesIntegrationsLaravelMaintenanceStore($organization, $server, $site, $enable_maintenance_mode_request);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsLaravelMaintenanceStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **enable_maintenance_mode_request** | [**\Dimer47\Model\EnableMaintenanceModeRequest**](../Model/EnableMaintenanceModeRequest.md)|  | |

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

## `organizationsServersSitesIntegrationsLaravelSchedulerDestroy()`

```php
organizationsServersSitesIntegrationsLaravelSchedulerDestroy($organization, $server, $site)
```

Delete Laravel Scheduler integration job

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesIntegrationsLaravelSchedulerDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsLaravelSchedulerDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesIntegrationsLaravelSchedulerShow()`

```php
organizationsServersSitesIntegrationsLaravelSchedulerShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsLaravelSchedulerShow200Response
```

Get Laravel Scheduler integration job

Show whether Laravel Scheduler integration is enabled.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsLaravelSchedulerShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsLaravelSchedulerShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsLaravelSchedulerShow200Response**](../Model/OrganizationsServersSitesIntegrationsLaravelSchedulerShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsLaravelSchedulerStore()`

```php
organizationsServersSitesIntegrationsLaravelSchedulerStore($organization, $server, $site): object
```

Create Laravel Scheduler integration job

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsLaravelSchedulerStore($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsLaravelSchedulerStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsOctaneDestroy()`

```php
organizationsServersSitesIntegrationsOctaneDestroy($organization, $server, $site)
```

Delete Laravel Octane integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesIntegrationsOctaneDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsOctaneDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesIntegrationsOctaneShow()`

```php
organizationsServersSitesIntegrationsOctaneShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsOctaneShow200Response
```

Get Laravel Octane integration status

Show whether Laravel Octane integration is enabled.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsOctaneShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsOctaneShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsOctaneShow200Response**](../Model/OrganizationsServersSitesIntegrationsOctaneShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsOctaneStore()`

```php
organizationsServersSitesIntegrationsOctaneStore($organization, $server, $site, $enable_octane_request): object
```

Create Laravel Octane integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$enable_octane_request = new \Dimer47\Model\EnableOctaneRequest(); // \Dimer47\Model\EnableOctaneRequest

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsOctaneStore($organization, $server, $site, $enable_octane_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsOctaneStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **enable_octane_request** | [**\Dimer47\Model\EnableOctaneRequest**](../Model/EnableOctaneRequest.md)|  | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsPulseDestroy()`

```php
organizationsServersSitesIntegrationsPulseDestroy($organization, $server, $site)
```

Delete Laravel Pulse integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesIntegrationsPulseDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsPulseDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesIntegrationsPulseShow()`

```php
organizationsServersSitesIntegrationsPulseShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsPulseShow200Response
```

Get Laravel Pulse integration status

Show whether Laravel Pulse integration is enabled.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsPulseShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsPulseShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsPulseShow200Response**](../Model/OrganizationsServersSitesIntegrationsPulseShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsPulseStore()`

```php
organizationsServersSitesIntegrationsPulseStore($organization, $server, $site): object
```

Create Laravel Pulse integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsPulseStore($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsPulseStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsReverbDestroy()`

```php
organizationsServersSitesIntegrationsReverbDestroy($organization, $server, $site)
```

Delete Laravel Reverb integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesIntegrationsReverbDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsReverbDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesIntegrationsReverbShow()`

```php
organizationsServersSitesIntegrationsReverbShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesIntegrationsReverbShow200Response
```

Get Laravel Reverb integration status

Show whether Laravel Reverb integration is enabled.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsReverbShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsReverbShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesIntegrationsReverbShow200Response**](../Model/OrganizationsServersSitesIntegrationsReverbShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIntegrationsReverbStore()`

```php
organizationsServersSitesIntegrationsReverbStore($organization, $server, $site, $enable_reverb_request): object
```

Create Laravel Reverb integration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\IntegrationsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$enable_reverb_request = new \Dimer47\Model\EnableReverbRequest(); // \Dimer47\Model\EnableReverbRequest

try {
    $result = $apiInstance->organizationsServersSitesIntegrationsReverbStore($organization, $server, $site, $enable_reverb_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling IntegrationsApi->organizationsServersSitesIntegrationsReverbStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **enable_reverb_request** | [**\Dimer47\Model\EnableReverbRequest**](../Model/EnableReverbRequest.md)|  | |

### Return type

**object**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
