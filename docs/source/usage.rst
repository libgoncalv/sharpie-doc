Usage
=====

.. _installation:

Installation
------------

To use SHARPIE, we highly recommend to use a virtual environment such as Anaconda. If you have already installed Anaconda:

.. code-block:: console

   conda create -n sharpie_env python=3.11
   conda activate sharpie_env

Then, git clone the SHARPIE repository:

.. code-block:: console

   git clone https://github.com/hybrid-intelligence/SHARPIE.git

Install Redis server:

.. code-block:: console

   # On Ubuntu
   sudo apt-get install redis-server & redis-server

Navigate to the SHARPIE directory and install the required packages:

.. code-block:: console

   cd SHARPIE
   pip install -r requirements.txt

Run in development mode
----------------

Start the web server:

.. code-block:: console

   cd webserver
   python manage.py runserver

In another terminal, start the runner:

.. code-block:: console

   cd runner
   python manage.py runserver

You can access the website at http://localhost:8000 and manage the authorized users from http://localhost:8000/admin with the username "admin" and password "password". For now there is no experiment available but you can find some examples ready to use in our `galery <https://github.com/hybrid-intelligence/SHARPIE_Gallery/>`_!