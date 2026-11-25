# SAA-C03 practice questions

1. A fleet needs to mount one shared Linux directory from multiple Availability Zones. Which storage interface fits, and why would independent EBS volumes fail the requirement?
2. An order worker may receive the same queue message again after a timeout. Where should it enforce idempotency?
3. A dataset is rarely retrieved and deleted within two weeks. Which charge categories must the team compare before a lifecycle transition?

## Answers

1. Use an EFS file system for shared NFS access. Separate EBS volumes do not provide a single shared directory.
2. Persist an idempotency key at the business operation boundary. A successful side effect must remain identifiable after a retry.
3. Compare storage, transition and retrieval requests, retrieval charges, and any minimum-duration charges for the candidate class.
