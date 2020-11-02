---------------------------------------------------
Spark cluster from your python environment
---------------------------------------------------

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/J43qKJnp_N8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

|

Install
--------------------------

.. code-block:: bash

   $ pip install ods

``ods`` package uses `staroid python library <https://github.com/staroids/staroid-python>`_.
`Get access token <https://staroid.com/settings/accesstokens>`_ and set ``STAROID_ACCESS_TOKEN`` environment variable to configure it.

.. code-block:: bash

   $ export STAROID_ACCESS_TOKEN="<your access token>"

You can find alternative way to configure Staroid package. `Learn more <https://github.com/staroids/staroid-python#configuration>`_.

Initialize
--------------------------

.. code-block:: python

   import ods
   # 'ske' is the name of kubernetes cluster created from staroid.com.
   # Alternatively, you can set the 'STAROID_SKE' environment variable.
   ods.init(ske="kube-cluster-1")


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
