=========================================
Ray cluster from Ray Cluster Launcher CLI
=========================================

Ray master branch includes `Ray cluster launcher for Staroid <https://docs.ray.io/en/master/cluster/cloud.html#staroid>`_.
This allows creating a ray cluster using standard ``ray up <cluster configuration yaml>`` CLI command.

First, install python dependency packages.

.. code-block:: bash

   $ pip install ray staroid kubernetes

Since Staroid cloud provider is available from Ray 1.1.0, let's install 1.1.0 snapshot.

.. code-block:: bash

   $ ray install nightly

or

.. code-block:: bash

   $ pip install -U [link to wheel]

See instructions https://docs.ray.io/en/latest/installation.html#latest-snapshots-nightlies.

Then, let's configure staroid access token. `Get access token <https://staroid.com/settings/accesstokens>`_ and set
``STAROID_ACCESS_TOKEN`` environment variable.

.. code-block:: bash

   $ export STAROID_ACCESS_TOKEN=[your access token]

We can get example Ray cluster launcher configuration files for Staroid from Ray source tree.

.. code-block:: bash

   $ git clone https://github.com/ray-project/ray.git
   $ ls ray/python/ray/autoscaler/staroid/example-*.yaml

Open example configurations and modify them as you need.
And then, you can create a Ray cluster using ``ray up`` command.

.. code-block:: bash

   $ ray up ray/python/ray/autoscaler/staroid/example-full.yaml

Once cluster is up and running, you can attach your shell to the Ray head node.

.. code-block:: bash

   $ ray attach ray/python/ray/autoscaler/staroid/example-full.yaml

To shutdown cluster,

.. code-block:: bash

   $ ray down ray/python/ray/autoscaler/staroid/example-full.yaml
