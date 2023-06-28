# Secrets Management

## OIDC

Attempt to replace any static credentials used in CircleCI for connection to cloud environments with authentication using [OIDC tokens](https://circleci.com/docs/openid-connect-tokens/). This is not available for all tools so some credentials may need to remain. A rotation policy should be created for those remaining credentials.

A common and secure alternative to having static credentials in CircleCI is storing them in a secrets manager, like Vault or AWS Secrets Manager. OIDC can be used to authenticate with the secrets manager tool and pull secrets into the job.

## Contexts

For github orgs, ensure [contexts](https://circleci.com/docs/contexts/) are restricted to applicable security groups. If possible, migrate important secrets to a secrets manager and use OIDC to pull those secrets into jobs.

---

---

### Table of Contents

[Self Service Configuration Review](../../self_service_config_review.md)

1. [Configuration Review Preparation](../../review_preparation/review_preparation.md)
    - [Document the Config Review](../../review_preparation/document_review.md)
    - [Review CircleCI Features](../../review_preparation/review_features.md)
    - [Snapshot Project Metrics](../../review_preparation/snapshot_metrics.md)
2. [Review Each Job for Improvement Opportunities](../../job_review/job_review.md)
    - [General Job Opportunities](../../job_review/general_opportunities.md)
    - [Execution Environment Opportunities](../../job_review/execution_environment.md)
    - [Opportunities for Jobs with High Duration](../../job_review/high_duration.md)
3. [Review Each Workflow for Improvement Opportunities](../../workflow_review/workflow_review.md)
4. [High Level Improvement Opportunities](../../high_level_recommendations/high_level_recommendations.md)
    - [Inside the Config](../inside_config/inside_config.md)
        - [Config Security](../inside_config/config_security.md)
        - [Reusable Config](../inside_config/reusable_config.md)
        - [Dynamic Config](../inside_config/dynamic_config.md)
    - [Outside the Config](outside_config.md)
        - [Security Settings](security_settings.md)
        - \>\>[Secret Management](secret_management.md)<<
        - [Storage Usage](storage_usage.md)
        - [Project Settings](project_settings.md)
5. [Finalize Review](../../finalize_review/finalize_review.md)
