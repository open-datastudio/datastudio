===============================================
Ray cluster from Staroid management console GUI
===============================================

Ray cluster can be managed from `Instance management menu <https://staroid.com/g/open-datastudio/ray-cluster/instances>`_
without using Ray CLI (Command Line Interface).

Start a Ray cluster from GUI
----------------------------

Click ``Launch`` button from `Instance management menu <https://staroid.com/g/open-datastudio/ray-cluster/instances>`_.

.. image:: https://user-images.githubusercontent.com/1540981/101434974-65ef7400-38c0-11eb-8647-22a4a11ca2e1.png
   :width: 500
   :alt: Ray cluster launch dialog

In a launch dialog, you can configure a name of your Ray cluster instance, number of max workers and so on.
Once launched, you can see status of your Ray cluster instance.

.. note::

   Ray cluster takes few seconds to a couple of minutes to fully initialized.
   During initialization, it performs node provisioning, downloading Ray container image and executing bootstrap commands.

Access Ray dashboard and Jupyter notebook
-----------------------------------------

Once your Ray cluster instance is fully initialized,
you'll see link to the Ray dashbaord and Jupyter notebook.

.. image:: https://user-images.githubusercontent.com/1540981/101435650-8f5ccf80-38c1-11eb-8619-ea448c33a50e.png
   :width: 600

In the Jupyter notebook, ray environment is pre-configured so you can just run

.. code-block:: python

   import ray
   ray.init()  # no 'address' parameter required :)

and use Ray cluster environment.


Stop Ray cluster instance
--------------------------

In `Instance management menu <https://staroid.com/g/open-datastudio/ray-cluster/instances>`_ menu,
You can find ``Stop`` (``Start``) and ``Terminate`` button.

Stop
    Stop Ray head and all workers. Can be (re)started later. Data stored in persistent volume is not removed.

Terminate
    Stop Ray head and all workers permanently. Can not be restarted. Data stored in persistent volume is also removed.
