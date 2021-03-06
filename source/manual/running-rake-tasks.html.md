---
owner_slack: "#2ndline"
title: Run a rake task
section: Deployment
layout: manual_layout
parent: "/manual.html"
old_path_in_opsmanual: "../opsmanual/2nd-line/running-rake-tasks.md"
important: true
last_reviewed_on: 2016-12-21
review_in: 6 months
---

> **This page was imported from [the opsmanual on GitHub Enterprise](https://github.com/alphagov/govuk-legacy-opsmanual)**.
It hasn't been reviewed for accuracy yet.
[View history in old opsmanual](https://github.com/alphagov/govuk-legacy-opsmanual/tree/master/2nd-line/running-rake-tasks.md)


There is a Jenkins job that can be used to run any rake task:

-   Integration:
    <https://deploy.integration.publishing.service.gov.uk/job/run-rake-task/>
-   Staging:
    <https://deploy.staging.publishing.service.gov.uk/job/run-rake-task/>
-   Production:
    <https://deploy.publishing.service.gov.uk/job/run-rake-task/>

Jenkins jobs are also linkable. For example:

<https://deploy.integration.publishing.service.gov.uk/job/run-rake-task/parambuild/?TARGET_APPLICATION=content-tagger&MACHINE=backend-1.backend&RAKE_TASK=routes>
