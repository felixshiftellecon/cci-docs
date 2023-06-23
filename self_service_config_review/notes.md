# Intro

## What

## Why

## Table of Contents

Kick off
- Which project
- Source pain points
- Figure out which metrics matter and why

  Create a doc
  - If doing more in the future, create a template
  - Should contain
    - Goals
    - Metrics
    - Job specific recommendations
    - High level/ overarching recommendations
    - Place for documentation links
  - Importance of links

  Review features
  - link to changelog and RSS feed
  - Keep in back of mind during config review

  Snapshot Metrics
  - Use API
  - Separate important branches from all branches
  - Provide starter API script

Reviewing each job
- Why line by line, step by step review is beneficial

  General tips
    - step outputs
    - do steps belong in this job
    - Could this be DRYer

  Resources
    - resource class size
      - resource tab
      - insights
    - custom docker image
    - runner

  High Duration
    - resource class size
    - caching
    - test splitting
    - DLC

Reviewing the workflow
- job order
- do jobs belong in this workflow
- can triggers be dynamic
- can jobs be dynamic

Generic High Level Recommendations
    - org/project wide recs
    - jobs with same recommendations = high level rec
      - more visible as a solution for multiple instances

  Inside the config
    - security
    - config order
    - Reusable Config
    - Dynamic Config

  Outside the config
    - Security
    - Contexts
    - Storage usage controls
    - Project settings

Documentation
- compile all links at the end of the review