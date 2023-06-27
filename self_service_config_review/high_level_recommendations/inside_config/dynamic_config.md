# Dynamic Config

## Why Dynamic Config

Dynamic configuration is an easy way to not have to run a full pipeline when it's not needed, saving credits and time. Most projects can benefit from dynamic config but monolith repos especially benefit.

## Starting Out

Dynamic config has a wide variety of uses but essentially boils down to creating pipeline parameters in a setup workflow, then running workflows based off those parameters.

To start using dynamic config, CircleCI has an orb that creates parameters based on the paths in the repo where changes have been made. With a little bit of setup you can use the path filtering orb to not have to run your full workflow.

## Advanced Use

Review the pipeline and figure out what parameters could be created and used to trigger conditional workflows and jobs. Create a setup config that generates those parameters then uses the continuation orb to pass them to a downstream workflow.

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
        - \>\>[Dynamic Config](high_level_recommendations/inside_config/dynamic_config.md)<<
    - [Outside the Config](high_level_recommendations/outside_config/outside_config.md)
        - [Security Settings](high_level_recommendations/outside_config/security_settings.md)
        - [Secret Management](high_level_recommendations/outside_config/secret_management.md)
        - [Storage Usage](high_level_recommendations/outside_config/storage_usage.md)
        - [Project Settings](high_level_recommendations/outside_config/project_settings.md)
5. [Finalize Review](finalize_review/finalize_review.md)
