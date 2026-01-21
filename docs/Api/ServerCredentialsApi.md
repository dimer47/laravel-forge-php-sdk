# Dimer47\ServerCredentialsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsTeamsServerCredentialsDestroy()**](ServerCredentialsApi.md#organizationsTeamsServerCredentialsDestroy) | **DELETE** /orgs/{organization}/teams/{team}/server-credentials/{credential} | Delete a server credential share |
| [**organizationsTeamsServerCredentialsIndex()**](ServerCredentialsApi.md#organizationsTeamsServerCredentialsIndex) | **GET** /orgs/{organization}/teams/{team}/server-credentials | List team server credentials |
| [**organizationsTeamsServerCredentialsStore()**](ServerCredentialsApi.md#organizationsTeamsServerCredentialsStore) | **POST** /orgs/{organization}/teams/{team}/server-credentials | Create a new server credential share |


## `organizationsTeamsServerCredentialsDestroy()`

```php
organizationsTeamsServerCredentialsDestroy($organization, $team, $credential)
```

Delete a server credential share

Unshare a server credential with a team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServerCredentialsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$credential = 56; // int | The credential ID

try {
    $apiInstance->organizationsTeamsServerCredentialsDestroy($organization, $team, $credential);
} catch (Exception $e) {
    echo 'Exception when calling ServerCredentialsApi->organizationsTeamsServerCredentialsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **credential** | **int**| The credential ID | |

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

## `organizationsTeamsServerCredentialsIndex()`

```php
organizationsTeamsServerCredentialsIndex($organization, $team, $page_size, $page_cursor): \Dimer47\Model\OrganizationsServerCredentialsIndex200Response
```

List team server credentials

Show all server credentials for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServerCredentialsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsTeamsServerCredentialsIndex($organization, $team, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServerCredentialsApi->organizationsTeamsServerCredentialsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsServerCredentialsIndex200Response**](../Model/OrganizationsServerCredentialsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsServerCredentialsStore()`

```php
organizationsTeamsServerCredentialsStore($organization, $team, $share_credential_request): \Dimer47\Model\OrganizationsServerCredentialsShow200Response
```

Create a new server credential share

Share a server credential with a team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\ServerCredentialsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$share_credential_request = new \Dimer47\Model\ShareCredentialRequest(); // \Dimer47\Model\ShareCredentialRequest

try {
    $result = $apiInstance->organizationsTeamsServerCredentialsStore($organization, $team, $share_credential_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServerCredentialsApi->organizationsTeamsServerCredentialsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **share_credential_request** | [**\Dimer47\Model\ShareCredentialRequest**](../Model/ShareCredentialRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsServerCredentialsShow200Response**](../Model/OrganizationsServerCredentialsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
