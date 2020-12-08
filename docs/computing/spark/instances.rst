===========================
Managing cluster instances
===========================

Spark serverless doesn't really need complex management or maintenance of the Spark cluster.
Upgrading, scaling-out, optimization, and other complex tasks are handled automatically.
Enjoy **zero maintenance** serverless experience.

All you need to do is simple task, such as Start or Stop cluster instances when you need.

Cluster instance management operations can be done 
either programmatically using Python client library or with mouse clicks from `Instance management menu <https://staroid.com/g/open-datastudio/spark-serverless/instances>`_.

Create a new Spark cluster instance
-----------------------------------

You can create multiple Spark serverless cluster instances in
one or more Kubernetes cluster (SKE). See :ref:`Create Kubernetes cluster` section to create a SKE.

You can create a cluster instance by creating a spark session from your Python environment.

Create spark session with the default configuration
    .. code-block:: python

        import ods
        ods.init(ske="my-ske")
        spark = ods.spark("my-cluster").session()

Create spark session with 3 initial worker nodes
    .. code-block:: python

        import ods
        ods.init(ske="my-ske")
        spark = ods.spark("my-cluster", worker_num=3).session()

Create spark session with delta lake support
    .. code-block:: python

        import ods
        ods.init(ske="my-ske")
        spark = ods.spark("my-cluster", delta=True).session()


.. note::

   ``pip install ods`` to install ods library.
   Python version 3.6, 3.7, 3.8 are supported.

Done! You have Spark session that is connected to executors running remotely on the cloud.
No application packaging and job submit to the cluster required.

Your Spark session is capable of doing interactive computing.
That means, you can use Spark session in Python REPL or in the Notebook.


.. note::

   It may take a few seconds to minutes for executors to be fully ready. See next section to monitor status of executors.


Spark cluster instance management menu
--------------------------------------

Open `Instance management menu <https://staroid.com/g/open-datastudio/spark-serverless/instances>`_
and you'll find Spark cluster instance automatically created by the Spark session.
You can also access :ref:`Access Spark UI` from here.

.. note::

   Log console and shell terminal is provided for more advanced usage as well.


Stop Spark cluster instance
-----------------------------

In `Instance management menu <https://staroid.com/g/open-datastudio/spark-serverless/instances>`_ menu,
You can find ``Stop`` (``Start``) and ``Terminate`` button.

Stop
    Stop all executors. Can be (re)started later. Data stored in persistent volume is not removed.

    Python API equivalent is

    .. code-block:: python

       # 'spark' is spark session created from 'spark = ods.spark("my-cluster").session()'
       spark.stop()

Terminate
    Stop all executors permanently. Can not be restarted. Data stored in persistent volume is also removed.

    Python API equivalent is

    .. code-block:: python

       ods.spark("my-cluster").delete()

