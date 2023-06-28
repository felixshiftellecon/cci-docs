# Document the Config Review

## 1) Create a Document for the Review

Most organizations have more than one [project](https://circleci.com/docs/glossary/#project) on CircleCI and will most likely need to do more than one config review. Creating a format or template that can be used for all config reviews can be helpful to ensure they are standardized.

The following information should be included in the document:
- Goals
- Project metrics
- [Job](https://circleci.com/docs/glossary/#job) specific recommendations
- High level recommendations
- Place for documentation links

As the config review is conducted, you will most likely find yourself referencing all sorts of documentation both internal and external. Recording the links to those docs can be very helpful for anyone working on the changes after the review or who wants to understand why a certain recommendation was made.

---

---

### Table of Contents

[Self Service Configuration Review](../self_service_config_review.md)

1. [Configuration Review Preparation](review_preparation.md)
    - \>\>[Document the Config Review](document_review.md)<<
    - [Review CircleCI Features](review_features.md)
    - [Snapshot Project Metrics](snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](../job_review/job_review.md)
    - [General Job Opportunities](../job_review/general_opportunities.md)
    - [Execution Environment Opportunities](../job_review/execution_environment.md)
    - [Opportunities for Jobs with High Duration](../job_review/high_duration.md)
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