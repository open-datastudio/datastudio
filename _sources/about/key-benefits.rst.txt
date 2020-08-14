Key benefits
============

Machine learning pipeline
-------------------------

  Open Data Studio provides Jupyter, Zeppelin notebook to experiment, build your model on your favorite ML framework.
  Trained model can be stored in MLflow model registry and then being deployed for serving using MLflow model serving.

Distributed computing
----------------------

  Open Data Studio integrates various distributed computing environment you can use out of the box.
   
      - Apache Spark
      - Apache Flink (Work in progress)
      - Dask (Work in progress)
      - Ray (Work in progress)

Integrated environment
----------------------

  ODS is not only just a collection of open-source tools but also the integration of them to build end-to-end data processing / ML pipeline.
   
  For example

      - When MLflow model tracking server is deployed, Jupyter notebook and MLflow model serving will be automatically configured to use it.
      - When Hive-metastore is deployed, Spark thrift server and Apache Zeppelin are automatically configured to connect remote metastore.

Highly Modular
--------------

  Deploy the only components you need. Don't have to deploy all the components.
  ODS is widely open for new component integration.


Works on Kubernetes
-------------------

ODS works in any Kubernetes cluster. From minikube to your Kubernetes cluster on the cloud.

  - Minimum technolodgy dependencies
      - Requires minimum set of features in Kubernetes. Just plain old Kuberentes API is required.
        Does not depends on additional layer (such as Istio) to keep things simple.
  - Run as a non-root
      - All components runs with non-root permission.
  - Minimum Rbac permission
      - ODS only requires minimum Rbac that most multi-tenant configuration allows.
