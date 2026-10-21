# Rollback Checklist (Drill Sandbox)

1. Declare the rollback in the release channel.
2. Freeze the affected deploy pipeline.
3. Tag the last known-good release commit.
4. Trigger the rollback pipeline for the target environment.
5. Watch the pipeline until every stage reports success.
6. Watch dashboards and the alert channel for 30 minutes.
7. Confirm data integrity after rollback.
