# Snapshot Project Metrics

## 1) Gather Project Metrics

The UI can be used to gather metrics, but when doing multiple config reviews it is helpful to write a script that uses the CircleCI API. There are many Insights endpoints available to choose from, but a good place to start is the [project summary endpoint](https://circleci.com/docs/api/v2/index.html#operation/getProjectWorkflowsPageData) which provides metrics down to the branch level for workflows in the project.

## 2) Separate Out Significant Branches

Metrics for all branches can be useful but for certain metrics, like success rate or mean time to recovery, it is helpful to separate out metrics for important branches. Branches such as main, staging, qa, etc have different expectations so metric goals will be different as well. The [project summary endpoint](https://circleci.com/docs/api/v2/index.html#operation/getProjectWorkflowsPageData) can be filtered to show specific branches.

## Example API script

<!-- insert bash script here -->

---

[Self Service Configuration Review](self_service_config_review.md)

1. [Configuration Review Preparation](review_preparation.md)
    - [Document the Config Review](document_review.md)
    - [Review CircleCI Features](review_features.md)
    - \>\>[Snapshot Project Metrics](snapshot_metrics.md)<<
2. [Review Each Job for Improvement Opportunities](job_review/job_review.md)
    - [General Job Opportunities](job_review/general_opportunities.md)
    - [Execution Environment Opportunities](job_review/execution_environment.md)
    - [Opportunities for Jobs with High Duration](job_review/high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](workflow_review/workflow_review.md)
4. [High Level Improvement Opportunities](high_level_recommendations/high_level_recommendations.md)
    - [Inside the Config](high_level_recommendations/inside_config/inside_config.md)
        - [Config Security](high_level_recommendations/inside_config/config_security.md)
        - [Reusable Config](high_level_recommendations/inside_config/reusable_config.md)
        - [Dynamic Config](high_level_recommendations/inside_config/dynamic_config.md)
    - [Outside the Config](high_level_recommendations/outside_config/outside_config.md)
        - [Security Settings](high_level_recommendations/outside_config/security_settings.md)
        - [Secret Management](high_level_recommendations/outside_config/secret_management.md)
        - [Storage Usage](high_level_recommendations/outside_config/storage_usage.md)
        - [Project Settings](high_level_recommendations/outside_config/project_settings.md)
5. [Finalize Review](finalize_review/finalize_review.md)