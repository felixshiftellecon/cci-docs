# Security Settings

## Project Settings

Review [project](https://circleci.com/docs/glossary/#project) settings to ensure they are set correctly, this can be done via the UI or [API](https://fieldguide.circleci-labs.com/api_endpoints/project_settings_api/).

Confirm that the following Advanced settings are toggled _off_ unless needed for your use case:

- Build forked pull requests
- Pass secrets to builds from forked pull requests

Confirm that the following [API only project settings](https://fieldguide.circleci-labs.com/api_endpoints/project_settings_api/) are toggled _on_ unless not needed for your use case:

- disable-ssh
- write-settings-requires-admin

Confirm no unexpected SSH keys, project API tokens, or integrations are present.

## Org Settings

Confirm there are no unexpected technical or security contacts present. Add at least one if none are present.

Confirm [contexts](https://circleci.com/docs/contexts/) are restricted appropriately.

Ensure use of uncertified [orbs](https://circleci.com/docs/glossary/#orbs) is disabled if applicable.

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
        - [Dynamic Config](dynamic_config.md)
    - [Outside the Config](outside_config.md)
        - \>\>[Security Settings](security_settings.md)<<
        - [Secret Management](secret_management.md)
        - [Storage Usage](storage_usage.md)
        - [Project Settings](project_settings.md)
5. [Finalize Review](finalize_review.md)
