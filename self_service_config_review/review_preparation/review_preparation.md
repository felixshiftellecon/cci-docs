# Configuration Review Preparation

## 1) Select the project

Config reviews should be scoped to one [project](https://circleci.com/docs/glossary/#project). In some cases scoping them to a specific larger [workflow](https://circleci.com/docs/glossary/#workflow) can be helpful, but some opportunities may be missed.

Top 3 reasons to select a project:

- High [credit](https://circleci.com/docs/credits/#what-are-credits) consumption
- Long workflow durations
- Overly complex configurations

## 2) Identify Current Pain Points

Source pain points from the people that use CircleCI in the selected project on a regular basis. The most common pain point is a high duration, which is easy to see while looking through metrics. Other common pain points are a workflows being hard to onboard new people to or flaky tests, which can be harder to identify through metrics.

Collecting pain points from the whole team can be a great way to find opportunities for improvement and there may be some opportunities surfaced that wouldn't have been found solely through metrics.

## 3) Decide Which Metrics are Important

A high duration is the most common metric of concern when doing a config review. Other metrics that come up often are success rate, mean time to recover, flaky tests, and credit consumption. [CircleCI's Insights](https://circleci.com/docs/insights/#overview) offers data for these metrics in the UI or [via the API](https://circleci.com/docs/api/v2/index.html#tag/Insights) and is a great way to not only identify areas of concern but also to ensure any changes made are having an impact.

[Self Service Configuration Review](self_service_config_review.md)
1. \>\>[Configuration Review Preparation](review_preparation/review_preparation.md)<<
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
