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
