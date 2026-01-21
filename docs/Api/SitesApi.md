# Dimer47\SitesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsServersSitesComposerCredentialsDestroy()**](SitesApi.md#organizationsServersSitesComposerCredentialsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/composer/credentials/{repository} | Delete composer credentials for the site |
| [**organizationsServersSitesComposerCredentialsIndex()**](SitesApi.md#organizationsServersSitesComposerCredentialsIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/composer/credentials | Get composer credentials for the site |
| [**organizationsServersSitesComposerCredentialsShow()**](SitesApi.md#organizationsServersSitesComposerCredentialsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/composer/credentials/{repository} | Get composer credential for the site |
| [**organizationsServersSitesComposerCredentialsStore()**](SitesApi.md#organizationsServersSitesComposerCredentialsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/composer/credentials | Create composer credentials for the site |
| [**organizationsServersSitesComposerCredentialsUpdate()**](SitesApi.md#organizationsServersSitesComposerCredentialsUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/composer/credentials/{repository} | Update composer credentials for the site |
| [**organizationsServersSitesDestroy()**](SitesApi.md#organizationsServersSitesDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site} | Delete site |
| [**organizationsServersSitesDomainsActionsStore()**](SitesApi.md#organizationsServersSitesDomainsActionsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/actions | Create domain action |
| [**organizationsServersSitesDomainsCertificateActionsStore()**](SitesApi.md#organizationsServersSitesDomainsCertificateActionsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/certificate/actions | Create domain certificate action |
| [**organizationsServersSitesDomainsCertificateDestroy()**](SitesApi.md#organizationsServersSitesDomainsCertificateDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/certificate | Delete domain certificate |
| [**organizationsServersSitesDomainsCertificateShow()**](SitesApi.md#organizationsServersSitesDomainsCertificateShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/certificate | Get domain certificate |
| [**organizationsServersSitesDomainsCertificateStore()**](SitesApi.md#organizationsServersSitesDomainsCertificateStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/certificate | Create domain certificate |
| [**organizationsServersSitesDomainsConfigurations()**](SitesApi.md#organizationsServersSitesDomainsConfigurations) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/configurations | Get domain DNS configuration |
| [**organizationsServersSitesDomainsDestroy()**](SitesApi.md#organizationsServersSitesDomainsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord} | Delete domain |
| [**organizationsServersSitesDomainsIndex()**](SitesApi.md#organizationsServersSitesDomainsIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/domains | List domains |
| [**organizationsServersSitesDomainsNginxShow()**](SitesApi.md#organizationsServersSitesDomainsNginxShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/nginx | Get domain Nginx configuration |
| [**organizationsServersSitesDomainsNginxUpdate()**](SitesApi.md#organizationsServersSitesDomainsNginxUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord}/nginx | Update domain Nginx configuration |
| [**organizationsServersSitesDomainsShow()**](SitesApi.md#organizationsServersSitesDomainsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord} | Get domain |
| [**organizationsServersSitesDomainsStore()**](SitesApi.md#organizationsServersSitesDomainsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/domains | Create domain |
| [**organizationsServersSitesDomainsUpdate()**](SitesApi.md#organizationsServersSitesDomainsUpdate) | **PATCH** /orgs/{organization}/servers/{server}/sites/{site}/domains/{domainRecord} | Update domain |
| [**organizationsServersSitesEnvironmentShow()**](SitesApi.md#organizationsServersSitesEnvironmentShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/environment | Get .env content |
| [**organizationsServersSitesEnvironmentUpdate()**](SitesApi.md#organizationsServersSitesEnvironmentUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/environment | Update .env content |
| [**organizationsServersSitesHealthcheckShow()**](SitesApi.md#organizationsServersSitesHealthcheckShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/healthcheck | Get healthcheck endpoint |
| [**organizationsServersSitesHealthcheckUpdate()**](SitesApi.md#organizationsServersSitesHealthcheckUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/healthcheck | Update healthcheck endpoint |
| [**organizationsServersSitesHeartbeatsDestroy()**](SitesApi.md#organizationsServersSitesHeartbeatsDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/heartbeats/{heartbeat} | Delete heartbeat |
| [**organizationsServersSitesHeartbeatsIndex()**](SitesApi.md#organizationsServersSitesHeartbeatsIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/heartbeats | List heartbeats |
| [**organizationsServersSitesHeartbeatsShow()**](SitesApi.md#organizationsServersSitesHeartbeatsShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/heartbeats/{heartbeat} | Get heartbeat |
| [**organizationsServersSitesHeartbeatsStore()**](SitesApi.md#organizationsServersSitesHeartbeatsStore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/heartbeats | Create heartbeat |
| [**organizationsServersSitesHeartbeatsUpdate()**](SitesApi.md#organizationsServersSitesHeartbeatsUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/heartbeats/{heartbeat} | Update heartbeat |
| [**organizationsServersSitesIndex()**](SitesApi.md#organizationsServersSitesIndex) | **GET** /orgs/{organization}/servers/{server}/sites | List sites for server |
| [**organizationsServersSitesLoadBalancingNodesIndex()**](SitesApi.md#organizationsServersSitesLoadBalancingNodesIndex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/load-balancing-nodes | List load balancing nodes |
| [**organizationsServersSitesLoadBalancingNodesUpdate()**](SitesApi.md#organizationsServersSitesLoadBalancingNodesUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/load-balancing-nodes | Update load balancing nodes |
| [**organizationsServersSitesLogsApplicationDestroy()**](SitesApi.md#organizationsServersSitesLogsApplicationDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/logs/application | Delete site log content |
| [**organizationsServersSitesLogsApplicationShow()**](SitesApi.md#organizationsServersSitesLogsApplicationShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/logs/application | Get site log content |
| [**organizationsServersSitesLogsNginxAccessDestroy()**](SitesApi.md#organizationsServersSitesLogsNginxAccessDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/logs/nginx-access | Delete Nginx access log content |
| [**organizationsServersSitesLogsNginxAccessShow()**](SitesApi.md#organizationsServersSitesLogsNginxAccessShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/logs/nginx-access | Get Nginx access log content |
| [**organizationsServersSitesLogsNginxErrorDestroy()**](SitesApi.md#organizationsServersSitesLogsNginxErrorDestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/logs/nginx-error | Delete Nginx error log content |
| [**organizationsServersSitesLogsNginxErrorShow()**](SitesApi.md#organizationsServersSitesLogsNginxErrorShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/logs/nginx-error | Get Nginx error log content |
| [**organizationsServersSitesNginxShow()**](SitesApi.md#organizationsServersSitesNginxShow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/nginx | Get Nginx configuration |
| [**organizationsServersSitesNginxUpdate()**](SitesApi.md#organizationsServersSitesNginxUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/nginx | Update Nginx configuration |
| [**organizationsServersSitesStore()**](SitesApi.md#organizationsServersSitesStore) | **POST** /orgs/{organization}/servers/{server}/sites | Create site |
| [**organizationsServersSitesUpdate()**](SitesApi.md#organizationsServersSitesUpdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site} | Update site |
| [**organizationsSitesIndex()**](SitesApi.md#organizationsSitesIndex) | **GET** /orgs/{organization}/sites | List sites for Organization |
| [**organizationsSitesShow()**](SitesApi.md#organizationsSitesShow) | **GET** /orgs/{organization}/sites/{site} | Get site |
| [**sitesIndex()**](SitesApi.md#sitesIndex) | **GET** /sites | List sites |


## `organizationsServersSitesComposerCredentialsDestroy()`

```php
organizationsServersSitesComposerCredentialsDestroy($organization, $server, $site, $repository)
```

Delete composer credentials for the site

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$repository = 'repository_example'; // string

try {
    $apiInstance->organizationsServersSitesComposerCredentialsDestroy($organization, $server, $site, $repository);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesComposerCredentialsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **repository** | **string**|  | |

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

## `organizationsServersSitesComposerCredentialsIndex()`

```php
organizationsServersSitesComposerCredentialsIndex($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesComposerCredentialsIndex200Response
```

Get composer credentials for the site

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesComposerCredentialsIndex($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesComposerCredentialsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesComposerCredentialsIndex200Response**](../Model/OrganizationsServersSitesComposerCredentialsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesComposerCredentialsShow()`

```php
organizationsServersSitesComposerCredentialsShow($organization, $server, $site, $repository): \Dimer47\Model\OrganizationsServersSitesComposerCredentialsShow200Response
```

Get composer credential for the site

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$repository = 'repository_example'; // string

try {
    $result = $apiInstance->organizationsServersSitesComposerCredentialsShow($organization, $server, $site, $repository);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesComposerCredentialsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **repository** | **string**|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesComposerCredentialsShow200Response**](../Model/OrganizationsServersSitesComposerCredentialsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesComposerCredentialsStore()`

```php
organizationsServersSitesComposerCredentialsStore($organization, $server, $site, $create_composer_credential_request)
```

Create composer credentials for the site

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_composer_credential_request = new \Dimer47\Model\CreateComposerCredentialRequest(); // \Dimer47\Model\CreateComposerCredentialRequest

try {
    $apiInstance->organizationsServersSitesComposerCredentialsStore($organization, $server, $site, $create_composer_credential_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesComposerCredentialsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_composer_credential_request** | [**\Dimer47\Model\CreateComposerCredentialRequest**](../Model/CreateComposerCredentialRequest.md)|  | |

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

## `organizationsServersSitesComposerCredentialsUpdate()`

```php
organizationsServersSitesComposerCredentialsUpdate($organization, $server, $site, $repository, $update_composer_credential_request)
```

Update composer credentials for the site

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$repository = 'repository_example'; // string
$update_composer_credential_request = new \Dimer47\Model\UpdateComposerCredentialRequest(); // \Dimer47\Model\UpdateComposerCredentialRequest

try {
    $apiInstance->organizationsServersSitesComposerCredentialsUpdate($organization, $server, $site, $repository, $update_composer_credential_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesComposerCredentialsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **repository** | **string**|  | |
| **update_composer_credential_request** | [**\Dimer47\Model\UpdateComposerCredentialRequest**](../Model/UpdateComposerCredentialRequest.md)|  | |

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

## `organizationsServersSitesDestroy()`

```php
organizationsServersSitesDestroy($organization, $server, $site)
```

Delete site

Remove a site from the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesDomainsActionsStore()`

```php
organizationsServersSitesDomainsActionsStore($organization, $server, $site, $domain_record, $domain_action_request)
```

Create domain action

Run an action on a domain, defined by the action type parameter.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID
$domain_action_request = new \Dimer47\Model\DomainActionRequest(); // \Dimer47\Model\DomainActionRequest

try {
    $apiInstance->organizationsServersSitesDomainsActionsStore($organization, $server, $site, $domain_record, $domain_action_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |
| **domain_action_request** | [**\Dimer47\Model\DomainActionRequest**](../Model/DomainActionRequest.md)|  | |

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

## `organizationsServersSitesDomainsCertificateActionsStore()`

```php
organizationsServersSitesDomainsCertificateActionsStore($organization, $server, $site, $domain_record, $domain_certificate_action_request)
```

Create domain certificate action

Run an action on a domain certificate, defined by the action type parameter.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID
$domain_certificate_action_request = new \Dimer47\Model\DomainCertificateActionRequest(); // \Dimer47\Model\DomainCertificateActionRequest

try {
    $apiInstance->organizationsServersSitesDomainsCertificateActionsStore($organization, $server, $site, $domain_record, $domain_certificate_action_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsCertificateActionsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |
| **domain_certificate_action_request** | [**\Dimer47\Model\DomainCertificateActionRequest**](../Model/DomainCertificateActionRequest.md)|  | |

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

## `organizationsServersSitesDomainsCertificateDestroy()`

```php
organizationsServersSitesDomainsCertificateDestroy($organization, $server, $site, $domain_record)
```

Delete domain certificate

Delete the certificate for a given domain.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID

try {
    $apiInstance->organizationsServersSitesDomainsCertificateDestroy($organization, $server, $site, $domain_record);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsCertificateDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |

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

## `organizationsServersSitesDomainsCertificateShow()`

```php
organizationsServersSitesDomainsCertificateShow($organization, $server, $site, $domain_record): \Dimer47\Model\OrganizationsServersSitesDomainsCertificateShow200Response
```

Get domain certificate

Get the certificate for a given domain.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID

try {
    $result = $apiInstance->organizationsServersSitesDomainsCertificateShow($organization, $server, $site, $domain_record);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsCertificateShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsCertificateShow200Response**](../Model/OrganizationsServersSitesDomainsCertificateShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsCertificateStore()`

```php
organizationsServersSitesDomainsCertificateStore($organization, $server, $site, $domain_record, $create_domain_certificate_request): \Dimer47\Model\OrganizationsServersSitesDomainsCertificateShow200Response
```

Create domain certificate

Create a new certificate for a given domain.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID
$create_domain_certificate_request = new \Dimer47\Model\CreateDomainCertificateRequest(); // \Dimer47\Model\CreateDomainCertificateRequest

try {
    $result = $apiInstance->organizationsServersSitesDomainsCertificateStore($organization, $server, $site, $domain_record, $create_domain_certificate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsCertificateStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |
| **create_domain_certificate_request** | [**\Dimer47\Model\CreateDomainCertificateRequest**](../Model/CreateDomainCertificateRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsCertificateShow200Response**](../Model/OrganizationsServersSitesDomainsCertificateShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsConfigurations()`

```php
organizationsServersSitesDomainsConfigurations($organization, $server, $site, $domain_record): \Dimer47\Model\OrganizationsServersSitesDomainsConfigurations200Response
```

Get domain DNS configuration

Show the DNS configuration instructions for a domain.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID

try {
    $result = $apiInstance->organizationsServersSitesDomainsConfigurations($organization, $server, $site, $domain_record);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsConfigurations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsConfigurations200Response**](../Model/OrganizationsServersSitesDomainsConfigurations200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsDestroy()`

```php
organizationsServersSitesDomainsDestroy($organization, $server, $site, $domain_record)
```

Delete domain

Remove a domain from the site  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID

try {
    $apiInstance->organizationsServersSitesDomainsDestroy($organization, $server, $site, $domain_record);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |

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

## `organizationsServersSitesDomainsIndex()`

```php
organizationsServersSitesDomainsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_status, $filter_type): \Dimer47\Model\OrganizationsServersSitesDomainsIndex200Response
```

List domains

Show all domains for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `name`, `created_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-name`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_status = new \Dimer47\Model\\Dimer47ModelDomainRecordStatus(); // \Dimer47ModelDomainRecordStatus | The status of the domain.
$filter_type = 'filter_type_example'; // string | The type of domain.

try {
    $result = $apiInstance->organizationsServersSitesDomainsIndex($organization, $server, $site, $sort, $page_size, $page_cursor, $filter_status, $filter_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;name&#x60;, &#x60;created_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-name&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_status** | [**\Dimer47ModelDomainRecordStatus**](../Model/.md)| The status of the domain. | [optional] |
| **filter_type** | **string**| The type of domain. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsIndex200Response**](../Model/OrganizationsServersSitesDomainsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsNginxShow()`

```php
organizationsServersSitesDomainsNginxShow($organization, $server, $site, $domain_record): \Dimer47\Model\OrganizationsServersSitesDomainsNginxShow200Response
```

Get domain Nginx configuration

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID

try {
    $result = $apiInstance->organizationsServersSitesDomainsNginxShow($organization, $server, $site, $domain_record);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsNginxShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsNginxShow200Response**](../Model/OrganizationsServersSitesDomainsNginxShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsNginxUpdate()`

```php
organizationsServersSitesDomainsNginxUpdate($organization, $server, $site, $domain_record, $update_nginx_configuration_request)
```

Update domain Nginx configuration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID
$update_nginx_configuration_request = new \Dimer47\Model\UpdateNginxConfigurationRequest(); // \Dimer47\Model\UpdateNginxConfigurationRequest

try {
    $apiInstance->organizationsServersSitesDomainsNginxUpdate($organization, $server, $site, $domain_record, $update_nginx_configuration_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsNginxUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |
| **update_nginx_configuration_request** | [**\Dimer47\Model\UpdateNginxConfigurationRequest**](../Model/UpdateNginxConfigurationRequest.md)|  | |

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

## `organizationsServersSitesDomainsShow()`

```php
organizationsServersSitesDomainsShow($organization, $server, $site, $domain_record): \Dimer47\Model\OrganizationsServersSitesDomainsStore202Response
```

Get domain

Show the specified domain for the site  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID

try {
    $result = $apiInstance->organizationsServersSitesDomainsShow($organization, $server, $site, $domain_record);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsStore202Response**](../Model/OrganizationsServersSitesDomainsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsStore()`

```php
organizationsServersSitesDomainsStore($organization, $server, $site, $create_domain_request): \Dimer47\Model\OrganizationsServersSitesDomainsStore202Response
```

Create domain

Add a new domain to the site  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_domain_request = new \Dimer47\Model\CreateDomainRequest(); // \Dimer47\Model\CreateDomainRequest

try {
    $result = $apiInstance->organizationsServersSitesDomainsStore($organization, $server, $site, $create_domain_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_domain_request** | [**\Dimer47\Model\CreateDomainRequest**](../Model/CreateDomainRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsStore202Response**](../Model/OrganizationsServersSitesDomainsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesDomainsUpdate()`

```php
organizationsServersSitesDomainsUpdate($organization, $server, $site, $domain_record, $update_domain_request): \Dimer47\Model\OrganizationsServersSitesDomainsStore202Response
```

Update domain

Update an existing domain for the site  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$domain_record = 56; // int | The domain record ID
$update_domain_request = new \Dimer47\Model\UpdateDomainRequest(); // \Dimer47\Model\UpdateDomainRequest

try {
    $result = $apiInstance->organizationsServersSitesDomainsUpdate($organization, $server, $site, $domain_record, $update_domain_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesDomainsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **domain_record** | **int**| The domain record ID | |
| **update_domain_request** | [**\Dimer47\Model\UpdateDomainRequest**](../Model/UpdateDomainRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsStore202Response**](../Model/OrganizationsServersSitesDomainsStore202Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesEnvironmentShow()`

```php
organizationsServersSitesEnvironmentShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesEnvironmentShow200Response
```

Get .env content

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesEnvironmentShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesEnvironmentShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesEnvironmentShow200Response**](../Model/OrganizationsServersSitesEnvironmentShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesEnvironmentUpdate()`

```php
organizationsServersSitesEnvironmentUpdate($organization, $server, $site, $update_environment_request)
```

Update .env content

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$update_environment_request = new \Dimer47\Model\UpdateEnvironmentRequest(); // \Dimer47\Model\UpdateEnvironmentRequest

try {
    $apiInstance->organizationsServersSitesEnvironmentUpdate($organization, $server, $site, $update_environment_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesEnvironmentUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **update_environment_request** | [**\Dimer47\Model\UpdateEnvironmentRequest**](../Model/UpdateEnvironmentRequest.md)|  | |

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

## `organizationsServersSitesHealthcheckShow()`

```php
organizationsServersSitesHealthcheckShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesHealthcheckShow200Response
```

Get healthcheck endpoint

Show the healthcheck endpoint that has been set for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesHealthcheckShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHealthcheckShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesHealthcheckShow200Response**](../Model/OrganizationsServersSitesHealthcheckShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesHealthcheckUpdate()`

```php
organizationsServersSitesHealthcheckUpdate($organization, $server, $site, $update_healthcheck_endpoint_request)
```

Update healthcheck endpoint

Update the healthcheck endpoint for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$update_healthcheck_endpoint_request = new \Dimer47\Model\UpdateHealthcheckEndpointRequest(); // \Dimer47\Model\UpdateHealthcheckEndpointRequest

try {
    $apiInstance->organizationsServersSitesHealthcheckUpdate($organization, $server, $site, $update_healthcheck_endpoint_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHealthcheckUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **update_healthcheck_endpoint_request** | [**\Dimer47\Model\UpdateHealthcheckEndpointRequest**](../Model/UpdateHealthcheckEndpointRequest.md)|  | [optional] |

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

## `organizationsServersSitesHeartbeatsDestroy()`

```php
organizationsServersSitesHeartbeatsDestroy($organization, $server, $site, $heartbeat)
```

Delete heartbeat

Delete a specific heartbeat for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$heartbeat = 56; // int | The heartbeat ID

try {
    $apiInstance->organizationsServersSitesHeartbeatsDestroy($organization, $server, $site, $heartbeat);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHeartbeatsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **heartbeat** | **int**| The heartbeat ID | |

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

## `organizationsServersSitesHeartbeatsIndex()`

```php
organizationsServersSitesHeartbeatsIndex($organization, $server, $site, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServersSitesHeartbeatsIndex200Response
```

List heartbeats

Show all heartbeats for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsServersSitesHeartbeatsIndex($organization, $server, $site, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHeartbeatsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesHeartbeatsIndex200Response**](../Model/OrganizationsServersSitesHeartbeatsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesHeartbeatsShow()`

```php
organizationsServersSitesHeartbeatsShow($organization, $server, $site, $heartbeat): \Dimer47\Model\OrganizationsServersSitesHeartbeatsStore200Response
```

Get heartbeat

Show a specific heartbeat for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$heartbeat = 56; // int | The heartbeat ID

try {
    $result = $apiInstance->organizationsServersSitesHeartbeatsShow($organization, $server, $site, $heartbeat);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHeartbeatsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **heartbeat** | **int**| The heartbeat ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesHeartbeatsStore200Response**](../Model/OrganizationsServersSitesHeartbeatsStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesHeartbeatsStore()`

```php
organizationsServersSitesHeartbeatsStore($organization, $server, $site, $create_heartbeat_request): \Dimer47\Model\OrganizationsServersSitesHeartbeatsStore200Response
```

Create heartbeat

Create a new heartbeat for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$create_heartbeat_request = new \Dimer47\Model\CreateHeartbeatRequest(); // \Dimer47\Model\CreateHeartbeatRequest

try {
    $result = $apiInstance->organizationsServersSitesHeartbeatsStore($organization, $server, $site, $create_heartbeat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHeartbeatsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **create_heartbeat_request** | [**\Dimer47\Model\CreateHeartbeatRequest**](../Model/CreateHeartbeatRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesHeartbeatsStore200Response**](../Model/OrganizationsServersSitesHeartbeatsStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesHeartbeatsUpdate()`

```php
organizationsServersSitesHeartbeatsUpdate($organization, $server, $site, $heartbeat, $update_heartbeat_request): \Dimer47\Model\OrganizationsServersSitesHeartbeatsStore200Response
```

Update heartbeat

Update a specific heartbeat for the site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$heartbeat = 56; // int | The heartbeat ID
$update_heartbeat_request = new \Dimer47\Model\UpdateHeartbeatRequest(); // \Dimer47\Model\UpdateHeartbeatRequest

try {
    $result = $apiInstance->organizationsServersSitesHeartbeatsUpdate($organization, $server, $site, $heartbeat, $update_heartbeat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesHeartbeatsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **heartbeat** | **int**| The heartbeat ID | |
| **update_heartbeat_request** | [**\Dimer47\Model\UpdateHeartbeatRequest**](../Model/UpdateHeartbeatRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesHeartbeatsStore200Response**](../Model/OrganizationsServersSitesHeartbeatsStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesIndex()`

```php
organizationsServersSitesIndex($organization, $server, $sort, $include, $page_size, $page_cursor, $filter_name): \Dimer47\Model\SitesIndex200Response
```

List sites for server

List all sites associated with the server.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$sort = 'sort_example'; // string | Available sorts are `name`, `created_at`, `updated_at`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-name`.
$include = 'include_example'; // string | Available includes are `server`, `serverCount`, `serverExists`, `tags`, `tagsCount`, `tagsExists`, `latestDeployment`, `latestDeploymentCount`, `latestDeploymentExists`, `securityRules`, `securityRulesCount`, `securityRulesExists`, `redirectRules`, `redirectRulesCount`, `redirectRulesExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string | The name of the site.

try {
    $result = $apiInstance->organizationsServersSitesIndex($organization, $server, $sort, $include, $page_size, $page_cursor, $filter_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **sort** | **string**| Available sorts are &#x60;name&#x60;, &#x60;created_at&#x60;, &#x60;updated_at&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-name&#x60;. | [optional] |
| **include** | **string**| Available includes are &#x60;server&#x60;, &#x60;serverCount&#x60;, &#x60;serverExists&#x60;, &#x60;tags&#x60;, &#x60;tagsCount&#x60;, &#x60;tagsExists&#x60;, &#x60;latestDeployment&#x60;, &#x60;latestDeploymentCount&#x60;, &#x60;latestDeploymentExists&#x60;, &#x60;securityRules&#x60;, &#x60;securityRulesCount&#x60;, &#x60;securityRulesExists&#x60;, &#x60;redirectRules&#x60;, &#x60;redirectRulesCount&#x60;, &#x60;redirectRulesExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**| The name of the site. | [optional] |

### Return type

[**\Dimer47\Model\SitesIndex200Response**](../Model/SitesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesLoadBalancingNodesIndex()`

```php
organizationsServersSitesLoadBalancingNodesIndex($organization, $server, $site, $sort, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServersSitesLoadBalancingNodesIndex200Response
```

List load balancing nodes

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$sort = 'sort_example'; // string | Available sorts are `id`. You can sort by multiple options by separating them with a comma. To sort in descending order, use `-` sign in front of the sort, for example: `-id`.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsServersSitesLoadBalancingNodesIndex($organization, $server, $site, $sort, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLoadBalancingNodesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **sort** | **string**| Available sorts are &#x60;id&#x60;. You can sort by multiple options by separating them with a comma. To sort in descending order, use &#x60;-&#x60; sign in front of the sort, for example: &#x60;-id&#x60;. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesLoadBalancingNodesIndex200Response**](../Model/OrganizationsServersSitesLoadBalancingNodesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesLoadBalancingNodesUpdate()`

```php
organizationsServersSitesLoadBalancingNodesUpdate($organization, $server, $site, $update_load_balancer_request)
```

Update load balancing nodes

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$update_load_balancer_request = new \Dimer47\Model\UpdateLoadBalancerRequest(); // \Dimer47\Model\UpdateLoadBalancerRequest

try {
    $apiInstance->organizationsServersSitesLoadBalancingNodesUpdate($organization, $server, $site, $update_load_balancer_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLoadBalancingNodesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **update_load_balancer_request** | [**\Dimer47\Model\UpdateLoadBalancerRequest**](../Model/UpdateLoadBalancerRequest.md)|  | |

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

## `organizationsServersSitesLogsApplicationDestroy()`

```php
organizationsServersSitesLogsApplicationDestroy($organization, $server, $site)
```

Delete site log content

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesLogsApplicationDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLogsApplicationDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesLogsApplicationShow()`

```php
organizationsServersSitesLogsApplicationShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesLogsApplicationShow200Response
```

Get site log content

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesLogsApplicationShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLogsApplicationShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesLogsApplicationShow200Response**](../Model/OrganizationsServersSitesLogsApplicationShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesLogsNginxAccessDestroy()`

```php
organizationsServersSitesLogsNginxAccessDestroy($organization, $server, $site)
```

Delete Nginx access log content

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesLogsNginxAccessDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLogsNginxAccessDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesLogsNginxAccessShow()`

```php
organizationsServersSitesLogsNginxAccessShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesLogsNginxAccessShow200Response
```

Get Nginx access log content

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesLogsNginxAccessShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLogsNginxAccessShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesLogsNginxAccessShow200Response**](../Model/OrganizationsServersSitesLogsNginxAccessShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesLogsNginxErrorDestroy()`

```php
organizationsServersSitesLogsNginxErrorDestroy($organization, $server, $site)
```

Delete Nginx error log content

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $apiInstance->organizationsServersSitesLogsNginxErrorDestroy($organization, $server, $site);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLogsNginxErrorDestroy: ', $e->getMessage(), PHP_EOL;
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

## `organizationsServersSitesLogsNginxErrorShow()`

```php
organizationsServersSitesLogsNginxErrorShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesLogsNginxErrorShow200Response
```

Get Nginx error log content

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesLogsNginxErrorShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesLogsNginxErrorShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesLogsNginxErrorShow200Response**](../Model/OrganizationsServersSitesLogsNginxErrorShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesNginxShow()`

```php
organizationsServersSitesNginxShow($organization, $server, $site): \Dimer47\Model\OrganizationsServersSitesDomainsNginxShow200Response
```

Get Nginx configuration

Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsServersSitesNginxShow($organization, $server, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesNginxShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsServersSitesDomainsNginxShow200Response**](../Model/OrganizationsServersSitesDomainsNginxShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesNginxUpdate()`

```php
organizationsServersSitesNginxUpdate($organization, $server, $site, $update_nginx_configuration_request)
```

Update Nginx configuration

Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$update_nginx_configuration_request = new \Dimer47\Model\UpdateNginxConfigurationRequest(); // \Dimer47\Model\UpdateNginxConfigurationRequest

try {
    $apiInstance->organizationsServersSitesNginxUpdate($organization, $server, $site, $update_nginx_configuration_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesNginxUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **update_nginx_configuration_request** | [**\Dimer47\Model\UpdateNginxConfigurationRequest**](../Model/UpdateNginxConfigurationRequest.md)|  | |

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

## `organizationsServersSitesStore()`

```php
organizationsServersSitesStore($organization, $server, $create_site_request): \Dimer47\Model\OrganizationsSitesShow200Response
```

Create site

Add a new site to the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$create_site_request = new \Dimer47\Model\CreateSiteRequest(); // \Dimer47\Model\CreateSiteRequest

try {
    $result = $apiInstance->organizationsServersSitesStore($organization, $server, $create_site_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **create_site_request** | [**\Dimer47\Model\CreateSiteRequest**](../Model/CreateSiteRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsSitesShow200Response**](../Model/OrganizationsSitesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsServersSitesUpdate()`

```php
organizationsServersSitesUpdate($organization, $server, $site, $update_site_request)
```

Update site

Update a site on the server.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$server = 56; // int | The server ID
$site = 56; // int | The site ID
$update_site_request = new \Dimer47\Model\UpdateSiteRequest(); // \Dimer47\Model\UpdateSiteRequest

try {
    $apiInstance->organizationsServersSitesUpdate($organization, $server, $site, $update_site_request);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsServersSitesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **server** | **int**| The server ID | |
| **site** | **int**| The site ID | |
| **update_site_request** | [**\Dimer47\Model\UpdateSiteRequest**](../Model/UpdateSiteRequest.md)|  | [optional] |

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

## `organizationsSitesIndex()`

```php
organizationsSitesIndex($organization, $include, $page_size, $page_cursor, $filter_name): \Dimer47\Model\SitesIndex200Response
```

List sites for Organization

Show all sites for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$include = 'include_example'; // string | Available includes are `server`, `serverCount`, `serverExists`, `tags`, `tagsCount`, `tagsExists`, `latestDeployment`, `latestDeploymentCount`, `latestDeploymentExists`, `securityRules`, `securityRulesCount`, `securityRulesExists`, `redirectRules`, `redirectRulesCount`, `redirectRulesExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string

try {
    $result = $apiInstance->organizationsSitesIndex($organization, $include, $page_size, $page_cursor, $filter_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsSitesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **include** | **string**| Available includes are &#x60;server&#x60;, &#x60;serverCount&#x60;, &#x60;serverExists&#x60;, &#x60;tags&#x60;, &#x60;tagsCount&#x60;, &#x60;tagsExists&#x60;, &#x60;latestDeployment&#x60;, &#x60;latestDeploymentCount&#x60;, &#x60;latestDeploymentExists&#x60;, &#x60;securityRules&#x60;, &#x60;securityRulesCount&#x60;, &#x60;securityRulesExists&#x60;, &#x60;redirectRules&#x60;, &#x60;redirectRulesCount&#x60;, &#x60;redirectRulesExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\SitesIndex200Response**](../Model/SitesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsSitesShow()`

```php
organizationsSitesShow($organization, $site): \Dimer47\Model\OrganizationsSitesShow200Response
```

Get site

Show the specified site.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$site = 56; // int | The site ID

try {
    $result = $apiInstance->organizationsSitesShow($organization, $site);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->organizationsSitesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **site** | **int**| The site ID | |

### Return type

[**\Dimer47\Model\OrganizationsSitesShow200Response**](../Model/OrganizationsSitesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sitesIndex()`

```php
sitesIndex($include, $page_size, $page_cursor, $filter_name): \Dimer47\Model\SitesIndex200Response
```

List sites

Show all sites the current token has access to.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\SitesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$include = 'include_example'; // string | Available includes are `server`, `serverCount`, `serverExists`, `tags`, `tagsCount`, `tagsExists`, `latestDeployment`, `latestDeploymentCount`, `latestDeploymentExists`, `securityRules`, `securityRulesCount`, `securityRulesExists`, `redirectRules`, `redirectRulesCount`, `redirectRulesExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.
$filter_name = 'filter_name_example'; // string

try {
    $result = $apiInstance->sitesIndex($include, $page_size, $page_cursor, $filter_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SitesApi->sitesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **include** | **string**| Available includes are &#x60;server&#x60;, &#x60;serverCount&#x60;, &#x60;serverExists&#x60;, &#x60;tags&#x60;, &#x60;tagsCount&#x60;, &#x60;tagsExists&#x60;, &#x60;latestDeployment&#x60;, &#x60;latestDeploymentCount&#x60;, &#x60;latestDeploymentExists&#x60;, &#x60;securityRules&#x60;, &#x60;securityRulesCount&#x60;, &#x60;securityRulesExists&#x60;, &#x60;redirectRules&#x60;, &#x60;redirectRulesCount&#x60;, &#x60;redirectRulesExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |
| **filter_name** | **string**|  | [optional] |

### Return type

[**\Dimer47\Model\SitesIndex200Response**](../Model/SitesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
