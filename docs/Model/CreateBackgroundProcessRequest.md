# # CreateBackgroundProcessRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the background process. |
**command** | **string** | The command to run. |
**user** | **string** | The user to run the background process as. |
**directory** | **string** | The directory to run the background process from. | [optional]
**processes** | **int** | The number of processes to run. |
**startsecs** | **int** | The number of seconds to wait before starting the process. | [optional]
**stopwaitsecs** | **int** | The number of seconds to wait before stopping the process. | [optional]
**stopsignal** | **string** | The signal to send to stop the process. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
