# # CreateSiteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**\Dimer47\Model\SiteType**](SiteType.md) |  |
**domain_mode** | [**\Dimer47\Model\CreateSiteRequestDomainMode**](CreateSiteRequestDomainMode.md) |  | [optional]
**name** | **string** |  | [optional]
**www_redirect_type** | **string** |  | [optional]
**allow_wildcard_subdomains** | **string** |  | [optional]
**root_directory** | **string** |  | [optional]
**web_directory** | **string** |  | [optional]
**is_isolated** | **bool** |  | [optional]
**isolated_user** | **string** |  | [optional]
**php_version** | [**\Dimer47\Model\PhpVersion**](PhpVersion.md) |  | [optional]
**zero_downtime_deployments** | **bool** |  | [optional]
**nginx_template_id** | **int** |  | [optional]
**source_control_provider** | [**\Dimer47\Model\SourceControlProvider**](SourceControlProvider.md) |  | [optional]
**repository** | **string** |  | [optional]
**branch** | **string** |  | [optional]
**database_id** | **int** |  | [optional]
**database_user_id** | **string** |  | [optional]
**statamic_setup** | **string** | The type of setup for Statmic apps. | [optional]
**statamic_starter_kit** | **string** | The starter kit for the Statamic app. | [optional]
**statamic_super_user_email** | **string** |  | [optional]
**statamic_super_user_password** | **string** |  | [optional]
**install_composer_dependencies** | **bool** |  | [optional]
**generate_deploy_key** | **bool** |  | [optional]
**public_deploy_key** | **string** |  | [optional]
**private_deploy_key** | **string** |  | [optional]
**frontend_package_manager** | **string** | The package manager for frontend applications. | [optional]
**frontend_build_command** | **string** | The build command for frontend assets. | [optional]
**nuxt_next_mode** | **string** | The render mode for Next/Nuxt applications. | [optional]
**nuxt_next_port** | **int** | The port used for Next/Nuxt applications. | [optional]
**push_to_deploy** | **bool** | Automatically trigger a new deployment when changes are pushed to the environment&#39;s Git branch. | [optional] [default to false]
**tags** | **string[]** |  | [optional]
**shared_paths** | [**\Dimer47\Model\CreateSiteRequestSharedPathsInner[]**](CreateSiteRequestSharedPathsInner.md) | A list of files or directories to be shared between releases for zero-downtime deployments. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
