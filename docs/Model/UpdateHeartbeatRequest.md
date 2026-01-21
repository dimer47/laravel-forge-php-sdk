# # UpdateHeartbeatRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the heartbeat. |
**grace_period** | [**\Dimer47\Model\HeartbeatGracePeriod**](HeartbeatGracePeriod.md) | The duration (in minutes) after which a heartbeat is considered missing. |
**frequency** | [**\Dimer47\Model\HeartbeatFrequency**](HeartbeatFrequency.md) | The interval (in minutes) at which the client is expected to send a ping. |
**custom_frequency** | **string** | A cron expression representing the custom frequency at which the client is expected to send a ping, if the frequency is set to -1. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
