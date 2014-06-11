vim.alarm.AndAlarmExpression
============================
inherits from [vim.alarm.AlarmExpression](docs/vim.alarm.AlarmExpression.md)


A data object type that links multiple alarm expressions with AND operators.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| expression | [vim.alarm.AlarmExpression](vim.alarm.AlarmExpression.md "vim.alarm.AlarmExpression") | None | None | List of alarm expressions that define the overall status of the alarm.   <p>   <ul>   <li>The state of the alarm expression is gray if all subexpressions are gray.       Otherwise, gray subexpressions are ignored.   <li>The state is red if all subexpressions are red.   <li>Otherwise, the state is yellow if all subexpressions are red or yellow.   <li>Otherwise, the state of the alarm expression is green.   </ul> |


