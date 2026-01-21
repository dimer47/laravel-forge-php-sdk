# Dimer47\TeamsApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**organizationsTeamsDestroy()**](TeamsApi.md#organizationsTeamsDestroy) | **DELETE** /orgs/{organization}/teams/{team} | Delete team |
| [**organizationsTeamsIndex()**](TeamsApi.md#organizationsTeamsIndex) | **GET** /orgs/{organization}/teams | List teams |
| [**organizationsTeamsInvitesDestroy()**](TeamsApi.md#organizationsTeamsInvitesDestroy) | **DELETE** /orgs/{organization}/teams/{team}/invites/{invitation} | Delete team invitation |
| [**organizationsTeamsInvitesIndex()**](TeamsApi.md#organizationsTeamsInvitesIndex) | **GET** /orgs/{organization}/teams/{team}/invites | List team invitations |
| [**organizationsTeamsInvitesShow()**](TeamsApi.md#organizationsTeamsInvitesShow) | **GET** /orgs/{organization}/teams/{team}/invites/{invitation} | Get team invitation |
| [**organizationsTeamsInvitesStore()**](TeamsApi.md#organizationsTeamsInvitesStore) | **POST** /orgs/{organization}/teams/{team}/invites | Create team invite |
| [**organizationsTeamsMembersDestroy()**](TeamsApi.md#organizationsTeamsMembersDestroy) | **DELETE** /orgs/{organization}/teams/{team}/members/{user} | Delete team member |
| [**organizationsTeamsMembersIndex()**](TeamsApi.md#organizationsTeamsMembersIndex) | **GET** /orgs/{organization}/teams/{team}/members | List team members |
| [**organizationsTeamsMembersShow()**](TeamsApi.md#organizationsTeamsMembersShow) | **GET** /orgs/{organization}/teams/{team}/members/{user} | Get team member |
| [**organizationsTeamsMembersUpdate()**](TeamsApi.md#organizationsTeamsMembersUpdate) | **PUT** /orgs/{organization}/teams/{team}/members/{user} | Update team member |
| [**organizationsTeamsShow()**](TeamsApi.md#organizationsTeamsShow) | **GET** /orgs/{organization}/teams/{team} | Get team |
| [**organizationsTeamsStore()**](TeamsApi.md#organizationsTeamsStore) | **POST** /orgs/{organization}/teams | Create team |
| [**organizationsTeamsUpdate()**](TeamsApi.md#organizationsTeamsUpdate) | **PUT** /orgs/{organization}/teams/{team} | Update team |


## `organizationsTeamsDestroy()`

```php
organizationsTeamsDestroy($organization, $team)
```

Delete team

Delete a team for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID

try {
    $apiInstance->organizationsTeamsDestroy($organization, $team);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |

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

## `organizationsTeamsIndex()`

```php
organizationsTeamsIndex($organization, $page_size, $page_cursor): \Dimer47\Model\OrganizationsTeamsIndex200Response
```

List teams

Show all teams for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsTeamsIndex($organization, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsTeamsIndex200Response**](../Model/OrganizationsTeamsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsInvitesDestroy()`

```php
organizationsTeamsInvitesDestroy($organization, $team, $invitation)
```

Delete team invitation

Cancel a pending invitation for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$invitation = 56; // int | The invitation ID

try {
    $apiInstance->organizationsTeamsInvitesDestroy($organization, $team, $invitation);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsInvitesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **invitation** | **int**| The invitation ID | |

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

## `organizationsTeamsInvitesIndex()`

```php
organizationsTeamsInvitesIndex($organization, $team, $include, $page_size, $page_cursor): \Dimer47\Model\OrganizationsTeamsInvitesIndex200Response
```

List team invitations

Show all pending invitations for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$include = 'include_example'; // string | Available includes are `role`, `roleCount`, `roleExists`, `team`, `teamCount`, `teamExists`, `organization`, `organizationCount`, `organizationExists`. You can include multiple options by separating them with a comma.
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsTeamsInvitesIndex($organization, $team, $include, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsInvitesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **include** | **string**| Available includes are &#x60;role&#x60;, &#x60;roleCount&#x60;, &#x60;roleExists&#x60;, &#x60;team&#x60;, &#x60;teamCount&#x60;, &#x60;teamExists&#x60;, &#x60;organization&#x60;, &#x60;organizationCount&#x60;, &#x60;organizationExists&#x60;. You can include multiple options by separating them with a comma. | [optional] |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsTeamsInvitesIndex200Response**](../Model/OrganizationsTeamsInvitesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsInvitesShow()`

```php
organizationsTeamsInvitesShow($organization, $team, $invitation): \Dimer47\Model\OrganizationsTeamsInvitesStore200Response
```

Get team invitation

Show a pending invitation for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$invitation = 56; // int | The invitation ID

try {
    $result = $apiInstance->organizationsTeamsInvitesShow($organization, $team, $invitation);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsInvitesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **invitation** | **int**| The invitation ID | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsInvitesStore200Response**](../Model/OrganizationsTeamsInvitesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsInvitesStore()`

```php
organizationsTeamsInvitesStore($organization, $team, $create_team_invite_request): \Dimer47\Model\OrganizationsTeamsInvitesStore200Response
```

Create team invite

Invite a new member to the team.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$create_team_invite_request = new \Dimer47\Model\CreateTeamInviteRequest(); // \Dimer47\Model\CreateTeamInviteRequest

try {
    $result = $apiInstance->organizationsTeamsInvitesStore($organization, $team, $create_team_invite_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsInvitesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **create_team_invite_request** | [**\Dimer47\Model\CreateTeamInviteRequest**](../Model/CreateTeamInviteRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsInvitesStore200Response**](../Model/OrganizationsTeamsInvitesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsMembersDestroy()`

```php
organizationsTeamsMembersDestroy($organization, $team, $user)
```

Delete team member

Remove a member from the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$user = 56; // int | The user ID

try {
    $apiInstance->organizationsTeamsMembersDestroy($organization, $team, $user);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsMembersDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **user** | **int**| The user ID | |

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

## `organizationsTeamsMembersIndex()`

```php
organizationsTeamsMembersIndex($organization, $team, $page_size, $page_cursor): \Dimer47\Model\OrganizationsTeamsMembersIndex200Response
```

List team members

Show all members for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
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
    $result = $apiInstance->organizationsTeamsMembersIndex($organization, $team, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsMembersIndex: ', $e->getMessage(), PHP_EOL;
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

[**\Dimer47\Model\OrganizationsTeamsMembersIndex200Response**](../Model/OrganizationsTeamsMembersIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsMembersShow()`

```php
organizationsTeamsMembersShow($organization, $team, $user): \Dimer47\Model\OrganizationsTeamsMembersShow200Response
```

Get team member

Show the team member for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$user = 56; // int | The user ID

try {
    $result = $apiInstance->organizationsTeamsMembersShow($organization, $team, $user);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsMembersShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **user** | **int**| The user ID | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsMembersShow200Response**](../Model/OrganizationsTeamsMembersShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsMembersUpdate()`

```php
organizationsTeamsMembersUpdate($organization, $team, $user, $update_team_member_request): \Dimer47\Model\OrganizationsTeamsMembersShow200Response
```

Update team member

Update the team member for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$user = 56; // int | The user ID
$update_team_member_request = new \Dimer47\Model\UpdateTeamMemberRequest(); // \Dimer47\Model\UpdateTeamMemberRequest

try {
    $result = $apiInstance->organizationsTeamsMembersUpdate($organization, $team, $user, $update_team_member_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsMembersUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **user** | **int**| The user ID | |
| **update_team_member_request** | [**\Dimer47\Model\UpdateTeamMemberRequest**](../Model/UpdateTeamMemberRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsMembersShow200Response**](../Model/OrganizationsTeamsMembersShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsShow()`

```php
organizationsTeamsShow($organization, $team): \Dimer47\Model\OrganizationsTeamsStore200Response
```

Get team

Show a specific team for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID

try {
    $result = $apiInstance->organizationsTeamsShow($organization, $team);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsStore200Response**](../Model/OrganizationsTeamsStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsStore()`

```php
organizationsTeamsStore($organization, $create_team_request): \Dimer47\Model\OrganizationsTeamsStore200Response
```

Create team

Create a new team for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$create_team_request = new \Dimer47\Model\CreateTeamRequest(); // \Dimer47\Model\CreateTeamRequest

try {
    $result = $apiInstance->organizationsTeamsStore($organization, $create_team_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **create_team_request** | [**\Dimer47\Model\CreateTeamRequest**](../Model/CreateTeamRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsStore200Response**](../Model/OrganizationsTeamsStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsUpdate()`

```php
organizationsTeamsUpdate($organization, $team, $update_team_request): \Dimer47\Model\OrganizationsTeamsStore200Response
```

Update team

Update a team for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\TeamsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$update_team_request = new \Dimer47\Model\UpdateTeamRequest(); // \Dimer47\Model\UpdateTeamRequest

try {
    $result = $apiInstance->organizationsTeamsUpdate($organization, $team, $update_team_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TeamsApi->organizationsTeamsUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **update_team_request** | [**\Dimer47\Model\UpdateTeamRequest**](../Model/UpdateTeamRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationsTeamsStore200Response**](../Model/OrganizationsTeamsStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
