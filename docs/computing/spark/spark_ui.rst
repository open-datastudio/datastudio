===============
Access Spark UI
===============

Access Spark UI locally
-----------------------

While Spark-serverless keeps Spark driver running on your python environment (client-side),
you can simply browse ``localhost:4040`` (or subsequent port numbers) to access Spark UI when you are using your laptop.


Access Spark UI remotely
------------------------

If you're using some environment that accesses to the other local ports are limited
(for example, notebook environment on the cloud, such as Google Colab) or you'd like to share
your Spark UI with your team, you can find a Spark UI link, when you open a detail view of your instance
from `Instance management menu <https://staroid.com/g/open-datastudio/spark-serverless/instances>`_.

.. image:: https://user-images.githubusercontent.com/1540981/100956146-af108400-34cc-11eb-9ee5-1e8dd9937694.png
   :width: 600
