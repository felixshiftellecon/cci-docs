# Review Each Workflow for Improvement Opportunities

## 1) Review Job Placement

[Job](https://circleci.com/docs/glossary/#job) order can be the largest impact on [workflow](https://circleci.com/docs/glossary/#workflow) duration. Review the workflow for opportunities to [run jobs in parallel](https://circleci.com/docs/workflows/#fan-outfan-in-workflow) and note which jobs are bottlenecking the workflow to review them for improvement opportunities.

Placing shorter jobs, like linters, in the beginning of the workflow is helpful in reducing the time to receive feedback about a change being tested. This saves [credits](https://circleci.com/docs/credits/) and time as a large portion of the workflow doesn't need to run to receive feedback about a small issue.

## 2) Identify Modular Configuration Opportunities

When reviewing workflows that fan out but never fan back in, see if the jobs could be grouped into separate workflows. Having multiple workflows provides the separation needed to take advantage of [dynamic config](https://circleci.com/docs/dynamic-config/), which allows workflows to be triggered based on parameters set in a setup workflow. [Workflows and jobs can then be conditionally run](https://support.circleci.com/hc/en-us/articles/360043638052-Conditional-steps-in-jobs-and-conditional-workflows), saving time and credits.

Creating [parameterized jobs](https://circleci.com/docs/reusing-config/#authoring-parameterized-jobs) allows for further implementation of dynamic config and leads an easier to manage config in most cases.
