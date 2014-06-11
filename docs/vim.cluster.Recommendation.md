vim.cluster.Recommendation
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Recommendation is the base class for any packaged group of    actions that are intended to take the system from one    state to another one.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key to identify the recommendation when calling applyRecommendation. |
| type | string | None | None | Type of the recommendation. This differentiates between various  of recommendations aimed at achieving different goals. |
| time | datetime | None | None | The time this recommendation was computed. |
| rating | int | None | None | A rating of the recommendation.   Valid values range from 1 (lowest confidence) to 5 (highest confidence). |
| reason | string | None | None | A reason code explaining why this set of migrations is being suggested. |
| reasonText | string | None | None | Text that provides more information about the reason code for the suggested  set of migrations. |
| prerequisite | string | true | None | This recommendation may depend on some other recommendations.  The prerequisite recommendations are listed by their keys. |
| action | [vim.cluster.Action](vim.cluster.Action.md "vim.cluster.Action") | true | None | List of actions that are executed as part of this recommendation |
| target | vim.ExtensibleManagedObject | true | None | The target object of this recommendation. |


