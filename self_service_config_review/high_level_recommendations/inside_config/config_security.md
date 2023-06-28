# Config Security Opportunities

## 1) OIDC

[OIDC tokens](circleci.com/docs/openid-connect-tokens) are available in any [job](https://circleci.com/docs/glossary/#job) and is a great way to replace static credentials used to connect with cloud services for example, a Vault instance in AWS. Static credentials are not only a security issue, they can also add to the difficulty of managing CI as a whole since you need to have a rotation policy in place.

OIDC is also available for [custom images, stored in ECR](https://circleci.com/docs/pull-an-image-from-aws-ecr-with-oidc/), that are used as a job's [executor](https://circleci.com/docs/glossary/#executor).

## 2) Contexts

[Contexts](https://circleci.com/docs/glossary/#context) are used to help manage secrets within CircleCI. By default, they are available for anyone with access to run a [pipeline](https://circleci.com/docs/glossary/#pipeline) to use. Github projects can [restrict contexts](https://circleci.com/docs/contexts/#restrict-a-context) to a security group, allowing for more granular access levels.

## 3) Runner

<!-- I don't like the word difficult here -->

Jobs that need to access internal resources may be difficult to setup on a CircleCI cloud. [Runner](https://circleci.com/docs/runner-overview/) allows you to run the job on your own infrastructure which removes the need to setup complicated tunnels. Runners do need to be maintained so be sure to take that into account when considering implementing them.

## 4) IP Ranges

Jobs that need access to internal resources, but don't need to lock down the connection to a tunnel, can take advantage of [IP Ranges](https://circleci.com/docs/ip-ranges/) which restricts the traffic from CircleCI to a well defined list of IPs.

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
4. [High Level Improvement Opportunities](../high_level_recommendations.md)
    - [Inside the Config](inside_config.md)
        - \>\>[Config Security](config_security.md)<<
        - [Reusable Config](reusable_config.md)
        - [Dynamic Config](dynamic_config.md)
    - [Outside the Config](high_level_recommendations/outside_config/outside_config.md)
        - [Security Settings](high_level_recommendations/outside_config/security_settings.md)
        - [Secret Management](high_level_recommendations/outside_config/secret_management.md)
        - [Storage Usage](high_level_recommendations/outside_config/storage_usage.md)
        - [Project Settings](high_level_recommendations/outside_config/project_settings.md)
5. [Finalize Review](finalize_review/finalize_review.md)
