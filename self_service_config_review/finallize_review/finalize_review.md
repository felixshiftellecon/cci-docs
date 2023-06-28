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
4. [High Level Improvement Opportunities](high_level_recommendations/high_level_recommendations.md)
    - [Inside the Config](high_level_recommendations/inside_config/inside_config.md)
        - [Config Security](high_level_recommendations/inside_config/config_security.md)
        - [Reusable Config](high_level_recommendations/inside_config/reusable_config.md)
        - [Dynamic Config](high_level_recommendations/inside_config/dynamic_config.md)
    - [Outside the Config](high_level_recommendations/outside_config/outside_config.md)
        - [Security Settings](high_level_recommendations/outside_config/security_settings.md)
        - [Secret Management](high_level_recommendations/outside_config/secret_management.md)
        - [Storage Usage](high_level_recommendations/outside_config/storage_usage.md)
        - [Project Settings](high_level_recommendations/outside_config/project_settings.md)
5. \>\>[Finalize Review](finalize_review.md)<<
