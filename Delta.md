# Delta


## Delta Lake

Delta Lake is an open source storage layer that brings reliability to data lake.

### Partition 

```
  def createPartitionedTable(data: DataFrame, tableName: String, Keys: String): Unit = {
  data
      .write
      .partitionBy(Keys)
      .format("delta")
      .mode("overwrite")
      .option("mergeSchema", "true")
      .save("/opt/partitioned_lake/" + tableName)
  }
```

### Index

**Indexing happens automatically** on Databricks Delta.

## Dalta Engine

Delta Engine provides optimized layouts and indexes for fast interactive queries.

# References

- https://docs.databricks.com/delta/index.html#
- https://docs.databricks.com/_static/notebooks/delta/optimize-sql.html
- https://medium.com/@aravinthR/partitioned-delta-lake-part-3-5cc52b64ebda
- https://docs.databricks.com/spark/latest/spark-sql/dataskipping-index.html
- https://stackoverflow.com/questions/58527576/create-index-for-tables-within-delta-lake
- https://docs.databricks.com/delta/optimizations/file-mgmt.html#data-skipping
