# plan-ci

*Continuous integration for PLAN*

This repo contains a build pipeline and related files for building and integration testing all the various PLAN components, and publishing of binary releases for public development use. For day-to-day development, you shouldn't need to use anything in this repo.

## Access for PLAN developers

Log into the the [Concourse CI server](https://ci.machinistlabs.com) using GitHub OAuth.

## Access for PLAN contributors and users

The pipeline for the master branch of this repo has been made public (read-only) on our [Concourse CI server](https://ci.machinistlabs.com/teams/plan/pipelines/plan). This currently builds only commits that have been merged to master of the various PLAN repos.

In the near future, we want to have a bot for the GitHub organization that can flag PRs from the community as safe to build (so as not to expose the donated build environment to risk from malicious PRs). At that time, we'll expose the results of builds to the public. Stay tuned!
