vim.alarm.StateAlarmExpression
==============================
inherits from [vim.alarm.AlarmExpression](docs/vim.alarm.AlarmExpression.md)


An alarm expression that uses the running state of either a virtual machine or   a host as the condition that triggers the alarm. Base type.   <p>   There are two alarm operands: yellow and red. At least one of them   must be set. The value of the alarm expression is determined as follows:   <ul>   <li>If the red state is set but the yellow state is not: the expression is red when   the state operand matches (isEqual operator) or does not match (isUnequal operator)   the state of the managed entity. The expression is green otherwise.   <li>If yellow is set but red is not: the expression is yellow when   the state operand matches (isEqual) or does not match (isUnequal)   the state of the managed entity. The expression is green otherwise.   <li>If both yellow and red are set, the value of the expression is red when   the red state operand matches (isEqual) or does not match (isUnequal)   the state of the managed entity. Otherwise, the expression is   yellow when the yellow state operand matches (isEqual) or does not match (isUnequal)   the state of the managed entity. Otherwise, the expression is green.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operator | [vim.alarm.StateAlarmExpression.StateOperator](vim.alarm.StateAlarmExpression.StateOperator.md "vim.alarm.StateAlarmExpression.StateOperator") | None | None | The operation to be tested on the target state. |
| type | string | None | None | Name of the object type containing the property. |
| statePath | string | None | None | Path of the state property.  <p>  The supported values:  <ul>  <li>for vim.VirtualMachine type:  <li>  runtime.powerState or summary.quickStats.guestHeartbeatStatus  <li>for vim.HostSystem type: runtime.connectionState  </ul> |
| yellow | string | true | None | Whether or not to test for a yellow condition.   If this property is not set, do not calculate yellow status. |
| red | string | true | None | Whether or not to test for a red condition.   If this property is not set, do not calculate red status. |


