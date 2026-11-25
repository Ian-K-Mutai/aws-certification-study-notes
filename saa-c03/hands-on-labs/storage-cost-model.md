# Storage cost model exercise

Use a spreadsheet or calculator. This exercise uses invented prices and incurs no cloud charges.

Compare two options for 100 GiB retained for 15 days in a 30-day month. Class A charges 0.025 units per GiB-month and no retrieval fee. Class B charges 0.012 units per GiB-month, has a 30-day minimum and charges 0.01 units per GiB retrieved. The example ignores request charges so you can isolate these effects.

1. Calculate the bill if nobody retrieves the data. Class A costs 1.25 units. Class B costs 1.20 units because its minimum duration applies.
2. Retrieve 30 GiB in the model. Class B rises to 1.50 units. Class A remains at 1.25 units under the exercise assumptions.
3. Solve for the retrieval threshold. Five GiB produces a tie when the other assumptions stay fixed.
4. List the service-specific terms you would replace with current rates for a real workload, including requests, minimum billable object size, transitions and applicable data transfer.

[Cost-optimised architectures](../04-cost-optimised-architectures/README.md)
