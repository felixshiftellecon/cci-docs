# Opportunities for Jobs with High Duration

## 1) Resource Allocation

Optimizing the [resource classes](https://circleci.com/docs/glossary/#resource-class) of your [jobs](https://circleci.com/docs/glossary/#job) is an easy way to attempt to reduce the duration of a job. Each job has a resource tab in the UI shows the resource usage throughout the job, which is useful while reviewing jobs individually. [CircleCI's Insights UI](https://circleci.com/docs/resource-class-overview/#resource-class-insights) offers a view of historical usage for every job in a workflow which is more helpful when doing a config review.

A good rule of thumb is a job should be using 50% - 75% of it's resources. If a job is outside of that band try out one of the other resource classes for the [execution environment being used](https://circleci.com/product/features/resource-classes/).

**NOTE:** Increasing resource class size does not guarantee a job's duration will be reduced.

## 2) Caching

Jobs that install dependencies should [cache those dependencies](https://circleci.com/docs/caching) to speed up install time for future jobs. Caches are [project](https://circleci.com/docs/glossary/#project) wide so multiple jobs and multiple workflows can share them.

Most dependencies support using a [fallback cache key](https://circleci.com/docs/caching-strategy/#partial-dependency-caching-strategies) to allow for a partial cache match. Implementing a fallback cache key can help reduce duration when making changes on a new branch.

Review how [specific any current cache keys are](https://circleci.com/docs/caching-strategy/#avoid-strict-cache-keys) and if they need to be more or less specific.

## 3) Test splitting

Jobs that run tests can most likely be split. [Test splitting](https://circleci.com/docs/parallelism-faster-jobs/) runs multiple instances of the job in parallel and splits the tests among them, with [splitting by timing](https://circleci.com/docs/parallelism-faster-jobs/#how-test-splitting-works) being the more optimized approach. The [parallelism of the job](https://circleci.com/docs/parallelism-faster-jobs/#specify-a-jobs-parallelism-level) should be set to balance dependency setup time versus test suite duration. [The Timing tab](https://circleci.com/docs/test-splitting-tutorial/#step-three-view-results) in each job's UI is helpful when reviewing that balance.

## 4) Docker Layer Caching

Jobs that build docker images can typically benefit from enabling [Docker Layer Caching](https://circleci.com/docs/docker-layer-caching/). DLC caches individual docker image layers so they can be used in future jobs.
