<br />
<center>
  <img src="https://github.com/open-datastudio/datastudio/raw/master/docs/_static/open-datastudio-logo.png" width="250px"/>
</center>
<br />

# Open datastudio

Open datastudio is a set of data-science, machine learning projects that integrates to [staroid](https://staroid.com).

Goal is to make projects ready to run in a few clicks without complex installation and maintenance.

Also to fund the contributors of each individual projects via [StarRank](https://staroid.com/site/starrank).

## Projects

| Component | Project | Description | Integration Status |
| ------- | --------- | ----------- | ------- |
| Notebook | [jupyter](https://github.com/open-datastudio/jupyter) | Jupyter Lab | Integrated |
| | [zeppelin](https://github.com/open-datastudio/zeppelin) | Integrates with Apache Zeppelin and Apache Spark on Kubernetes mode | Integrated |
| Data Lake | [hive-metastore](https://github.com/open-datastudio/hive-metastore) | Provides hive metastore server with Postgresql database | Integrated |
| | [spark-thriftserver](https://github.com/open-datastudio/spark-thriftserver) | Spark cluster on Kubernetes for ODBC/JDBC connection | Integrated |
| Computing | [dask-cluster](https://github.com/open-datastudio/dask-cluster) | [Dask](https://dask.org) cluster | In progress |
| | [ray-cluster](https://github.com/open-datastudio/ray-cluster) | [Ray](https://ray.io/) cluster | In progress |
| | [spark-serverless](https://github.com/open-datastudio/spark-serverless) | On-demand [Spark](https://spark.apache.org) cluster from everywhere | Integrated |
| Machine learning | [mlflow-server](https://github.com/open-datastudio/mlflow-server) | [MLflow](https://mlflow.org/) model remote tracking server and ui | Integrated
| | [mlflow-model-serving](https://github.com/open-datastudio/mlflow-model-serving) | Deploy models from mlflow-server and get endpoint | Integrated
| Business Intelligence | [metabase](https://github.com/open-datastudio/metabase) | Metabase Business Intelligence | Integrated |
| | [superset](https://github.com/open-datastudio/superset) | Apache Superset Business Intelligence | Integrated |
| Misc | [spark](https://github.com/open-datastudio/spark) | It does not integrates to Staroid but publishes docker image for other projects | - |



## How to contribute?

You can create issues or pull requests to contribute individual repositories under [open-datasicence](https://github.com/open-datastudio).

If you'd like to create a new integration project here, please create an [issue](https://github.com/open-datastudio/datastudio/issues) in this repository.

We need your help!
