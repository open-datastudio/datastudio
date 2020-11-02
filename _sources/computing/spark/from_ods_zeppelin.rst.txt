---------------------------------------------------
Spark cluster from Open data studio Zeppelin
---------------------------------------------------

.. raw:: html

   <iframe width="560" height="315" src="https://www.youtube.com/embed/JuEkv5oEsFo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

|

Open data studio :ref:`Apache Zeppelin` integrates Spark 3.x out of the box.
Extra installation/initialization steps are not required.

.. image:: https://user-images.githubusercontent.com/1540981/80290438-cf3bc180-86f9-11ea-8c1f-d2dedcd48a86.png
   :width: 600

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
