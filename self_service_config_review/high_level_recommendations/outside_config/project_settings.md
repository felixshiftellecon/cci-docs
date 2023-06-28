# Project Settings

## Security

Review [project](https://circleci.com/docs/glossary/#project) settings to ensure they are set correctly, this can be done via the UI or [API](https://fieldguide.circleci-labs.com/api_endpoints/project_settings_api/).

Confirm that the following Advanced settings are toggled _off_ unless needed for your use case:

- Build forked pull requests
- Pass secrets to builds from forked pull requests

Confirm that the following [API only project settings](https://fieldguide.circleci-labs.com/api_endpoints/project_settings_api/) are toggled _on_ unless not needed for your use case:

- disable-ssh
- write-settings-requires-admin

Confirm no unexpected SSH keys, project API tokens, or integrations are present.

## Non-security

Review project settings to see if any options would be helpful with your use case. Helpful options include:

- Only build pull requests
- Auto-cancel redundant [workflows](https://circleci.com/docs/glossary/#workflow)
- Enable dynamic config using setup workflows
- GitHub Status Updates

Review current triggers to ensure [scheduled pipelines](https://circleci.com/docs/scheduled-pipelines/) are running at the correct times. If there are no scheduled pipelines, consider implementing one.

Review available integrations and see if any can be implemented to improve user experience.

Review current [webhooks](https://circleci.com/docs/webhooks/) to ensure they are being consumed appropriately. If webhooks aren't being used, consider implementing them.

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
        - [Security Settings](security_settings.md)
        - [Secret Management](secret_management.md)
        - [Storage Usage](storage_usage.md)
        - \>\>[Project Settings](project_settings.md)<<
5. [Finalize Review](finalize_review.md)
