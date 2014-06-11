vim.alarm.MetricAlarmExpression
===============================
inherits from [vim.alarm.AlarmExpression](docs/vim.alarm.AlarmExpression.md)


An alarm expression that uses a metric as the condition that triggers an   alarm. Base type.   <p>   There are two alarm operands: yellow and red. At least one of them   must be set. The value of the alarm expression is determined as follows:   <ul>   <li>If the host is not connected, the host metric expression is gray.   <li>If the vm is not connected, the vm metric expression is gray.   <li>If red is set but yellow is not, the expression is red when   the metric is over (isAbove operator) or under (isBelow operator)   the red value. Otherwise, the expression is green.   <li>If yellow is set but red is not, the expression is yellow when   the metric is over (isAbove) or under (isBelow)   the yellow value. Otherwise, the expression is green.   <li>If both yellow and red are set, the value of the expression is red   when the metric is over (isAbove) or under (isBelow) the red value.   Otherwise, the expression is yellow when the metric is over (isAbove)   or under (isBelow) the yellow value. Otherwise, the expression is green.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operator | [vim.alarm.MetricAlarmExpression.MetricOperator](vim.alarm.MetricAlarmExpression.MetricOperator.md "vim.alarm.MetricAlarmExpression.MetricOperator") | None | None | The operation to be tested on the metric. |
| type | string | None | None | Name of the object type containing the property. |
| metric | [vim.PerformanceManager.MetricId](vim.PerformanceManager.MetricId.md "vim.PerformanceManager.MetricId") | None | None | The instance of the metric. |
| yellow | int | true | None | Whether or not to test for a yellow condition.   If not set, do not calculate yellow status.   If set, it contains the threshold value that triggers yellow status. |
| yellowInterval | int | true | None | Time interval in seconds for which the yellow condition must be true  before the yellow status is triggered. If unset, the yellow status is  triggered immediately when the yellow condition becomes true. |
| red | int | true | None | Whether or not to test for a red condition.   If not set, do not calculate red status.   If set, it contains the threshold value that triggers red status. |
| redInterval | int | true | None | Time interval in seconds for which the red condition must be true  before the red status is triggered. If unset, the red status is  triggered immediately when the red condition becomes true. |


