.. amqpstorm documentation master file, created by
   sphinx-quickstart on Sun Apr 10 16:25:24 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

AMQPStorm3 Documentation
=======================
Thread-safe Python3 RabbitMQ Client & Management library.

Installation
------------
The latest version can be installed using `pip <https://pip.pypa.io/en/stable/quickstart/>`_ and is available at pypi `here <https://pypi.org/project/AMQPStorm3/>`_
::

    pip install amqpstorm3


You can also install AMQPStorm3 with the management dependencies using.
::

    pip install amqpstorm3[management]

Basic Example
-------------

::

   with amqpstorm3.Connection('rmq.eandersson.net', 'guest', 'guest') as connection:
       with connection.channel() as channel:
           channel.queue.declare('fruits')
           message = amqpstorm3.Message.create(
               channel, body='Hello RabbitMQ!', properties={
                   'content_type': 'text/plain'
               })
           message.publish('fruits')

Additional Examples
-------------------

A wide verity of examples are available on Github at `here <https://github.com/eandersson/amqpstorm/tree/master/examples>`_

.. toctree::
   :caption: Usage
   :name: usage

   usage/connection
   usage/channel
   usage/exceptions
   usage/message

.. toctree::
   :caption: Management API Usage
   :name: api_usage

   api_usage/api
   api_usage/exception

.. toctree::
   :glob:
   :caption: Examples
   :name: examples

   examples/*

.. toctree::
   :glob:
   :caption: Management Examples
   :name: management_examples

   management_examples/*

Issues
------
Please report any issues on Github `here <https://github.com/eandersson/amqpstorm3/issues>`_

Source
------
AMQPStorm3 source code is available on Github `here <https://github.com/eandersson/amqpstorm3>`_

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`