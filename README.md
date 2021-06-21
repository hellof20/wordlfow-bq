# wordlfow-bq

- workflow1: insert2.workflows.yaml, decide by args to run a insert job
- workflow2: para2.workflows.yaml, invode multiple insert2.workflow.yaml jobs concurrently.

```
gcloud workflows deploy --source=./insert2.workflows.yaml --location=us-central1 test-insert2
gcloud workflows run test-insert2 --data='{"key1":1}'
gcloud workflows deploy --source=./para2.workflows.yaml --location=us-central1 para2
gcloud workflows run para2
```
