# # MonitorResourceAttributes

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**\Dimer47\Model\MonitorMetricType**](MonitorMetricType.md) | The type of the monitor. |
**operator** | [**\Dimer47\Model\MonitorOperator**](MonitorOperator.md) | The operator used against the threshold. |
**threshold** | **float** | The threshold to alert on once breached. |
**minutes** | **int** | The frequency in minutes to evaluate the monitor. |
**notify** | **string** | The email address to notify when the monitor is in an alert state. |
**status** | [**\Dimer47\Model\ResourceState**](ResourceState.md) | The status of the monitor. |
**state** | [**\Dimer47\Model\MonitorState**](MonitorState.md) | The state of the monitor. |
**state_changed_at** | **\DateTime** | The date and time the monitor state was last changed. |
**created_at** | **\DateTime** | The date and time the monitor was created. |
**updated_at** | **\DateTime** | The date and time the monitor was last updated. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
