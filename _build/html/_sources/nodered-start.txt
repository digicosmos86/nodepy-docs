Setting up Node-RED
===================

If you are using our custom image, please skip the section below. Node-RED is already set up on your Raspberry Pi.

Setting up Node-RED on Raspberry Pi
-----------------------------------

The easiest way to set up Node-RED on your Raspberry Pi is to use this command:

.. codeblock:: bash
   $ sudo bash <(curl -sL https://raw.githubusercontent.com/node-red/raspbian-deb-package/master/resources/update-nodejs-and-nodered)

You will also need to install some useful nodes as well:

.. codeblock:: bash
   $ sudo npm install -g node-red-dashboard
   $ sudo npm install -g node-red-contrib-python3-function
   $ sudo npm install -g node-red-contrib-web-worldmap

Setting up Node-RED on a Server
-------------------------------



