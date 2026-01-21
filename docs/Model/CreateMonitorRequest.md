# # CreateMonitorRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**\Dimer47\Model\MonitorMetricType**](MonitorMetricType.md) | The type of the monitor. |
**operator** | [**\Dimer47\Model\MonitorOperator**](MonitorOperator.md) | The operator used against the threshold. |
**threshold** | **float** | The threshold to alert on once breached. |
**minutes** | **int** | The frequency in minutes to evaluate the monitor. | [optional]
**notify** | **string** | The email address to notify when the monitor is in an alert state. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
