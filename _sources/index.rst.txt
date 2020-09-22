|ods-logo| Open Data Studio
==================================

Open data studio is a managed computing service on Staroid_ cloud. Run your machine learning workloads without managing clusters and servers.

|

Technology
------------

Use all the latest machine learning technology in a single place.
Open data studio continues to integrate the best technologies for machine learning.

|spark-logo| |ray-logo| |dask-logo| |delta-logo| |cuda-logo|

.. |spark-logo| image:: ./_static/spark-logo.png
   :width: 80px
   :alt: Apache spark

.. |dask-logo| image:: ./_static/dask-logo.png
   :width: 100px
   :alt: Dask

.. |ray-logo| image:: ./_static/ray-logo.png
   :width: 100px
   :alt: Ray

.. |delta-logo| image:: ./_static/delta-logo.png
   :width: 70px
   :alt: Delta lake

.. |cuda-logo| image:: ./_static/cuda-logo.png
   :width: 70px
   :alt: Nvidia CUDA

|

Easy of use
-----------

Access to the latest machine learning technology shouldn't be more than a few clicks or a few lines of code away.

.. code-block:: python
   :caption: Install, configure and spinup spark cluster with 3 remotely running workers

   import ods
   spark = ods.spark("my-spark", worker_num=3).session()

|


Fully managed
-------------

Save time and reduce risk.
Open data studio is maintained by the committers of the open source project and industry experts
on top of secure, reliable, and high performance cloud platform Staroid_.

|

Open source
-----------

Open data studio is an open source project.
You can easily see source code, understand how it works, and get involved.
When you need, fork and get your own version of managed service!

|

.. toctree::
   :maxdepth: 2

   about/index
   notebook/index
   data-lake/index
   computing/index
   machine-learning/index
   business-intelligence/index

.. include:: ./ref.rst

.. |ods-logo| image:: ./_static/open-datastudio-logo.png
   :width: 60px
   :alt: Open Datastudio
