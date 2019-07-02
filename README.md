# plan-ci

*Continuous integration for PLAN*

This repo contains a build pipeline and related files for building and integration testing all the various PLAN components. The goal is for this process to eventually publish binary releases for public use. For day-to-day development, you shouldn't need to use anything in this repo.

## Access for PLAN developers

Log into the the [Concourse CI server](https://ci.machinistlabs.com) using GitHub OAuth.

## Access for PLAN contributors and users

In the near future, we want to have a bot for the GitHub organization that can flag PRs from the community as safe to build (so as not to expose the donated build environment to risk from malicious PRs). At that time, we'll expose the results of builds to the public. Stay tuned!
