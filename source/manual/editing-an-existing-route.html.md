---
owner_slack: "#2ndline"
title: Edit an existing route in the Router
section: Routing
layout: manual_layout
parent: "/manual.html"
old_path_in_opsmanual: "../opsmanual/2nd-line/editing-an-existing-route.md"
last_reviewed_on: 2017-02-10
review_in: 6 months
---

> **This page was imported from [the opsmanual on GitHub Enterprise](https://github.com/alphagov/govuk-legacy-opsmanual)**.
It hasn't been reviewed for accuracy yet.
[View history in old opsmanual](https://github.com/alphagov/govuk-legacy-opsmanual/tree/master/2nd-line/editing-an-existing-route.md)


If there's a need to edit a Route in the database, follow these
instructions:

    $ ssh router-backend-1.router.production
    $ cd /var/apps/router-api
    $ sudo -u deploy govuk_setenv router-api bundle exec rails c
    > r = Route.where(incoming_path: '/path-to-item').first

manipulate the `r` object directly (see the
[documentation](https://github.com/alphagov/router#data-structure) for
available options), eg:

    > r.route_type = 'exact'
    > r.save!

once you've edited the Route appropriately and saved it, you need to
reload the router:

    > RouterReloader.reload
