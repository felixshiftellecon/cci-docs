# Review Each Workflow for Improvement Opportunities

## 1) Review Job Placement

[Job](https://circleci.com/docs/glossary/#job) order can be the largest impact on [workflow](https://circleci.com/docs/glossary/#workflow) duration. Review the workflow for opportunities to [run jobs in parallel](https://circleci.com/docs/workflows/#fan-outfan-in-workflow) and note which jobs are bottlenecking the workflow to review them for improvement opportunities.

Placing shorter jobs, like linters, in the beginning of the workflow is helpful in reducing the time to receive feedback about a change being tested. This saves [credits](https://circleci.com/docs/credits/) and time as a large portion of the workflow doesn't need to run to receive feedback about a small issue.

## 2) Identify Modular Configuration Opportunities

When reviewing workflows that fan out but never fan back in, see if the jobs could be grouped into separate workflows. Having multiple workflows provides the separation needed to take advantage of [dynamic config](https://circleci.com/docs/dynamic-config/), which allows workflows to be triggered based on parameters set in a setup workflow. [Workflows and jobs can then be conditionally run](https://support.circleci.com/hc/en-us/articles/360043638052-Conditional-steps-in-jobs-and-conditional-workflows), saving time and credits.

Creating [parameterized jobs](https://circleci.com/docs/reusing-config/#authoring-parameterized-jobs) allows for further implementation of dynamic config and leads an easier to manage config in most cases. Those jobs can also be used to create matrix jobs.

[Self Service Configuration Review](self_service_config_review.md)
1. [Configuration Review Preparation](review_preparation/review_preparation.md)
    - [Document the Config Review](review_preparation/document_review.md)
    - [Review CircleCI Features](review_preparation/review_features.md)
    - [Snapshot Project Metrics](review_preparation/snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](job_review/job_review.md)
    - [General Job Opportunities](job_review/general_opportunities.md)
    - [Execution Environment Opportunities](job_review/execution_environment.md)
    - [Opportunities for Jobs with High Duration](job_review/high_duration.md)
3. \>\>[Review Each Workflow for Improvement Opportunities](workflow_review/workflow_review.md)<<
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
