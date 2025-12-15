This is an example for reproducing an [issue with schema evolvability](https://github.com/datacontract/datacontract-cli/issues/977) using the datacontract CLI tool.

These should succeed:

`datacontract test --server dev-csv ./odcs-datacontract-cities_0_1_1.yaml`

`datacontract test --server dev-parquet ./odcs-datacontract-cities_0_1_1.yaml`

These will fail because the new optional field `population` is missing in historical data:

`datacontract test --server dev-csv ./odcs-datacontract-cities_0_2_0.yaml`

`datacontract test --server dev-parquet ./odcs-datacontract-cities_0_2_0.yaml`
