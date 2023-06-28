# Config Security Opportunities

## 1) OIDC

[OIDC tokens](circleci.com/docs/openid-connect-tokens) are available in any [job](https://circleci.com/docs/glossary/#job) and is a great way to replace static credentials used to connect with cloud services. For example, a Vault instance in AWS. Static credentials are not only a security issue, they can also add to the difficulty of managing CI as a whole since you need to have a rotation policy in place.

OIDC is also available for [custom images, stored in ECR](https://circleci.com/docs/pull-an-image-from-aws-ecr-with-oidc/), that are used as a job's [executor](https://circleci.com/docs/glossary/#executor).

## 2) Contexts

[Contexts](https://circleci.com/docs/glossary/#context) are used to help manage secrets within CircleCI. By default, they are available for anyone with access to run a [pipeline](https://circleci.com/docs/glossary/#pipeline) to use. Github projects can [restrict contexts](https://circleci.com/docs/contexts/#restrict-a-context) to a security group, allowing for more granular access levels.

## 3) Runner

Jobs that need to access internal resources may be hard to manage on CircleCI cloud. [Runner](https://circleci.com/docs/runner-overview/) allows you to run the job on your own infrastructure which removes the need to setup complicated tunnels. Runners do need to be maintained so be sure to take that into account when considering implementing them.

## 4) IP Ranges

Jobs that need access to internal resources, but don't need to lock down the connection to a tunnel, can take advantage of [IP Ranges](https://circleci.com/docs/ip-ranges/) which restricts the traffic from CircleCI to a well defined list of IPs.

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
        - \>\>[Config Security](config_security.md)<<
        - [Reusable Config](reusable_config.md)
        - [Dynamic Config](dynamic_config.md)
    - [Outside the Config](outside_config.md)
        - [Security Settings](security_settings.md)
        - [Secret Management](secret_management.md)
        - [Storage Usage](storage_usage.md)
        - [Project Settings](project_settings.md)
5. [Finalize Review](finalize_review.md)
