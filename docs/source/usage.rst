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

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

