vim.cluster.DrsRecommendation
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
### DEPRECATED



DrsRecommendation describes a recommendation to migrate    one or more virtual machines.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key to identify the recommendation when calling applyRecommendation. |
| rating | int | None | None | A rating of the recommendation.   Valid values range from 1 (lowest confidence) to 5 (highest confidence). |
| reason | string | None | None | A reason code explaining why this set of migrations is being suggested. |
| reasonText | string | None | None | Text that provides more information about the reason code for the suggested   set of migrations. |
| migrationList | [vim.cluster.DrsMigration](vim.cluster.DrsMigration.md "vim.cluster.DrsMigration") | None | None |  |


