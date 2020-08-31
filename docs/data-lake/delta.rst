==============
Delta Lake
==============

Delta Lake is an open-source storage layer that brings ACID
transactions to Apache Spark™ and big data workloads.

Open data provides Delta lake in the following spark environments

================================================== ==========================================
Service                                            Note
================================================== ==========================================
:ref:`Apache Zeppelin`                             Through ``%spark`` interpreter
:ref:`Spark cluster from your python environment`  ``ods.spark("cluster-name", delta=True)``
================================================== ==========================================

.. include:: ../ref.rst
