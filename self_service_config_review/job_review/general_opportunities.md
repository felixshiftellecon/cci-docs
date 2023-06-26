# General Job Opportunities

## 1) Review Step Outputs

Review each [step's](https://circleci.com/docs/glossary/#step) output to ensure it is completing as expected. This is important because steps can silently fail or not work as intended. For example, if a caching key is not found in the [`restore_cache` step](https://circleci.com/docs/configuration-reference/#restorecache) it will not fail the [job](https://circleci.com/docs/glossary/#job).

## 2) Review Step Placement

Review each step to see if it makes sense to have that step in the job. A job typically has a singular purpose and steps may fit better in their own job or in a different order. For example, if linting and unit tests are being done in the same job it may be a good idea to move the unit tests to a separate job. Especially if setting up dependencies is quick.

Having separation between various aspects of the pipeline allows those jobs to be run in parallel, reducing overall duration. The separation also provides clearer feedback when a [pipeline](https://circleci.com/docs/glossary/#pipeline) fails.

## 3) Record Reusable Config Opportunities

Note any steps, groups of steps, [executors](https://circleci.com/docs/glossary/#executor), [parameters](https://circleci.com/docs/reusing-config/#using-the-parameters-declaration), or jobs that are repeated in the config. Creating [reusable config keys](https://circleci.com/docs/reusing-config) allows those keys to be more easily maintained. For example, if a job uses environment variables for credentials and those variables change they only need to be updated in one place.

Parameterizing jobs can be a great way to make the config easier to maintain. [Steps can be conditional](https://circleci.com/docs/reusing-config/#defining-conditional-steps) to allow for multiple situations, like a staging environment vs production. [Jobs can be conditional](https://circleci.com/docs/reusing-config/#authoring-parameterized-jobs) and have [pre or post steps](https://circleci.com/docs/reusing-config/#using-pre-and-post-steps) added to them which expands how parameterized jobs can be used.

If any of these reusable config keys are used in other projects, consider [creating an orb](https://circleci.com/docs/orb-concepts/) to allow those keys to be used cross project and be maintained in once place.
