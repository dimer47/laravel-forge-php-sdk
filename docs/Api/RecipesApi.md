# Dimer47\RecipesApi



All URIs are relative to https://forge.laravel.com/api, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**forgeRecipesIndex()**](RecipesApi.md#forgeRecipesIndex) | **GET** /forge-recipes | List Forge&#39;s recipes |
| [**forgeRecipesRunsStore()**](RecipesApi.md#forgeRecipesRunsStore) | **POST** /forge-recipes/{forgeRecipe}/runs | Create Forge recipe run |
| [**forgeRecipesShow()**](RecipesApi.md#forgeRecipesShow) | **GET** /forge-recipes/{forgeRecipe} | Get Forge recipe |
| [**organizationRecipesStore()**](RecipesApi.md#organizationRecipesStore) | **POST** /orgs/{organization}/recipes | Create recipe |
| [**organizationsRecipesDestroy()**](RecipesApi.md#organizationsRecipesDestroy) | **DELETE** /orgs/{organization}/recipes/{recipe} | Delete recipe |
| [**organizationsRecipesIndex()**](RecipesApi.md#organizationsRecipesIndex) | **GET** /orgs/{organization}/recipes | List organization recipes |
| [**organizationsRecipesRunsIndex()**](RecipesApi.md#organizationsRecipesRunsIndex) | **GET** /orgs/{organization}/recipes/{recipe}/runs | List recipe runs |
| [**organizationsRecipesRunsShow()**](RecipesApi.md#organizationsRecipesRunsShow) | **GET** /orgs/{organization}/recipes/{recipe}/runs/{log} | Get recipe run |
| [**organizationsRecipesRunsStore()**](RecipesApi.md#organizationsRecipesRunsStore) | **POST** /orgs/{organization}/recipes/{recipe}/runs | Create recipe run |
| [**organizationsRecipesShow()**](RecipesApi.md#organizationsRecipesShow) | **GET** /orgs/{organization}/recipes/{recipe} | Get recipe |
| [**organizationsRecipesUpdate()**](RecipesApi.md#organizationsRecipesUpdate) | **PUT** /orgs/{organization}/recipes/{recipe} | Update recipe |
| [**organizationsTeamsRecipesDestroy()**](RecipesApi.md#organizationsTeamsRecipesDestroy) | **DELETE** /orgs/{organization}/teams/{team}/recipes/{recipe} | Delete a recipe share |
| [**organizationsTeamsRecipesIndex()**](RecipesApi.md#organizationsTeamsRecipesIndex) | **GET** /orgs/{organization}/teams/{team}/recipes | List team recipes |
| [**organizationsTeamsRecipesStore()**](RecipesApi.md#organizationsTeamsRecipesStore) | **POST** /orgs/{organization}/teams/{team}/recipes | Share recipe with the team |


## `forgeRecipesIndex()`

```php
forgeRecipesIndex($page_size, $page_cursor): \Dimer47\Model\ForgeRecipesIndex200Response
```

List Forge's recipes

Show all Forge provided recipes.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->forgeRecipesIndex($page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->forgeRecipesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\ForgeRecipesIndex200Response**](../Model/ForgeRecipesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `forgeRecipesRunsStore()`

```php
forgeRecipesRunsStore($forge_recipe, $run_recipe_request)
```

Create Forge recipe run

Run a Forge recipe on specified servers.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forge_recipe = 56; // int | The forge recipe ID
$run_recipe_request = new \Dimer47\Model\RunRecipeRequest(); // \Dimer47\Model\RunRecipeRequest

try {
    $apiInstance->forgeRecipesRunsStore($forge_recipe, $run_recipe_request);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->forgeRecipesRunsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **forge_recipe** | **int**| The forge recipe ID | |
| **run_recipe_request** | [**\Dimer47\Model\RunRecipeRequest**](../Model/RunRecipeRequest.md)|  | |

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

## `forgeRecipesShow()`

```php
forgeRecipesShow($forge_recipe): \Dimer47\Model\ForgeRecipesShow200Response
```

Get Forge recipe

Show the Forge recipe.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$forge_recipe = 56; // int | The forge recipe ID

try {
    $result = $apiInstance->forgeRecipesShow($forge_recipe);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->forgeRecipesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **forge_recipe** | **int**| The forge recipe ID | |

### Return type

[**\Dimer47\Model\ForgeRecipesShow200Response**](../Model/ForgeRecipesShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationRecipesStore()`

```php
organizationRecipesStore($organization, $create_recipe_request): \Dimer47\Model\OrganizationRecipesStore200Response
```

Create recipe

Create a new recipe for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$create_recipe_request = new \Dimer47\Model\CreateRecipeRequest(); // \Dimer47\Model\CreateRecipeRequest

try {
    $result = $apiInstance->organizationRecipesStore($organization, $create_recipe_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationRecipesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **create_recipe_request** | [**\Dimer47\Model\CreateRecipeRequest**](../Model/CreateRecipeRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationRecipesStore200Response**](../Model/OrganizationRecipesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRecipesDestroy()`

```php
organizationsRecipesDestroy($organization, $recipe)
```

Delete recipe

Delete a recipe from the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$recipe = 56; // int | The recipe ID

try {
    $apiInstance->organizationsRecipesDestroy($organization, $recipe);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **recipe** | **int**| The recipe ID | |

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

## `organizationsRecipesIndex()`

```php
organizationsRecipesIndex($organization, $page_size, $page_cursor): \Dimer47\Model\OrganizationsRecipesIndex200Response
```

List organization recipes

Show all recipes for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsRecipesIndex($organization, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsRecipesIndex200Response**](../Model/OrganizationsRecipesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRecipesRunsIndex()`

```php
organizationsRecipesRunsIndex($organization, $recipe, $page_size, $page_cursor): \Dimer47\Model\OrganizationsRecipesRunsIndex200Response
```

List recipe runs

Show all runs for the recipe.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$recipe = 56; // int | The recipe ID
$page_size = 30; // int | The number of results that will be returned per page.
$page_cursor = 'page_cursor_example'; // string | The cursor to start the pagination from.

try {
    $result = $apiInstance->organizationsRecipesRunsIndex($organization, $recipe, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesRunsIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **recipe** | **int**| The recipe ID | |
| **page_size** | **int**| The number of results that will be returned per page. | [optional] [default to 30] |
| **page_cursor** | **string**| The cursor to start the pagination from. | [optional] |

### Return type

[**\Dimer47\Model\OrganizationsRecipesRunsIndex200Response**](../Model/OrganizationsRecipesRunsIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRecipesRunsShow()`

```php
organizationsRecipesRunsShow($organization, $recipe, $log): \Dimer47\Model\OrganizationsRecipesRunsShow200Response
```

Get recipe run

Show a specific run for the recipe.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$recipe = 56; // int | The recipe ID
$log = 56; // int | The log ID

try {
    $result = $apiInstance->organizationsRecipesRunsShow($organization, $recipe, $log);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesRunsShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **recipe** | **int**| The recipe ID | |
| **log** | **int**| The log ID | |

### Return type

[**\Dimer47\Model\OrganizationsRecipesRunsShow200Response**](../Model/OrganizationsRecipesRunsShow200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRecipesRunsStore()`

```php
organizationsRecipesRunsStore($organization, $recipe, $run_recipe_request)
```

Create recipe run

Run a given recipe on a list of servers.  Processing mode: <small><code>async</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$recipe = 56; // int | The recipe ID
$run_recipe_request = new \Dimer47\Model\RunRecipeRequest(); // \Dimer47\Model\RunRecipeRequest

try {
    $apiInstance->organizationsRecipesRunsStore($organization, $recipe, $run_recipe_request);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesRunsStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **recipe** | **int**| The recipe ID | |
| **run_recipe_request** | [**\Dimer47\Model\RunRecipeRequest**](../Model/RunRecipeRequest.md)|  | |

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

## `organizationsRecipesShow()`

```php
organizationsRecipesShow($organization, $recipe): \Dimer47\Model\OrganizationRecipesStore200Response
```

Get recipe

Show the recipe for the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$recipe = 56; // int | The recipe ID

try {
    $result = $apiInstance->organizationsRecipesShow($organization, $recipe);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesShow: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **recipe** | **int**| The recipe ID | |

### Return type

[**\Dimer47\Model\OrganizationRecipesStore200Response**](../Model/OrganizationRecipesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsRecipesUpdate()`

```php
organizationsRecipesUpdate($organization, $recipe, $update_recipe_request): \Dimer47\Model\OrganizationRecipesStore200Response
```

Update recipe

Update a recipe in the organization.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$recipe = 56; // int | The recipe ID
$update_recipe_request = new \Dimer47\Model\UpdateRecipeRequest(); // \Dimer47\Model\UpdateRecipeRequest

try {
    $result = $apiInstance->organizationsRecipesUpdate($organization, $recipe, $update_recipe_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsRecipesUpdate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **recipe** | **int**| The recipe ID | |
| **update_recipe_request** | [**\Dimer47\Model\UpdateRecipeRequest**](../Model/UpdateRecipeRequest.md)|  | [optional] |

### Return type

[**\Dimer47\Model\OrganizationRecipesStore200Response**](../Model/OrganizationRecipesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsRecipesDestroy()`

```php
organizationsTeamsRecipesDestroy($organization, $team, $recipe)
```

Delete a recipe share

Unshare a recipe with a team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$recipe = 56; // int | The recipe ID

try {
    $apiInstance->organizationsTeamsRecipesDestroy($organization, $team, $recipe);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsTeamsRecipesDestroy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **recipe** | **int**| The recipe ID | |

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

## `organizationsTeamsRecipesIndex()`

```php
organizationsTeamsRecipesIndex($organization, $team, $page_size, $page_cursor): \Dimer47\Model\OrganizationsRecipesIndex200Response
```

List team recipes

Show all recipes for the team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
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
    $result = $apiInstance->organizationsTeamsRecipesIndex($organization, $team, $page_size, $page_cursor);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsTeamsRecipesIndex: ', $e->getMessage(), PHP_EOL;
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

[**\Dimer47\Model\OrganizationsRecipesIndex200Response**](../Model/OrganizationsRecipesIndex200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `organizationsTeamsRecipesStore()`

```php
organizationsTeamsRecipesStore($organization, $team, $share_recipe_request): \Dimer47\Model\OrganizationRecipesStore200Response
```

Share recipe with the team

Shares a recipe with a team.  Processing mode: <small><code>sync</code></small>

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Dimer47\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Dimer47\Api\RecipesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$organization = 'organization_example'; // string | The organization slug
$team = 56; // int | The team ID
$share_recipe_request = new \Dimer47\Model\ShareRecipeRequest(); // \Dimer47\Model\ShareRecipeRequest

try {
    $result = $apiInstance->organizationsTeamsRecipesStore($organization, $team, $share_recipe_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RecipesApi->organizationsTeamsRecipesStore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **organization** | **string**| The organization slug | |
| **team** | **int**| The team ID | |
| **share_recipe_request** | [**\Dimer47\Model\ShareRecipeRequest**](../Model/ShareRecipeRequest.md)|  | |

### Return type

[**\Dimer47\Model\OrganizationRecipesStore200Response**](../Model/OrganizationRecipesStore200Response.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/vnd.api+json`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
