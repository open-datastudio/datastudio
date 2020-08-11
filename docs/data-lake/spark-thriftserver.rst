==================
Spark thriftserver
==================

Spark thrift server allowing multiple remote clients to access Spark.
It provides a generic JDBC endpoint that let any client including BI tools connect and access the power of Spark.
Open data studio makes it easy to deploy on the cloud.

Key features

  - Allows JDBC/ODBC clients to execute SQL queries over JDBC and ODBC protocols on Apache Spark.
  - Spark 3.0
  - Spark cluster is automatically configured on Kubernetes
  - Connect to :ref:`Hive metastore`. No configuration required

=============================== ===================================================================
Launch page                     https://staroid.com/g/open-datastudio/spark-thriftserver
Open data studio repository     https://github.com/open-datastudio/spark-thriftserver
Original repository             https://github.com/apache/spark
Documentation                   https://spark.apache.org/docs/latest/sql-distributed-sql-engine.html
=============================== ===================================================================

Spark thrift-server Quickstart
------------------------------

.. image:: https://staroid.com/api/run/button.svg
   :target: https://staroid.com/g/open-datastudio/spark-thriftserver


Get spark-thriftserver address
-------------------------------------

`spark-thriftserver-info <https://github.com/open-datastudio/spark-thriftserver/blob/master/k8s/spark-thriftserver-info.yaml>`_ ConfigMap is created
after deployment. The ConfigMap includes spark-thriftserver JDBC URL to connect.
Other project can import this ConfigMap. `Learn more <https://docs.staroid.com/project/dependency.html>`__.

.. include:: ../ref.rst
