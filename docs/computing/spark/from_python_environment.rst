---------------------------------------------------
Spark cluster from your python environment
---------------------------------------------------

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/J43qKJnp_N8" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

|

Try in Google Colab
   .. image:: https://colab.research.google.com/assets/colab-badge.svg
      :target: https://colab.research.google.com/github/open-datastudio/ods/blob/master/notebook/open-data-studio.ipynb


|

Install
--------------------------

Install `ods <https://github.com/open-datastudio/ods>`_ package using pip command.

.. code-block:: bash

   $ pip install ods

And let's get an `access token <https://staroid.com/settings/accesstokens>`_ and set ``STAROID_ACCESS_TOKEN`` environment variable.

.. code-block:: bash

   $ export STAROID_ACCESS_TOKEN="<your access token>"

For alternative ways to configure access token, check `staroid-python <https://github.com/staroids/staroid-python#configuration>`_.

Create Kubernetes cluster
--------------------------

`staroid.com <https://staroid.com>`_  -> Products -> Kubernetes (SKE) -> New Kubernetes cluster.

.. image:: https://user-images.githubusercontent.com/1540981/87723637-ede8ac00-c76e-11ea-98d3-b6f8d972453d.png
   :width: 400

And configure kubernetes cluster name after import python library.

.. code-block:: python

   import ods
   # 'ske' is the name of kubernetes cluster created from staroid.com.
   # Alternatively, you can set the 'STAROID_SKE' environment variable.
   ods.init(ske="data-team1")


Create PySpark session
-----------------------

Spark-serverless enables you to create an interactive PySpark sessions with executors running on the cloud remotely.

.. code-block:: python

   import ods
   # 'ske' is the name of kubernetes cluster created from staroid.com.
   # Alternatively, you can set the 'STAROID_SKE' environment variable.
   ods.init(ske="data-team1")

   # get saprk session with 3 initial worker nodes, delta lake enabled
   spark = ods.spark("my-cluster", worker_num=3, delta=True).session()

   # Do your work with Spark session
   df = spark.read.load(...)

Now you can use Spark session with 3 remotely running executors.

.. note::

     There's no application packaging and submit step required. Everything runs interactively.


.. include:: ../../ref.rst
