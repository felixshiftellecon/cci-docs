# Snapshot Project Metrics

## 1) Gather Project Metrics

The UI can be usd to gather metrics, but when doing multiple config reviews it is helpful to write a script that uses the CircleCI API. There are many Insights endpoints available to choose from, but a good place to start is the [project summary endpoint](https://circleci.com/docs/api/v2/index.html#operation/getProjectWorkflowsPageData) which provides metrics down to the branch level for a workflow.

## 2) Separate Out Significant Branches

Metrics for all branches can be useful but for certain metrics, like success rate or mean time to recovery, it is helpful to separate out metrics for important branches. Branches such as main, staging, qa, etc have different expectations so metric goals will be different as well. The [project summary endpoint](https://circleci.com/docs/api/v2/index.html#operation/getProjectWorkflowsPageData) can be filters to show specific branches.

## Example API script

<!-- insert bash script here -->