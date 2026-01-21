# # CreateScheduledJobRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the command. | [optional]
**command** | **string** | The command to run. |
**user** | **string** | The user to run the scheduled job as. |
**frequency** | [**\Dimer47\Model\CronFrequency**](CronFrequency.md) | The frequency of the scheduled job. |
**cron** | **string** | The cron expression to use for the scheduled job. Only used if frequency is set to Custom. | [optional]
**heartbeat** | **bool** | Whether a heartbeat should be created for the scheduled job. | [optional]
**grace_period** | **string** | The grace period, in minutes, for the heartbeat. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
