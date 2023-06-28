# Dynamic Config

## Why Dynamic Config

[Dynamic configuration](https://circleci.com/docs/dynamic-config/) is an easy way to not have to run a full [pipeline](https://circleci.com/docs/glossary/#pipeline) when it's not needed, saving [credits](https://circleci.com/docs/credits/) and time. Most projects can benefit from dynamic config but monolith [projects](https://circleci.com/docs/glossary/#project) especially benefit.

## Starting Out

Dynamic config has a wide variety of uses but essentially boils down to creating [pipeline parameters](https://circleci.com/docs/pipeline-variables/#pipeline-parameters-in-configuration) in a setup workflow, then running [workflows](https://circleci.com/docs/glossary/#workflow) based off those parameters.

To start using dynamic config, CircleCI has an [orb](https://circleci.com/docs/glossary/#orbs) that creates parameters based on the paths in the repo where changes have been made. With a little bit of setup you can use the [path filtering orb](https://circleci.com/developer/orbs/orb/circleci/path-filtering) to not have to run your full workflow.

## Advanced Use

Review the pipeline and figure out what parameters could be created and used to trigger conditional workflows and jobs. Create a setup config that generates those parameters then uses the continuation orb to pass them to a downstream workflow.

---

---

### Table of Contents

[Self Service Configuration Review](self_service_config_review.md)

1. [Configuration Review Preparation](review_preparation.md)
    - [Document the Config Review](document_review.md)
    - [Review CircleCI Features](review_features.md)
    - [Snapshot Project Metrics](snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](job_review.md)
    - [General Job Opportunities](general_opportunities.md)
    - [Execution Environment Opportunities](execution_environment.md)
    - [Opportunities for Jobs with High Duration](high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](workflow_review.md)
4. [High Level Improvement Opportunities](high_level_recommendations.md)
    - [Inside the Config](inside_config.md)
        - [Config Security](config_security.md)
        - [Reusable Config](reusable_config.md)
        - \>\>[Dynamic Config](dynamic_config.md)<<
    - [Outside the Config](outside_config.md)
        - [Security Settings](security_settings.md)
        - [Secret Management](secret_management.md)
        - [Storage Usage](storage_usage.md)
        - [Project Settings](project_settings.md)
5. [Finalize Review](finalize_review.md)


---

[Self Service Configuration Review](self_service_config_review.md)

1. [Configuration Review Preparation](review_preparation/review_preparation.md)
    - [Document the Config Review](review_preparation/document_review.md)
    - [Review CircleCI Features](review_preparation/review_features.md)
    - [Snapshot Project Metrics](review_preparation/snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](job_review/job_review.md)
    - [General Job Opportunities](job_review/general_opportunities.md)
    - [Execution Environment Opportunities](job_review/execution_environment.md)
    - [Opportunities for Jobs with High Duration](job_review/high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](workflow_review/workflow_review.md)
4. [High Level Improvement Opportunities](../high_level_recommendations.md)
    - [Inside the Config](inside_config.md)
        - [Config Security](config_security.md)
        - [Reusable Config](reusable_config.md)
        - \>\>[Dynamic Config](dynamic_config.md)<<
    - [Outside the Config](high_level_recommendations/outside_config/outside_config.md)
        - [Security Settings](high_level_recommendations/outside_config/security_settings.md)
        - [Secret Management](high_level_recommendations/outside_config/secret_management.md)
        - [Storage Usage](high_level_recommendations/outside_config/storage_usage.md)
        - [Project Settings](high_level_recommendations/outside_config/project_settings.md)
5. [Finalize Review](finalize_review/finalize_review.md)
