---
owner_slack: "#2ndline"
title: Asset master attachment processing
parent: "/manual.html"
layout: manual_layout
section: Icinga alerts
last_reviewed_on: 2017-05-01
review_in: 6 months
---

When new assets get uploaded to asset-master-1, there is a script
(/usr/local/bin/process-uploaded-attachment.sh) run by the assets user
every minute in a cronjob. This kicks off a script (virus-scan-file.sh)
which scans files and then moves them into either a "clean" or
"infected" directory. If you have received an alert regarding this it
means that the job has not run for over half an hour and is probably
locked (or processing a large amount of files).
