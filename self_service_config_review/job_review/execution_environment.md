# Execution Environment Opportunities

## 1) Resource Allocation

Optimizing the [resource classes](https://circleci.com/docs/glossary/#resource-class) of your [jobs](https://circleci.com/docs/glossary/#job) is an easy way to ensure credits aren't being wasted. Each job has a resource tab in the UI shows the resource usage throughout the job, which is useful while reviewing jobs individually. [CircleCI's Insights UI](https://circleci.com/docs/resource-class-overview/#resource-class-insights) offers a view of historical usage for every job in a workflow which is more helpful when doing a config review.

A good rule of thumb is a job should be using 50% - 75% of it's resources. If a job is outside of that band try out one of the other resource classes for the [execution environment being used](https://circleci.com/product/features/resource-classes/).

## 2) Runner

<!-- I don't like the word difficult here -->

[Runners](https://circleci.com/docs/runner-overview/) are useful when a job needs to access data from an internal source or has many dependencies that need to be set up. Those types of jobs can be difficult to setup on a CircleCI cloud execution environment and may not be secure. Runner allows you to customize the environment your job is running in and run the job on your own infrastructure which helps support these difficult jobs. Runners do need to be maintained so be sure to take that into account when considering implementing them.