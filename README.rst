AMQPStorm3
==========
Thread-safe Python3 RabbitMQ Client & Management library.

|Version|

Introduction
============
AMQPStorm3 is a library designed to be consistent, stable and thread-safe.

- 100% Test Coverage!
- Supports Python 3.11+.
Why upgrade from amqpstorm to amqpstorm3?
=========================================

This release drops support for Python 2.7, allowing the library to
depend on a newer versions of ``pamqp`` and to resolve all deprecated
warnings.


Upgrade from amqpstorm to amqpstorm3
====================================

All imports of ``amqpstorm`` must be updated to ``amqpstorm3``.

For example, replace:

.. code-block:: python

    import amqpstorm

    ...

    amqpstorm.Connection(...)

with:

.. code-block:: python

    import amqpstorm3

    ...

    amqpstorm3.Connection(...)

Additionally, a new ``Connection`` parameter was introduced to control
the locale sent during connection negotiation.

Changelog
=========

Version 0.1
-------------
- Initial release.

.. |Version| image:: https://badge.fury.io/py/AMQPStorm3.svg
  :target: https://badge.fury.io/py/AMQPStorm3
