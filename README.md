# fabric-data-pipelines


# NYC Taxi Data Pipeline - Microsoft Fabric

## Project Overview
This project demonstrates an end-to-end data pipeline in Microsoft Fabric using a Fabric Trial capacity. It ingests NYC Green Taxi data, applies transformations to calculate discounts, and copies the final dataset to a Lakehouse.

## Architecture
1. **Source:** NYC Taxi - Green (Parquet files)
2. **Transformation:** `nyc_taxi_with_discounts` (Dataflow Gen2)
3. **Orchestration:** `nyc_taxi_discount_pipeline` (Data Pipeline)
4. **Destination:** `rohan` Lakehouse
5. **Copy Mechanism:** `trail` (Copy Job)

## Workspace Items
*   **Copy Job (`trail`):** Performs a full copy from the source Parquet files to the Lakehouse.
*   **Dataflow (`nyc_taxi_with_discounts`):** Cleans and transforms the raw data.
*   **Lakehouse (`rohan`):** Stores the final Delta tables.
*   **Pipeline (`nyc_taxi_discount_pipeline`):** Orchestrates the execution of the Dataflow and Copy Job.

## How to Reproduce
1. Create a Microsoft Fabric Trial workspace.
2. Create a Lakehouse named `rohan`.
3. Import the JSON files found in this repository into your Fabric workspace.
4. Reconnect the Dataflow and Copy Job to your specific Lakehouse and data sources.
5. Run the `nyc_taxi_discount_pipeline`.

## Screenshots


!fabric_powerbi_trail_1.0.png

https://github.com/rohanksingh/fabric-data-pipelines/blob/main/fabric_powerbi_trail_1.0.png

https://github.com/rohanksingh/fabric-data-pipelines/blob/main/trail_nyctaxi_green_workspace.png


https://github.com/rohanksingh/fabric-data-pipelines/blob/main/power_query.png
