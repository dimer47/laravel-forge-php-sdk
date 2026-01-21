# Laravel Forge PHP SDK

[![Latest Version on Packagist](https://img.shields.io/packagist/v/dimer47/laravel-forge-sdk.svg?style=flat-square)](https://packagist.org/packages/dimer47/laravel-forge-sdk)
[![Total Downloads](https://img.shields.io/packagist/dt/dimer47/laravel-forge-sdk.svg?style=flat-square)](https://packagist.org/packages/dimer47/laravel-forge-sdk)
[![License](https://img.shields.io/packagist/l/dimer47/laravel-forge-sdk.svg?style=flat-square)](https://packagist.org/packages/dimer47/laravel-forge-sdk)

A comprehensive PHP SDK for the [Laravel Forge API](https://forge.laravel.com/api-documentation), auto-generated from the official OpenAPI specification.

## Features

- **Complete API Coverage**: All Laravel Forge endpoints
- **Type-Safe**: Fully typed request/response models
- **PSR-7/PSR-18 Compatible**: Uses Guzzle HTTP client
- **Modern PHP**: Requires PHP 8.1+
- **Well Documented**: Inline documentation and examples

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

```bash
composer require dimer47/laravel-forge-sdk
```

Or add the following to `composer.json`:

```json
{
  "require": {
    "dimer47/laravel-forge-sdk": "^1.0"
  }
}
```

Then run `composer install`

## Quick Start

```php
<?php
require_once __DIR__ . '/vendor/autoload.php';

use Dimer47\LaravelForgeSdk\Configuration;
use Dimer47\LaravelForgeSdk\Api\ServersApi;

// Configure API token
$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');

// Create API instance
$serversApi = new ServersApi(
    new GuzzleHttp\Client(),
    $config
);

// List servers
$servers = $serversApi->organizationsServersIndex('your-organization');

foreach ($servers->getData() as $server) {
    echo $server->getAttributes()->getName() . "\n";
}
```

## Configuration

### Authentication

Laravel Forge API uses Bearer token authentication. Generate a token from your [Forge account settings](https://forge.laravel.com/user-profile/api).

```php
use Dimer47\LaravelForgeSdk\Configuration;

$config = Configuration::getDefaultConfiguration()
    ->setAccessToken('your-forge-api-token');
```

### Custom HTTP Client

You can provide your own Guzzle client:

```php
use GuzzleHttp\Client;
use Dimer47\LaravelForgeSdk\Api\ServersApi;

$client = new Client([
    'timeout' => 30,
    'verify' => true,
]);

$serversApi = new ServersApi($client, $config);
```

## Usage Examples

### Managing Servers

```php
use Dimer47\LaravelForgeSdk\Api\ServersApi;
use Dimer47\LaravelForgeSdk\Model\CreateServerRequest;

$serversApi = new ServersApi(null, $config);

// List servers
$servers = $serversApi->organizationsServersIndex('my-org');

// Get a specific server
$server = $serversApi->organizationsServersShow('my-org', 123456);

// Create a server
$request = new CreateServerRequest([
    'name' => 'my-server',
    'provider' => 'ocean2',
    'region' => 'nyc3',
    'size' => 's-1vcpu-1gb',
    'php_version' => '8.3',
]);
$newServer = $serversApi->organizationsServersStore('my-org', $request);

// Reboot a server
$serversApi->organizationsServersActionsStore('my-org', 123456, ['action' => 'reboot']);

// Delete a server
$serversApi->organizationsServersDestroy('my-org', 123456);
```

### Managing Sites

```php
use Dimer47\LaravelForgeSdk\Api\SitesApi;
use Dimer47\LaravelForgeSdk\Model\CreateSiteRequest;

$sitesApi = new SitesApi(null, $config);

// List sites on a server
$sites = $sitesApi->organizationsServersSitesIndex('my-org', 123456);

// Create a site
$request = new CreateSiteRequest([
    'domain' => 'example.com',
    'project_type' => 'php',
    'directory' => '/public',
]);
$site = $sitesApi->organizationsServersSitesStore('my-org', 123456, $request);

// Get/Update Nginx configuration
$nginxConfig = $sitesApi->organizationsServersSitesNginxShow('my-org', 123456, 789);

// Get/Update .env file
$env = $sitesApi->organizationsServersSitesEnvironmentShow('my-org', 123456, 789);
```

### Managing Deployments

```php
use Dimer47\LaravelForgeSdk\Api\DeploymentsApi;

$deploymentsApi = new DeploymentsApi(null, $config);

// Trigger a deployment
$deploymentsApi->organizationsServersSitesDeploymentsStore('my-org', 123456, 789);

// Get deployment script
$script = $deploymentsApi->organizationsServersSitesDeploymentsScriptShow('my-org', 123456, 789);

// Get deployment status
$status = $deploymentsApi->organizationsServersSitesDeploymentsStatusShow('my-org', 123456, 789);

// Enable push-to-deploy
$deploymentsApi->organizationsServersSitesDeploymentsPushToDeployStore('my-org', 123456, 789);
```

### Managing Databases

```php
use Dimer47\LaravelForgeSdk\Api\DatabasesApi;
use Dimer47\LaravelForgeSdk\Model\CreateDatabaseRequest;
use Dimer47\LaravelForgeSdk\Model\CreateDatabaseUserRequest;

$databasesApi = new DatabasesApi(null, $config);

// Create a database
$request = new CreateDatabaseRequest(['name' => 'my_database']);
$databasesApi->organizationsServersDatabaseSchemasStore('my-org', 123456, $request);

// Create a database user
$userRequest = new CreateDatabaseUserRequest([
    'name' => 'my_user',
    'password' => 'secure_password',
    'database_ids' => [1, 2, 3],
]);
$databasesApi->organizationsServersDatabaseUsersStore('my-org', 123456, $userRequest);

// List databases
$databases = $databasesApi->organizationsServersDatabaseSchemasIndex('my-org', 123456);
```

### Managing Background Processes (Daemons)

```php
use Dimer47\LaravelForgeSdk\Api\BackgroundProcessesApi;

$daemonsApi = new BackgroundProcessesApi(null, $config);

// List daemons
$daemons = $daemonsApi->organizationsServersBackgroundProcessesIndex('my-org', 123456);

// Create a daemon
$daemonsApi->organizationsServersBackgroundProcessesStore('my-org', 123456, [
    'command' => 'php /home/forge/example.com/artisan queue:work',
    'user' => 'forge',
    'directory' => '/home/forge/example.com',
]);
```

### Managing Scheduled Jobs (Cron)

```php
use Dimer47\LaravelForgeSdk\Api\ScheduledJobsApi;
use Dimer47\LaravelForgeSdk\Model\CreateScheduledJobRequest;

$cronApi = new ScheduledJobsApi(null, $config);

// Create a cron job
$request = new CreateScheduledJobRequest([
    'command' => 'php /home/forge/example.com/artisan schedule:run',
    'frequency' => 'minutely',
    'user' => 'forge',
]);
$cronApi->organizationsServersScheduledJobsStore('my-org', 123456, $request);
```

### Managing Laravel Integrations

```php
use Dimer47\LaravelForgeSdk\Api\IntegrationsApi;

$integrationsApi = new IntegrationsApi(null, $config);

// Enable Laravel Horizon
$integrationsApi->organizationsServersSitesIntegrationsHorizonStore('my-org', 123456, 789);

// Enable Laravel Octane
$integrationsApi->organizationsServersSitesIntegrationsOctaneStore('my-org', 123456, 789, [
    'server' => 'swoole',
    'port' => 8000,
]);

// Enable Laravel Reverb (WebSockets)
$integrationsApi->organizationsServersSitesIntegrationsReverbStore('my-org', 123456, 789, [
    'port' => 6001,
]);

// Get integration status
$status = $integrationsApi->organizationsServersSitesIntegrationsHorizonShow('my-org', 123456, 789);
```

## API Endpoints

All URIs are relative to *https://forge.laravel.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BackgroundProcessesApi* | [**organizationsServersBackgroundProcessesDestroy**](docs/Api/BackgroundProcessesApi.md#organizationsserversbackgroundprocessesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess} | Delete background process
*BackgroundProcessesApi* | [**organizationsServersBackgroundProcessesIndex**](docs/Api/BackgroundProcessesApi.md#organizationsserversbackgroundprocessesindex) | **GET** /orgs/{organization}/servers/{server}/background-processes | List background processes
*BackgroundProcessesApi* | [**organizationsServersBackgroundProcessesLogShow**](docs/Api/BackgroundProcessesApi.md#organizationsserversbackgroundprocesseslogshow) | **GET** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess}/log | Get background process log
*BackgroundProcessesApi* | [**organizationsServersBackgroundProcessesShow**](docs/Api/BackgroundProcessesApi.md#organizationsserversbackgroundprocessesshow) | **GET** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess} | Get background process
*BackgroundProcessesApi* | [**organizationsServersBackgroundProcessesStore**](docs/Api/BackgroundProcessesApi.md#organizationsserversbackgroundprocessesstore) | **POST** /orgs/{organization}/servers/{server}/background-processes | Create background process
*BackgroundProcessesApi* | [**organizationsServersBackgroundProcessesUpdate**](docs/Api/BackgroundProcessesApi.md#organizationsserversbackgroundprocessesupdate) | **PUT** /orgs/{organization}/servers/{server}/background-processes/{backgroundProcess} | Update background process
*BackupsApi* | [**organizationsServersDatabaseBackupsDestroy**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsdestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration} | Delete backup configuration
*BackupsApi* | [**organizationsServersDatabaseBackupsIndex**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsindex) | **GET** /orgs/{organization}/servers/{server}/database/backups | List backup configurations
*BackupsApi* | [**organizationsServersDatabaseBackupsInstancesDestroy**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsinstancesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances/{backup} | Delete backup
*BackupsApi* | [**organizationsServersDatabaseBackupsInstancesIndex**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsinstancesindex) | **GET** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances | List backups
*BackupsApi* | [**organizationsServersDatabaseBackupsInstancesRestoresStore**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsinstancesrestoresstore) | **POST** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances/{backup}/restores | Create a database restore from backup
*BackupsApi* | [**organizationsServersDatabaseBackupsInstancesShow**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsinstancesshow) | **GET** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances/{backup} | Get backup
*BackupsApi* | [**organizationsServersDatabaseBackupsInstancesStore**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsinstancesstore) | **POST** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration}/instances | Create backup
*BackupsApi* | [**organizationsServersDatabaseBackupsShow**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsshow) | **GET** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration} | Get backup configuration
*BackupsApi* | [**organizationsServersDatabaseBackupsStore**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsstore) | **POST** /orgs/{organization}/servers/{server}/database/backups | Create backup configuration
*BackupsApi* | [**organizationsServersDatabaseBackupsUpdate**](docs/Api/BackupsApi.md#organizationsserversdatabasebackupsupdate) | **PUT** /orgs/{organization}/servers/{server}/database/backups/{backupConfiguration} | Update backup configuration
*CommandsApi* | [**organizationsServersSitesCommandsDestroy**](docs/Api/CommandsApi.md#organizationsserverssitescommandsdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/commands/{command} | Delete command
*CommandsApi* | [**organizationsServersSitesCommandsIndex**](docs/Api/CommandsApi.md#organizationsserverssitescommandsindex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/commands | List commands
*CommandsApi* | [**organizationsServersSitesCommandsOutputShow**](docs/Api/CommandsApi.md#organizationsserverssitescommandsoutputshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/commands/{command}/output | Get command output
*CommandsApi* | [**organizationsServersSitesCommandsShow**](docs/Api/CommandsApi.md#organizationsserverssitescommandsshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/commands/{command} | Get command
*CommandsApi* | [**organizationsServersSitesCommandsStore**](docs/Api/CommandsApi.md#organizationsserverssitescommandsstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/commands | Create command
*DatabasesApi* | [**organizationsServersDatabasePasswordUpdate**](docs/Api/DatabasesApi.md#organizationsserversdatabasepasswordupdate) | **PUT** /orgs/{organization}/servers/{server}/database/password | Update the password for the database
*DatabasesApi* | [**organizationsServersDatabaseSchemasDestroy**](docs/Api/DatabasesApi.md#organizationsserversdatabaseschemasdestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/schemas/{database} | Delete database schema
*DatabasesApi* | [**organizationsServersDatabaseSchemasIndex**](docs/Api/DatabasesApi.md#organizationsserversdatabaseschemasindex) | **GET** /orgs/{organization}/servers/{server}/database/schemas | List database schemas
*DatabasesApi* | [**organizationsServersDatabaseSchemasShow**](docs/Api/DatabasesApi.md#organizationsserversdatabaseschemasshow) | **GET** /orgs/{organization}/servers/{server}/database/schemas/{database} | Get database schema
*DatabasesApi* | [**organizationsServersDatabaseSchemasStore**](docs/Api/DatabasesApi.md#organizationsserversdatabaseschemasstore) | **POST** /orgs/{organization}/servers/{server}/database/schemas | Create database schema
*DatabasesApi* | [**organizationsServersDatabaseSchemasSynchronizationsStore**](docs/Api/DatabasesApi.md#organizationsserversdatabaseschemassynchronizationsstore) | **POST** /orgs/{organization}/servers/{server}/database/schemas/synchronizations | Update database schemas
*DatabasesApi* | [**organizationsServersDatabaseUsersDestroy**](docs/Api/DatabasesApi.md#organizationsserversdatabaseusersdestroy) | **DELETE** /orgs/{organization}/servers/{server}/database/users/{databaseUser} | Delete database user
*DatabasesApi* | [**organizationsServersDatabaseUsersIndex**](docs/Api/DatabasesApi.md#organizationsserversdatabaseusersindex) | **GET** /orgs/{organization}/servers/{server}/database/users | List database users
*DatabasesApi* | [**organizationsServersDatabaseUsersShow**](docs/Api/DatabasesApi.md#organizationsserversdatabaseusersshow) | **GET** /orgs/{organization}/servers/{server}/database/users/{databaseUser} | Get database user
*DatabasesApi* | [**organizationsServersDatabaseUsersStore**](docs/Api/DatabasesApi.md#organizationsserversdatabaseusersstore) | **POST** /orgs/{organization}/servers/{server}/database/users | Create database user
*DatabasesApi* | [**organizationsServersDatabaseUsersUpdate**](docs/Api/DatabasesApi.md#organizationsserversdatabaseusersupdate) | **PUT** /orgs/{organization}/servers/{server}/database/users/{databaseUser} | Update database user
*DeploymentsApi* | [**organizationsServersSitesDeploymentsDeployHookShow**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsdeployhookshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/deploy-hook | Get the deployment trigger URL
*DeploymentsApi* | [**organizationsServersSitesDeploymentsDeployHookUpdate**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsdeployhookupdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/deployments/deploy-hook | Update deployment trigger URL
*DeploymentsApi* | [**organizationsServersSitesDeploymentsIndex**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsindex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments | List deployments
*DeploymentsApi* | [**organizationsServersSitesDeploymentsLogShow**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentslogshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/{deployment}/log | Get deployment output
*DeploymentsApi* | [**organizationsServersSitesDeploymentsPushToDeployDestroy**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentspushtodeploydestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/deployments/push-to-deploy | Delete push to deploy configuration
*DeploymentsApi* | [**organizationsServersSitesDeploymentsPushToDeployStore**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentspushtodeploystore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/deployments/push-to-deploy | Create push to deploy configuration
*DeploymentsApi* | [**organizationsServersSitesDeploymentsScriptShow**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsscriptshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/script | Get deployment script
*DeploymentsApi* | [**organizationsServersSitesDeploymentsScriptUpdate**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsscriptupdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/deployments/script | Update deployment script
*DeploymentsApi* | [**organizationsServersSitesDeploymentsShow**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/{deployment} | Get deployment
*DeploymentsApi* | [**organizationsServersSitesDeploymentsStatusDestroy**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsstatusdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/deployments/status | Update deployment state
*DeploymentsApi* | [**organizationsServersSitesDeploymentsStatusShow**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsstatusshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/deployments/status | Get deployment status
*DeploymentsApi* | [**organizationsServersSitesDeploymentsStore**](docs/Api/DeploymentsApi.md#organizationsserverssitesdeploymentsstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/deployments | Create deployment
*DeploymentsApi* | [**organizationsServersSitesWebhooksDestroy**](docs/Api/DeploymentsApi.md#organizationsserverssiteswebhooksdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/webhooks/{deploymentWebhook} | Delete site webhook
*DeploymentsApi* | [**organizationsServersSitesWebhooksIndex**](docs/Api/DeploymentsApi.md#organizationsserverssiteswebhooksindex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/webhooks | List site webhooks
*DeploymentsApi* | [**organizationsServersSitesWebhooksShow**](docs/Api/DeploymentsApi.md#organizationsserverssiteswebhooksshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/webhooks/{deploymentWebhook} | Get site webhook
*DeploymentsApi* | [**organizationsServersSitesWebhooksStore**](docs/Api/DeploymentsApi.md#organizationsserverssiteswebhooksstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/webhooks | Create site webhook
*FirewallRulesApi* | [**organizationsServersFirewallRulesDestroy**](docs/Api/FirewallRulesApi.md#organizationsserversfirewallrulesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/firewall-rules/{rule} | Delete server firewall rule
*FirewallRulesApi* | [**organizationsServersFirewallRulesIndex**](docs/Api/FirewallRulesApi.md#organizationsserversfirewallrulesindex) | **GET** /orgs/{organization}/servers/{server}/firewall-rules | List server firewall rules
*FirewallRulesApi* | [**organizationsServersFirewallRulesShow**](docs/Api/FirewallRulesApi.md#organizationsserversfirewallrulesshow) | **GET** /orgs/{organization}/servers/{server}/firewall-rules/{rule} | Get server firewall rule
*FirewallRulesApi* | [**organizationsServersFirewallRulesStore**](docs/Api/FirewallRulesApi.md#organizationsserversfirewallrulesstore) | **POST** /orgs/{organization}/servers/{server}/firewall-rules | Create server firewall rule
*IntegrationsApi* | [**organizationsServersSitesIntegrationsHorizonDestroy**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationshorizondestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/horizon | Delete Laravel Horizon integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsHorizonShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationshorizonshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/horizon | Get Laravel Horizon integration status
*IntegrationsApi* | [**organizationsServersSitesIntegrationsHorizonStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationshorizonstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/horizon | Create Laravel Horizon integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsInertiaShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsinertiashow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/inertia | Get Inertia integration status
*IntegrationsApi* | [**organizationsServersSitesIntegrationsInertiaStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsinertiastore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/inertia | Create Inertia integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsLaravelMaintenanceDestroy**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationslaravelmaintenancedestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-maintenance | Delete Laravel Maintenance integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsLaravelMaintenanceShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationslaravelmaintenanceshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-maintenance | Get Laravel Maintenance integration status
*IntegrationsApi* | [**organizationsServersSitesIntegrationsLaravelMaintenanceStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationslaravelmaintenancestore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-maintenance | Create Laravel Maintenance integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsLaravelSchedulerDestroy**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationslaravelschedulerdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-scheduler | Delete Laravel Scheduler integration job
*IntegrationsApi* | [**organizationsServersSitesIntegrationsLaravelSchedulerShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationslaravelschedulershow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-scheduler | Get Laravel Scheduler integration job
*IntegrationsApi* | [**organizationsServersSitesIntegrationsLaravelSchedulerStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationslaravelschedulerstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/laravel-scheduler | Create Laravel Scheduler integration job
*IntegrationsApi* | [**organizationsServersSitesIntegrationsOctaneDestroy**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsoctanedestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/octane | Delete Laravel Octane integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsOctaneShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsoctaneshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/octane | Get Laravel Octane integration status
*IntegrationsApi* | [**organizationsServersSitesIntegrationsOctaneStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsoctanestore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/octane | Create Laravel Octane integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsPulseDestroy**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationspulsedestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/pulse | Delete Laravel Pulse integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsPulseShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationspulseshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/pulse | Get Laravel Pulse integration status
*IntegrationsApi* | [**organizationsServersSitesIntegrationsPulseStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationspulsestore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/pulse | Create Laravel Pulse integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsReverbDestroy**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsreverbdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/integrations/reverb | Delete Laravel Reverb integration
*IntegrationsApi* | [**organizationsServersSitesIntegrationsReverbShow**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsreverbshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/integrations/reverb | Get Laravel Reverb integration status
*IntegrationsApi* | [**organizationsServersSitesIntegrationsReverbStore**](docs/Api/IntegrationsApi.md#organizationsserverssitesintegrationsreverbstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/integrations/reverb | Create Laravel Reverb integration
*LogsApi* | [**organizationsServersLogsDestroy**](docs/Api/LogsApi.md#organizationsserverslogsdestroy) | **DELETE** /orgs/{organization}/servers/{server}/logs/{key} | Delete server log content
*LogsApi* | [**organizationsServersLogsShow**](docs/Api/LogsApi.md#organizationsserverslogsshow) | **GET** /orgs/{organization}/servers/{server}/logs/{key} | Get server log content
*MonitorsApi* | [**organizationsServersMonitorsDestroy**](docs/Api/MonitorsApi.md#organizationsserversmonitorsdestroy) | **DELETE** /orgs/{organization}/servers/{server}/monitors/{monitor} | Delete server monitor
*MonitorsApi* | [**organizationsServersMonitorsIndex**](docs/Api/MonitorsApi.md#organizationsserversmonitorsindex) | **GET** /orgs/{organization}/servers/{server}/monitors | List server monitors
*MonitorsApi* | [**organizationsServersMonitorsShow**](docs/Api/MonitorsApi.md#organizationsserversmonitorsshow) | **GET** /orgs/{organization}/servers/{server}/monitors/{monitor} | Get server monitor
*MonitorsApi* | [**organizationsServersMonitorsStore**](docs/Api/MonitorsApi.md#organizationsserversmonitorsstore) | **POST** /orgs/{organization}/servers/{server}/monitors | Create server monitor
*NginxApi* | [**organizationsServersNginxTemplatesDestroy**](docs/Api/NginxApi.md#organizationsserversnginxtemplatesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/nginx/templates/{nginxTemplate} | Delete Nginx template
*NginxApi* | [**organizationsServersNginxTemplatesIndex**](docs/Api/NginxApi.md#organizationsserversnginxtemplatesindex) | **GET** /orgs/{organization}/servers/{server}/nginx/templates | List Nginx templates
*NginxApi* | [**organizationsServersNginxTemplatesShow**](docs/Api/NginxApi.md#organizationsserversnginxtemplatesshow) | **GET** /orgs/{organization}/servers/{server}/nginx/templates/{nginxTemplate} | Get Nginx template
*NginxApi* | [**organizationsServersNginxTemplatesStore**](docs/Api/NginxApi.md#organizationsserversnginxtemplatesstore) | **POST** /orgs/{organization}/servers/{server}/nginx/templates | Create Nginx template
*NginxApi* | [**organizationsServersNginxTemplatesUpdate**](docs/Api/NginxApi.md#organizationsserversnginxtemplatesupdate) | **PUT** /orgs/{organization}/servers/{server}/nginx/templates/{nginxTemplate} | Update Nginx template
*OrganizationsApi* | [**organizationsIndex**](docs/Api/OrganizationsApi.md#organizationsindex) | **GET** /orgs | List organizations
*OrganizationsApi* | [**organizationsServerCredentialsIndex**](docs/Api/OrganizationsApi.md#organizationsservercredentialsindex) | **GET** /orgs/{organization}/server-credentials | List server credentials
*OrganizationsApi* | [**organizationsServerCredentialsShow**](docs/Api/OrganizationsApi.md#organizationsservercredentialsshow) | **GET** /orgs/{organization}/server-credentials/{credential} | Get server credential
*OrganizationsApi* | [**organizationsServerCredentialsVpcsIndex**](docs/Api/OrganizationsApi.md#organizationsservercredentialsvpcsindex) | **GET** /orgs/{organization}/server-credentials/{credential}/regions/{region}/vpcs | List VPCs
*OrganizationsApi* | [**organizationsServerCredentialsVpcsShow**](docs/Api/OrganizationsApi.md#organizationsservercredentialsvpcsshow) | **GET** /orgs/{organization}/server-credentials/{credential}/regions/{region}/vpcs/{vpcId} | Get VPC
*OrganizationsApi* | [**organizationsServerCredentialsVpcsStore**](docs/Api/OrganizationsApi.md#organizationsservercredentialsvpcsstore) | **POST** /orgs/{organization}/server-credentials/{credential}/regions/{region}/vpcs | Create a new VPC
*OrganizationsApi* | [**organizationsShow**](docs/Api/OrganizationsApi.md#organizationsshow) | **GET** /orgs/{organization} | Get organization
*ProvidersApi* | [**providersIndex**](docs/Api/ProvidersApi.md#providersindex) | **GET** /providers | List providers
*ProvidersApi* | [**providersRegionsIndex**](docs/Api/ProvidersApi.md#providersregionsindex) | **GET** /providers/{provider}/regions | List provider regions
*ProvidersApi* | [**providersRegionsShow**](docs/Api/ProvidersApi.md#providersregionsshow) | **GET** /providers/{provider}/regions/{providerRegion} | Get provider region
*ProvidersApi* | [**providersRegionsSizesIndex**](docs/Api/ProvidersApi.md#providersregionssizesindex) | **GET** /providers/{provider}/regions/{providerRegion}/sizes | List provider region sizes
*ProvidersApi* | [**providersRegionsSizesShow**](docs/Api/ProvidersApi.md#providersregionssizesshow) | **GET** /providers/{provider}/regions/{providerRegion}/sizes/{providerSize} | Get provider region size
*ProvidersApi* | [**providersShow**](docs/Api/ProvidersApi.md#providersshow) | **GET** /providers/{provider} | Get provider
*ProvidersApi* | [**providersSizesIndex**](docs/Api/ProvidersApi.md#providerssizesindex) | **GET** /providers/{provider}/sizes | List provider sizes
*ProvidersApi* | [**providersSizesShow**](docs/Api/ProvidersApi.md#providerssizesshow) | **GET** /providers/{provider}/sizes/{providerSize} | Get provider size
*RecipesApi* | [**forgeRecipesIndex**](docs/Api/RecipesApi.md#forgerecipesindex) | **GET** /forge-recipes | List Forge's recipes
*RecipesApi* | [**forgeRecipesRunsStore**](docs/Api/RecipesApi.md#forgerecipesrunsstore) | **POST** /forge-recipes/{forgeRecipe}/runs | Create Forge recipe run
*RecipesApi* | [**forgeRecipesShow**](docs/Api/RecipesApi.md#forgerecipesshow) | **GET** /forge-recipes/{forgeRecipe} | Get Forge recipe
*RecipesApi* | [**organizationRecipesStore**](docs/Api/RecipesApi.md#organizationrecipesstore) | **POST** /orgs/{organization}/recipes | Create recipe
*RecipesApi* | [**organizationsRecipesDestroy**](docs/Api/RecipesApi.md#organizationsrecipesdestroy) | **DELETE** /orgs/{organization}/recipes/{recipe} | Delete recipe
*RecipesApi* | [**organizationsRecipesIndex**](docs/Api/RecipesApi.md#organizationsrecipesindex) | **GET** /orgs/{organization}/recipes | List organization recipes
*RecipesApi* | [**organizationsRecipesRunsIndex**](docs/Api/RecipesApi.md#organizationsrecipesrunsindex) | **GET** /orgs/{organization}/recipes/{recipe}/runs | List recipe runs
*RecipesApi* | [**organizationsRecipesRunsShow**](docs/Api/RecipesApi.md#organizationsrecipesrunsshow) | **GET** /orgs/{organization}/recipes/{recipe}/runs/{log} | Get recipe run
*RecipesApi* | [**organizationsRecipesRunsStore**](docs/Api/RecipesApi.md#organizationsrecipesrunsstore) | **POST** /orgs/{organization}/recipes/{recipe}/runs | Create recipe run
*RecipesApi* | [**organizationsRecipesShow**](docs/Api/RecipesApi.md#organizationsrecipesshow) | **GET** /orgs/{organization}/recipes/{recipe} | Get recipe
*RecipesApi* | [**organizationsRecipesUpdate**](docs/Api/RecipesApi.md#organizationsrecipesupdate) | **PUT** /orgs/{organization}/recipes/{recipe} | Update recipe
*RedirectRulesApi* | [**organizationsServersSitesRedirectRulesDestroy**](docs/Api/RedirectRulesApi.md#organizationsserverssitesredirectrulesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules/{redirectRule} | Delete site redirect rule
*RedirectRulesApi* | [**organizationsServersSitesRedirectRulesIndex**](docs/Api/RedirectRulesApi.md#organizationsserverssitesredirectrulesindex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules | List site redirect rules
*RedirectRulesApi* | [**organizationsServersSitesRedirectRulesShow**](docs/Api/RedirectRulesApi.md#organizationsserverssitesredirectrulesshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules/{redirectRule} | Get site redirect rule
*RedirectRulesApi* | [**organizationsServersSitesRedirectRulesStore**](docs/Api/RedirectRulesApi.md#organizationsserverssitesredirectrulesstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/redirect-rules | Create site redirect rule
*RolesApi* | [**organizationsRolesDestroy**](docs/Api/RolesApi.md#organizationsrolesdestroy) | **DELETE** /orgs/{organization}/roles/{role} | Delete role
*RolesApi* | [**organizationsRolesIndex**](docs/Api/RolesApi.md#organizationsrolesindex) | **GET** /orgs/{organization}/roles | List roles
*RolesApi* | [**organizationsRolesPermissionsIndex**](docs/Api/RolesApi.md#organizationsrolespermissionsindex) | **GET** /orgs/{organization}/roles/{role}/permissions | List role permissions
*RolesApi* | [**organizationsRolesShow**](docs/Api/RolesApi.md#organizationsrolesshow) | **GET** /orgs/{organization}/roles/{role} | Get role
*RolesApi* | [**organizationsRolesStore**](docs/Api/RolesApi.md#organizationsrolesstore) | **POST** /orgs/{organization}/roles | Create role
*RolesApi* | [**organizationsRolesUpdate**](docs/Api/RolesApi.md#organizationsrolesupdate) | **PUT** /orgs/{organization}/roles/{role} | Update role
*SSHKeysApi* | [**organizationsServersKeyShow**](docs/Api/SSHKeysApi.md#organizationsserverskeyshow) | **GET** /orgs/{organization}/servers/{server}/key | Get server public SSH key
*SSHKeysApi* | [**organizationsServersSshKeysDestroy**](docs/Api/SSHKeysApi.md#organizationsserverssshkeysdestroy) | **DELETE** /orgs/{organization}/servers/{server}/ssh-keys/{key} | Delete server SSH key
*SSHKeysApi* | [**organizationsServersSshKeysIndex**](docs/Api/SSHKeysApi.md#organizationsserverssshkeysindex) | **GET** /orgs/{organization}/servers/{server}/ssh-keys | List server SSH keys
*SSHKeysApi* | [**organizationsServersSshKeysShow**](docs/Api/SSHKeysApi.md#organizationsserverssshkeysshow) | **GET** /orgs/{organization}/servers/{server}/ssh-keys/{key} | Get server SSH key
*SSHKeysApi* | [**organizationsServersSshKeysStore**](docs/Api/SSHKeysApi.md#organizationsserverssshkeysstore) | **POST** /orgs/{organization}/servers/{server}/ssh-keys | Create server SSH key
*ScheduledJobsApi* | [**organizationsServersScheduledJobsDestroy**](docs/Api/ScheduledJobsApi.md#organizationsserversscheduledjobsdestroy) | **DELETE** /orgs/{organization}/servers/{server}/scheduled-jobs/{job} | Delete scheduled job
*ScheduledJobsApi* | [**organizationsServersScheduledJobsIndex**](docs/Api/ScheduledJobsApi.md#organizationsserversscheduledjobsindex) | **GET** /orgs/{organization}/servers/{server}/scheduled-jobs | List server scheduled jobs
*ScheduledJobsApi* | [**organizationsServersScheduledJobsOutputsShow**](docs/Api/ScheduledJobsApi.md#organizationsserversscheduledjobsoutputsshow) | **GET** /orgs/{organization}/servers/{server}/scheduled-jobs/{job}/output | Get scheduled job output
*ScheduledJobsApi* | [**organizationsServersScheduledJobsShow**](docs/Api/ScheduledJobsApi.md#organizationsserversscheduledjobsshow) | **GET** /orgs/{organization}/servers/{server}/scheduled-jobs/{job} | Get scheduled job
*ScheduledJobsApi* | [**organizationsServersScheduledJobsStore**](docs/Api/ScheduledJobsApi.md#organizationsserversscheduledjobsstore) | **POST** /orgs/{organization}/servers/{server}/scheduled-jobs | Create scheduled job
*SecurityRulesApi* | [**organizationsServersSitesSecurityRulesDestroy**](docs/Api/SecurityRulesApi.md#organizationsserverssitessecurityrulesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site}/security-rules/{securityRule} | Delete site security rule
*SecurityRulesApi* | [**organizationsServersSitesSecurityRulesIndex**](docs/Api/SecurityRulesApi.md#organizationsserverssitessecurityrulesindex) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/security-rules | List site security rules
*SecurityRulesApi* | [**organizationsServersSitesSecurityRulesShow**](docs/Api/SecurityRulesApi.md#organizationsserverssitessecurityrulesshow) | **GET** /orgs/{organization}/servers/{server}/sites/{site}/security-rules/{securityRule} | Get site security rule
*SecurityRulesApi* | [**organizationsServersSitesSecurityRulesStore**](docs/Api/SecurityRulesApi.md#organizationsserverssitessecurityrulesstore) | **POST** /orgs/{organization}/servers/{server}/sites/{site}/security-rules | Create site security rule
*SecurityRulesApi* | [**organizationsServersSitesSecurityRulesUpdate**](docs/Api/SecurityRulesApi.md#organizationsserverssitessecurityrulesupdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site}/security-rules/{securityRule} | Update site security rule
*ServersApi* | [**organizationsServersActionsStore**](docs/Api/ServersApi.md#organizationsserversactionsstore) | **POST** /orgs/{organization}/servers/{server}/actions | Create server action
*ServersApi* | [**organizationsServersDestroy**](docs/Api/ServersApi.md#organizationsserversdestroy) | **DELETE** /orgs/{organization}/servers/{server} | Delete server
*ServersApi* | [**organizationsServersEventsIndex**](docs/Api/ServersApi.md#organizationsserverseventsindex) | **GET** /orgs/{organization}/servers/{server}/events | List server events
*ServersApi* | [**organizationsServersIndex**](docs/Api/ServersApi.md#organizationsserversindex) | **GET** /orgs/{organization}/servers | List servers
*ServersApi* | [**organizationsServersShow**](docs/Api/ServersApi.md#organizationsserversshow) | **GET** /orgs/{organization}/servers/{server} | Get server
*ServersApi* | [**organizationsServersStore**](docs/Api/ServersApi.md#organizationsserversstore) | **POST** /orgs/{organization}/servers | Create server
*SitesApi* | [**organizationsServersSitesDestroy**](docs/Api/SitesApi.md#organizationsserverssitesdestroy) | **DELETE** /orgs/{organization}/servers/{server}/sites/{site} | Delete site
*SitesApi* | [**organizationsServersSitesIndex**](docs/Api/SitesApi.md#organizationsserverssitesindex) | **GET** /orgs/{organization}/servers/{server}/sites | List sites for server
*SitesApi* | [**organizationsServersSitesStore**](docs/Api/SitesApi.md#organizationsserverssitesstore) | **POST** /orgs/{organization}/servers/{server}/sites | Create site
*SitesApi* | [**organizationsServersSitesUpdate**](docs/Api/SitesApi.md#organizationsserverssitesupdate) | **PUT** /orgs/{organization}/servers/{server}/sites/{site} | Update site
*SitesApi* | [**organizationsSitesIndex**](docs/Api/SitesApi.md#organizationssitesindex) | **GET** /orgs/{organization}/sites | List sites for Organization
*SitesApi* | [**sitesIndex**](docs/Api/SitesApi.md#sitesindex) | **GET** /sites | List sites
*StorageProvidersApi* | [**organizationsStorageProvidersDestroy**](docs/Api/StorageProvidersApi.md#organizationsstorageprovidersdestroy) | **DELETE** /orgs/{organization}/storage-providers/{storageConfiguration} | Delete storage provider
*StorageProvidersApi* | [**organizationsStorageProvidersIndex**](docs/Api/StorageProvidersApi.md#organizationsstorageprovidersindex) | **GET** /orgs/{organization}/storage-providers | List storage providers
*StorageProvidersApi* | [**organizationsStorageProvidersShow**](docs/Api/StorageProvidersApi.md#organizationsstorageprovidersshow) | **GET** /orgs/{organization}/storage-providers/{storageConfiguration} | Get storage provider
*StorageProvidersApi* | [**organizationsStorageProvidersStore**](docs/Api/StorageProvidersApi.md#organizationsstorageprovidersstore) | **POST** /orgs/{organization}/storage-providers | Create storage provider
*StorageProvidersApi* | [**organizationsStorageProvidersUpdate**](docs/Api/StorageProvidersApi.md#organizationsstorageprovidersupdate) | **PUT** /orgs/{organization}/storage-providers/{storageConfiguration} | Update storage provider
*TeamsApi* | [**organizationsTeamsDestroy**](docs/Api/TeamsApi.md#organizationsteamsdestroy) | **DELETE** /orgs/{organization}/teams/{team} | Delete team
*TeamsApi* | [**organizationsTeamsIndex**](docs/Api/TeamsApi.md#organizationsteamsindex) | **GET** /orgs/{organization}/teams | List teams
*TeamsApi* | [**organizationsTeamsShow**](docs/Api/TeamsApi.md#organizationsteamsshow) | **GET** /orgs/{organization}/teams/{team} | Get team
*TeamsApi* | [**organizationsTeamsStore**](docs/Api/TeamsApi.md#organizationsteamsstore) | **POST** /orgs/{organization}/teams | Create team
*TeamsApi* | [**organizationsTeamsUpdate**](docs/Api/TeamsApi.md#organizationsteamsupdate) | **PUT** /orgs/{organization}/teams/{team} | Update team
*UserApi* | [**me**](docs/Api/UserApi.md#me) | **GET** /me | Get user
*UserApi* | [**userShow**](docs/Api/UserApi.md#usershow) | **GET** /user | Get user

## Available API Classes

| Class | Description |
|-------|-------------|
| `BackgroundProcessesApi` | Manage daemons/supervisor processes |
| `BackupsApi` | Database backup management |
| `CommandsApi` | Execute commands on sites |
| `DatabasesApi` | Database and user management |
| `DeploymentsApi` | Deployment management |
| `FirewallRulesApi` | Firewall rule management |
| `IntegrationsApi` | Laravel integrations (Horizon, Octane, etc.) |
| `LogsApi` | Server log management |
| `MonitorsApi` | Server monitoring |
| `NginxApi` | Nginx template management |
| `OrganizationsApi` | Organization management |
| `ProvidersApi` | Cloud provider information |
| `RecipesApi` | Automation recipes |
| `RedirectRulesApi` | Redirect rule management |
| `RolesApi` | Role and permission management |
| `SSHKeysApi` | SSH key management |
| `ScheduledJobsApi` | Cron job management |
| `SecurityRulesApi` | Security rule management |
| `ServerCredentialsApi` | Server credential management |
| `ServersApi` | Server management |
| `SitesApi` | Site management |
| `StorageProvidersApi` | Storage provider management |
| `TeamsApi` | Team management |
| `UserApi` | Current user information |

## Error Handling

```php
use Dimer47\LaravelForgeSdk\ApiException;

try {
    $server = $serversApi->organizationsServersShow('my-org', 999999);
} catch (ApiException $e) {
    echo "Error: " . $e->getMessage() . "\n";
    echo "Status Code: " . $e->getCode() . "\n";
    echo "Response Body: " . $e->getResponseBody() . "\n";

    // Get response headers
    $headers = $e->getResponseHeaders();
}
```

## Rate Limiting

Laravel Forge API has a rate limit of 60 requests per minute. The SDK does not handle rate limiting automatically. Consider implementing retry logic:

```php
use Dimer47\LaravelForgeSdk\ApiException;

function withRetry(callable $callback, int $maxRetries = 3)
{
    $attempts = 0;

    while ($attempts < $maxRetries) {
        try {
            return $callback();
        } catch (ApiException $e) {
            if ($e->getCode() === 429) {
                $attempts++;
                sleep(60); // Wait 1 minute
                continue;
            }
            throw $e;
        }
    }

    throw new \RuntimeException('Max retries exceeded');
}

$servers = withRetry(fn() => $serversApi->organizationsServersIndex('my-org'));
```

## Laravel Integration

For Laravel projects, you can create a service provider:

```php
// app/Providers/ForgeServiceProvider.php
namespace App\Providers;

use Illuminate\Support\ServiceProvider;
use Dimer47\LaravelForgeSdk\Configuration;
use Dimer47\LaravelForgeSdk\Api\ServersApi;
use Dimer47\LaravelForgeSdk\Api\SitesApi;

class ForgeServiceProvider extends ServiceProvider
{
    public function register()
    {
        $this->app->singleton(Configuration::class, function () {
            return Configuration::getDefaultConfiguration()
                ->setAccessToken(config('services.forge.token'));
        });

        $this->app->bind(ServersApi::class, function ($app) {
            return new ServersApi(null, $app->make(Configuration::class));
        });

        $this->app->bind(SitesApi::class, function ($app) {
            return new SitesApi(null, $app->make(Configuration::class));
        });
    }
}
```

Then use it:

```php
// In a controller or command
public function __construct(private ServersApi $serversApi) {}

public function index()
{
    $servers = $this->serversApi->organizationsServersIndex('my-org');
}
```

## Authorization

Authentication schemes defined for the API:

### Bearer Token (http)

- **Type**: Bearer authentication

### OAuth2

- **Type**: `OAuth`
- **Flow**: `accessCode`
- **Authorization URL**: `https://forge.laravel.com/oauth/authorize`

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Contributing

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Security

If you discover any security-related issues, please use the issue tracker.

## Credits

- [Dimitri Iachi](https://github.com/dimer47)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `0.0.1`
- Generator version: `7.19.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
