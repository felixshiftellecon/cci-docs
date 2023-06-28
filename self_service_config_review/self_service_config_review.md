# Self Service Configuration Review

<!-- Do we need to make this more interactive? i.e. how does your team go about doing x at the end of each step -->

## What is a Configuration Review

A config review is a process where a project's pipeline configuration is evaluated for improvement opportunities. Those opportunities are identified through the lens of goals created at the beginning of the review process.

## Why do a Configuration Review

 Config reviews are a key process for maintaining an optimized CI experience. The software you are building and the tools you are using are ever evolving so your pipelines should be evolving with them. Config reviews can help ensure the max value is extracted from every credit.

## Configuration Review Process

A config review can be conducted by following the recommended procedure below. Each step in the procedure will be in a separate post containing useful documentation links, helpful tips, and any recommended processes for that step.

Discussion of best practices, tips, tricks, and feedback for each step should be conducted within the relevant post.

Any feedback on the process as a whole should be discussed within this main post.

---

\>\>[Self Service Configuration Review](self_service_config_review.md)<<

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
5. [Finalize Review](finalize_review/finalize_review.md)