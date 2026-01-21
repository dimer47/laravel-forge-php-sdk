# # EnableMaintenanceModeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**secret** | **string** | The secret phrase that allows access to the application while in maintenance mode. | [optional]
**status** | [**\Dimer47\Model\MaintenanceModeStatusCode**](MaintenanceModeStatusCode.md) | The HTTP status code that should be returned while in maintenance mode. |
**redirect** | **string** | The redirect URL to which all requests should be sent while in maintenance mode. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
