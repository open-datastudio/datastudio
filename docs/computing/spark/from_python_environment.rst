---------------------------------------------------
Spark cluster from your python environment
---------------------------------------------------

Install
--------------------------

.. code-block:: bash

   pip install ods

Initialize
--------------------------

.. code-block:: python

   import ods
   ods.init()


See `ods quick start`_ for configuration.

Spark Quickstart
---------------------------

 - `Spark serverless on Google Colab <https://colab.research.google.com/github/open-datastudio/spark-serverless/blob/master/notebooks/Spark_serverless_on_Colab.ipynb>`_

Usage
-----

Create spark session with the default configuration
    .. code-block:: python

       import ods
       spark = ods.spark("my-cluster").session()

Create spark session with 3 worker nodes
    .. code-block:: python

       import ods
       spark = ods.spark("my-cluster", worker_num=3).session()

Create spark session with delta lake
    .. code-block:: python

       import ods
       spark = ods.spark("my-cluster", delta=True).session()



See `README <https://github.com/open-datastudio/spark-serverless/blob/master/README.md#how-to-use-staroid>`_ for more details.


.. include:: ../../ref.rst
