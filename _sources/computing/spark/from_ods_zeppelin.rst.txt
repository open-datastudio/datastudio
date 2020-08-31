---------------------------------------------------
Spark cluster from Open data studio Zeppelin
---------------------------------------------------

Open data studio :ref:`Apache Zeppelin` integrates Spark 3.0 out of the box.
Extra installation/initialization steps are not required.

Launch and use spark interpreter. Spark cluster will be automatically created.

.. code-block:: bash
   :caption: configure spark executors

   %spark.conf
   spark.executor.instances 3


.. code-block:: scala
   :caption: run spark api

   %spark
   // 'sc' and 'spark' are automatically created
   spark.read.json(...)


Check :ref:`Apache Zeppelin` for more details.
