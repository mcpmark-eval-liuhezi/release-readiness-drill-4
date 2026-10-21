# Deployment Runbook (Drill Sandbox)

## Pre-deploy checks
1. Confirm the release ticket is approved and linked.
2. Verify CI is green on the release commit.
3. Check that no other deploy is in flight.
4. Confirm rollback plan is on hand.

## Deploy
1. Tag the release commit.
2. Trigger the deploy pipeline for the target environment.
3. Watch the pipeline until every stage reports success.
4. Announce completion in the release channel.

## Post-deploy monitoring
1. Watch dashboards for latency and error rate for 30 minutes.
2. Watch the alert channel for new critical alerts.
3. Stop the rollout if error rate doubles.
4. Otherwise, hand back to the on-call rotation and close the drill ticket.
