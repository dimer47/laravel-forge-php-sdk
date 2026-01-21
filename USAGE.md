# Laravel Forge PHP SDK - Usage Guide

This SDK was automatically generated from the `laravel-forge-openapi.yaml` OpenAPI specification.

## Installation

```bash
composer require dimer47/laravel-forge-sdk
```

## Configuration

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\ServersApi;
use Dimer\ForgeSDK\Api\SitesApi;

// Configure with Bearer token
$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');
```

## Usage Examples

### List Servers

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\ServersApi;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');

$serversApi = new ServersApi(null, $config);

// List servers for an organization
$servers = $serversApi->listServers('my-organization');

foreach ($servers->getData() as $server) {
    echo $server->getAttributes()->getName() . "\n";
}
```

### Create a Site

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\SitesApi;
use Dimer\ForgeSDK\Model\CreateSiteRequest;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');

$sitesApi = new SitesApi(null, $config);

$request = new CreateSiteRequest([
    'domain' => 'example.com',
    'project_type' => 'php',
    'directory' => '/public',
]);

$site = $sitesApi->createSite('my-organization', 123456, $request);
```

### Manage Deployments

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\DeploymentsApi;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');

$deploymentsApi = new DeploymentsApi(null, $config);

// Trigger a deployment
$deploymentsApi->createSiteDeployment('my-organization', 123456, 789);

// Get deployment script
$script = $deploymentsApi->getSiteDeploymentScript('my-organization', 123456, 789);
```

### Manage Databases

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\DatabasesApi;
use Dimer\ForgeSDK\Model\CreateDatabaseRequest;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');

$databasesApi = new DatabasesApi(null, $config);

// Create a database
$request = new CreateDatabaseRequest([
    'name' => 'my_database',
]);

$databasesApi->createDatabaseSchema('my-organization', 123456, $request);
```

### Manage PHP

```php
use Dimer\ForgeSDK\Configuration;
use Dimer\ForgeSDK\Api\PHPApi;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');

$phpApi = new PHPApi(null, $config);

// List installed PHP versions
$versions = $phpApi->listPhpVersions('my-organization', 123456);

// Update PHP CLI version
$phpApi->updatePhpCliVersion('my-organization', 123456, [
    'php_version' => '8.3'
]);
```

## Available API Classes

| Class | Description |
|-------|-------------|
| `BackgroundProcessesApi` | Manage daemons/supervisor processes |
| `CertificatesApi` | SSL certificate management |
| `CommandsApi` | Execute commands on sites |
| `ComposerCredentialsApi` | Private package credentials |
| `DatabasesApi` | Database and user management |
| `DeploymentsApi` | Deployment management |
| `DomainsApi` | Domain management |
| `FirewallRulesApi` | Firewall rule management |
| `HeartbeatsApi` | Heartbeat monitoring |
| `IntegrationsApi` | Laravel integrations (Horizon, Octane, etc.) |
| `LoadBalancingApi` | Load balancing configuration |
| `MonitorsApi` | Server monitoring |
| `NginxApi` | Nginx template management |
| `OrganizationsApi` | Organization management |
| `PHPApi` | PHP version and configuration |
| `ProvidersApi` | Cloud provider information |
| `RecipesApi` | Automation recipes |
| `RedirectRulesApi` | Redirect rule management |
| `RolesApi` | Role and permission management |
| `SSHKeysApi` | SSH key management |
| `ScheduledJobsApi` | Cron job management |
| `SecurityRulesApi` | Security rule management |
| `ServersApi` | Server management |
| `ServicesApi` | Service actions (nginx, mysql, etc.) |
| `SitesApi` | Site management |
| `TeamsApi` | Team management |
| `UserApi` | Current user information |
| `WebhooksApi` | Deployment webhooks |

## Available Models

The SDK contains 167 models for API requests and responses, including:

- `Server`, `ServerAttributes`, `ServerResponse`, `ServerListResponse`
- `Site`, `SiteAttributes`, `SiteResponse`, `SiteListResponse`
- `Database`, `DatabaseUser`, `CreateDatabaseRequest`
- `Certificate`, `Domain`, `Deployment`
- And many more...

## Error Handling

```php
use Dimer\ForgeSDK\ApiException;

try {
    $servers = $serversApi->listServers('my-organization');
} catch (ApiException $e) {
    echo "API Error: " . $e->getMessage() . "\n";
    echo "Status Code: " . $e->getCode() . "\n";
    echo "Response Body: " . $e->getResponseBody() . "\n";
}
```

## Rate Limiting

Laravel Forge API has a rate limit of 60 requests per minute. The SDK does not handle rate limiting automatically - implement retry logic in your application if needed.
