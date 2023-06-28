# Finalize Review

## Document Opportunities

Document opportunities as they are found throughout the review. You will most likely find yourself referencing all sorts of documentation both internal and external in the review. Recording the links to those docs can be very helpful for anyone working on the changes after the review or who wants to understand why a certain recommendation was made.

## Implement Changes

Review available opportunities and prioritize them based the goal of the review. Implement changes in batches to see the impact of individual changes and make troubleshooting easier.

## Test Changes

Test changes made by running a pipeline. After confirming the changes work on a dev branch, be sure to test them in different environments as well. Compare the new pipeline metrics to the metrics recorded in the config review to confirm changes were successful.

It is beneficial to monitor the changes after releasing them to confirm metrics don't start going in the wrong direction unexpectedly.

## Record What Worked

Record the test results, even if they didn't work, to help future config reviewers or maintainers to understand why certain features or functionality do and do not work in the project.

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
        - [Project Settings](project_settings.md)
5. \>\>[Finalize Review](finalize_review.md)<<
