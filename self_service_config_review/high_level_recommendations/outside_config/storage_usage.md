# Storage Usage

## Caching

Inspect the output of [caching steps](https://circleci.com/docs/caching/) in [jobs](https://circleci.com/docs/glossary/#job) to ensure cache keys are regularly being found. If not, consider changing the cache key to be less specific or use a [fallback key](https://circleci.com/docs/caching-strategy/#partial-dependency-caching-strategies).

For caching steps that are taking a long time, consider breaking up the cache into multiple caches. If the job is on the docker executor, consider enabling [RAM disk](https://circleci.com/docs/using-docker/#ram-disks) to speed up I/O operations.

## Workspaces

Ensure data being added to a [workspace](https://circleci.com/docs/glossary/#workspace) is being used downstream and is accessible.

For workspace steps that are taking a long time, analyze the data for anything unnecessary. If the job is on the docker executor, consider enabling RAM disk to speed up I/O operations.

## Artifacts

Review how [artifacts](https://circleci.com/docs/artifacts/) are used by the team that works in the project and see if adding or removing them would be helpful.

In most cases if artifacts are uploaded to cloud storage, like an s3 bucket, they do not also need to be stored in CircleCI.

## Usage Controls

Most organizations can benefit from reducing the default [storage retention](https://circleci.com/docs/persist-data) periods without seeing impact, which can save some [credits](https://circleci.com/docs/credits/). The common recommendation is below but should be adjusted based on use case and user feedback.

| Setting     | CircleCI Default   | Recommendation |
|-------------|--------------------|--------------------|
| Artifacts   | 30 days            | 7 days             |
| Workspaces  | 15 days            | 3 days             |
| Caches      | 15 days            | 7 days             |

---

---

### Table of Contents

[Self Service Configuration Review](../self_service_config_review.md)

1. [Configuration Review Preparation](../review_preparation/review_preparation.md)
    - [Document the Config Review](../review_preparation/document_review.md)
    - [Review CircleCI Features](../review_preparation/review_features.md)
    - [Snapshot Project Metrics](../review_preparation/snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](../job_review/job_review.md)
    - [General Job Opportunities](../job_review/general_opportunities.md)
    - [Execution Environment Opportunities](../job_review/execution_environment.md)
    - [Opportunities for Jobs with High Duration](../job_review/high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](../workflow_review/workflow_review.md)
4. [High Level Improvement Opportunities](../high_level_recommendations/high_level_recommendations.md)
    - [Inside the Config](../inside_config/inside_config.md)
        - [Config Security](../inside_config/config_security.md)
        - [Reusable Config](../inside_config/reusable_config.md)
        - [Dynamic Config](../inside_config/dynamic_config.md)
    - [Outside the Config](outside_config.md)
        - [Security Settings](security_settings.md)
        - [Secret Management](secret_management.md)
        - \>\>[Storage Usage](storage_usage.md)<<
        - [Project Settings](project_settings.md)
5. [Finalize Review](../finalize_review/finalize_review.md)
