# # OrganizationsServersStoreRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  |
**provider** | **string** |  |
**credential_id** | **string** |  | [optional]
**team_id** | **int** |  | [optional]
**type** | [**\Dimer47\Model\ServerType**](ServerType.md) |  |
**ubuntu_version** | **string** |  |
**php_version** | **string** |  | [optional]
**database_type** | **string** |  | [optional]
**recipe_id** | **int** |  | [optional]
**tags** | **string[]** |  | [optional]
**aws** | [**\Dimer47\Model\CreateServerRequestAws**](CreateServerRequestAws.md) |  | [optional]
**ocean2** | [**\Dimer47\Model\CreateServerRequestOcean2**](CreateServerRequestOcean2.md) |  | [optional]
**hetzner** | [**\Dimer47\Model\OrganizationsServersStoreRequestAllOfHetzner**](OrganizationsServersStoreRequestAllOfHetzner.md) |  | [optional]
**vultr** | [**\Dimer47\Model\CreateServerRequestVultr**](CreateServerRequestVultr.md) |  | [optional]
**akamai** | [**\Dimer47\Model\CreateServerRequestAkamai**](CreateServerRequestAkamai.md) |  | [optional]
**laravel** | [**\Dimer47\Model\OrganizationsServersStoreRequestAllOfLaravel**](OrganizationsServersStoreRequestAllOfLaravel.md) |  | [optional]
**custom** | [**\Dimer47\Model\CreateServerRequestCustom**](CreateServerRequestCustom.md) |  | [optional]
**add_key_to_source_control** | **bool** |  | [optional] [default to true]
**database** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
