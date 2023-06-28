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

[Self Service Configuration Review](self_service_config_review.md)

1. [Configuration Review Preparation](review_preparation.md)
    - \>\>[Document the Config Review](document_review.md)<<
    - [Review CircleCI Features](review_features.md)
    - [Snapshot Project Metrics](snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](\job_review.md)
    - [General Job Opportunities](\general_opportunities.md)
    - [Execution Environment Opportunities](\execution_environment.md)
    - [Opportunities for Jobs with High Duration](\high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](workflow_review.md)
4. [High Level Improvement Opportunities](high_level_recommendations.md)
    - [Inside the Config](inside_config.md)
        - [Config Security](config_security.md)
        - [Reusable Config](reusable_config.md)
        - [Dynamic Config](dynamic_config.md)
    - [Outside the Config](outside_config.md)
        - [Security Settings](security_settings.md)
        - [Secret Management](secret_management.md)
        - [Storage Usage](storage_usage.md)
        - [Project Settings](project_settings.md)
5. [Finalize Review](finalize_review.md)
