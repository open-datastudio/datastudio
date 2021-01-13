=========================================
Ray cluster from Ray Cluster Launcher CLI
=========================================

Ray master branch includes `Ray cluster launcher for Staroid <https://docs.ray.io/en/master/cluster/cloud.html#staroid>`_.
This allows creating a ray cluster using standard ``ray up <cluster configuration yaml>`` CLI command.

Install Ray and dependency libraries
------------------------------------

First, install ray (1.1.0 or newer) and python dependency packages.

.. code-block:: bash

   $ pip install ray staroid kubernetes

Configure Staroid access token
------------------------------

Then, let's configure staroid access token. `Get access token <https://staroid.com/settings/accesstokens>`_ and set
``STAROID_ACCESS_TOKEN`` environment variable.

.. code-block:: bash

   $ export STAROID_ACCESS_TOKEN=[your access token]

Cluster configuration file
--------------------------

We can get example Ray cluster launcher configuration files for Staroid from Ray source tree.

.. code-block:: bash

   $ git clone https://github.com/ray-project/ray.git
   $ ls ray/python/ray/autoscaler/staroid/example-*.yaml

Open example configurations and modify them as you need.

Start a Ray cluster
-------------------

Now, you can create a Ray cluster using ``ray up`` command.

.. code-block:: bash

   $ ray up ray/python/ray/autoscaler/staroid/example-full.yaml

Once cluster is up and running, you can attach your shell to the Ray head node.

.. code-block:: bash

   $ ray attach ray/python/ray/autoscaler/staroid/example-full.yaml

Ray instance management menu
----------------------------

Check `Instance management menu <https://staroid.com/g/open-datastudio/ray-cluster/instances>`_.
You'll see your Ray cluster instances.

.. image:: https://user-images.githubusercontent.com/1540981/101430734-71d83780-38ba-11eb-94d4-f7b20f0135ae.png
   :width: 600

You'll find link to Ray dashbord and Jupyter notebook.


Shutdown Ray cluster
--------------------

To shutdown cluster,

.. code-block:: bash

   $ ray down ray/python/ray/autoscaler/staroid/example-full.yaml
