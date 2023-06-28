# Execution Environment Opportunities

## 1) Resource Allocation

Optimizing the [resource classes](https://circleci.com/docs/glossary/#resource-class) of your [jobs](https://circleci.com/docs/glossary/#job) is an easy way to ensure [credits](https://circleci.com/docs/credits/) aren't being wasted. Each job has a resource tab in the UI showing the resource usage throughout the job, which is useful while reviewing jobs individually. [CircleCI's Insights UI](https://circleci.com/docs/resource-class-overview/#resource-class-insights) offers a view of historical usage for every job in a [workflow](https://circleci.com/docs/glossary/#workflow) which is more helpful when doing a config review.

A good rule of thumb is a job should be using 50% - 75% of its resources. If a job is outside of that band try out one of the other resource classes for the [execution environment being used](https://circleci.com/product/features/resource-classes/).

## 2) Runner

[Runners](https://circleci.com/docs/runner-overview/) are useful when a job needs to access data from an internal source or has many dependencies that need to be set up. Those types of jobs can be hard to manage on a CircleCI cloud execution environment and may not be secure. Runner allows you to customize the environment your job is running in and run the job on your own infrastructure which helps support these jobs. Runners do need to be maintained so be sure to take that into account when considering implementing them.

---

---

### Table of Contents

[Self Service Configuration Review](../self_service_config_review.md)

1. [Configuration Review Preparation](../review_preparation/review_preparation.md)
    - [Document the Config Review](../review_preparation/document_review.md)
    - [Review CircleCI Features](../review_preparation/review_features.md)
    - [Snapshot Project Metrics](../review_preparation/snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](job_review.md)
    - [General Job Opportunities](general_opportunities.md)
    - \>\>[Execution Environment Opportunities](execution_environment.md)<<
    - [Opportunities for Jobs with High Duration](high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](../workflow_review/workflow_review.md)
4. [High Level Improvement Opportunities](../high_level_recommendations/high_level_recommendations.md)
    - [Inside the Config](../high_level_recommendations/inside_config/inside_config.md)
        - [Config Security](../high_level_recommendations/inside_config/config_security.md)
        - [Reusable Config](../high_level_recommendations/inside_config/reusable_config.md)
        - [Dynamic Config](../high_level_recommendations/inside_config/dynamic_config.md)
    - [Outside the Config](../high_level_recommendations/outside_config/outside_config.md)
        - [Security Settings](../high_level_recommendations/outside_config/security_settings.md)
        - [Secret Management](../high_level_recommendations/outside_config/secret_management.md)
        - [Storage Usage](../high_level_recommendations/outside_config/storage_usage.md)
        - [Project Settings](../high_level_recommendations/outside_config/project_settings.md)
5. [Finalize Review](../finalize_review/finalize_review.md)
