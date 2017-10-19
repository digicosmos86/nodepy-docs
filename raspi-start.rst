Setting up Raspberry Pi and SenseHAT
====================================

There are two ways to set up a Raspberry Pi.

From a Custom Image
---------------------

The easiest way to get Raspberry Pi and SenseHAT to work is to download our custom image from our download page.  This image will come with all software and hardware set up and read to go.  The only thing you will need to do is to expand your Linux partition by typing this command in the terminal:

.. code-block:: bash

   $ sudo raspi-config --expand-rootfs
   $ sudo reboot

From a Clean Raspbian or NOOBs Installation
-------------------------------------------

If you have a clean installation of Raspbian (or NOOBs) on your Raspberry Pi, you will need to confirm that you are running the latest Raspbian Stretch first:

.. code-block:: bash

   $ lsa-release -a

If your Raspberry Pi is not running Stretch, chances are that you do not have the SenseHAT extension for Stretch, or the Thorny Python IDE.  We highly recommend that you upgrade to Stretch.  `This official guide <https://www.raspberrypi.org/blog/raspbian-stretch/>`_ will show you how to upgrade.

If you already have Raspbian Stretch running, you will need to set up your locale, keyboard, and timezone.  You can do this with the `raspi-config` utility in your terminal, through System Settings, or with an automatic script:

.. code-block:: bash

   $ sudo bash <(curl -SL https://gist.githubusercontent.com/adoyle/71803222aff301da9662/raw/e40f2a447e0ae333801e6fddf5e6bdb7430c289d/raspi-init.sh)

If you need to use VNC, SSH, or i2c, you will have to manually enable them in `raspi-config`.

You will also need to update your Node-RED after this step. Although Node-RED comes pre-installed on the Raspberry Pi, this version is outdated and you will need to update node.js and Node-RED. Please click next and follow the next tutorial.