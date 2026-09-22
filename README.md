# xengine-consumer-analytics

Analytics team's dbt project on Snowflake. Depends on `xengine-producer-stock` ONLY through `models/_sources.yml`, where each table
declares the producer's physical identity (`glue:stock_common_mesh.<table>`). Marts are Snowflake-managed Iceberg in `STOCK_CONSUMER_MESH`.

    ./xdbt.sh build
    ./xdbt.sh docs generate
