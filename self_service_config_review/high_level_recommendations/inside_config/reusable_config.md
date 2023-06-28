# Reusable Config Opportunities

## 1) Config SDK

CircleCI config files are written in YAML but that doens't mean they have to be built using YAML. The [Config SDK](https://circleci.com/docs/circleci-config-sdk/#overview) is a javascript/typescript SDK that can be used to generate configuration files. This can be used to generate config manually or, using dynamic config, to generate them each time a [pipeline](https://circleci.com/docs/glossary/#pipeline) is triggered.

## 2) Orbs

[Orbs](https://circleci.com/docs/glossary/#orbs) can be used to share configuration keys across an organization. This is especially useful if all [projects](https://circleci.com/docs/glossary/#project) need to use a certain tool. The commands, [executors](https://circleci.com/docs/glossary/#executor), and parameters required to use the tool can be built into the orb.

CircleCI and our Partners maintain a number of orbs for common tools so reviewing the [orb registry](https://circleci.com/developer/orbs) is a great way to save yourself some time. Even if you need to create a private orb, the orb registry contains numerous examples to reference from other users.

## 3) Reusable Config

Review the config file for any repeated configuration keys. Repeated keys should be consolidated into a reusable key or added to an orb. Creating [parameterized jobs](https://circleci.com/docs/reusing-config/#authoring-parameterized-jobs) allows for implementation of dynamic config and leads to an easier to manage config in most cases.

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
    - [Inside the Config](inside_config.md)
        - [Config Security](config_security.md)
        - \>\>[Reusable Config](reusable_config.md)<<
        - [Dynamic Config](dynamic_config.md)
    - [Outside the Config](../outside_config/outside_config.md)
        - [Security Settings](../outside_config/security_settings.md)
        - [Secret Management](../outside_config/secret_management.md)
        - [Storage Usage](../outside_config/storage_usage.md)
        - [Project Settings](../outside_config/project_settings.md)
5. [Finalize Review](../finalize_review/finalize_review.md)
