:man_page: mongoc_write_concern_set_w

mongoc_write_concern_set_w()
============================

Synopsis
--------

.. code-block:: c

  void
  mongoc_write_concern_set_w (mongoc_write_concern_t *write_concern, int32_t w);

Parameters
----------

* ``write_concern``: A :symbol:`mongoc_write_concern_t`.
* ``w``: A positive ``int32_t`` or zero.

Description
-----------

Sets the ``w`` value for the write concern. See :symbol:`mongoc_write_concern_t` for more information on this setting.

Unacknowledged writes are not causally consistent. If you execute a write operation with a :symbol:`mongoc_write_concern_t` on which you have called :symbol:`mongoc_write_concern_set_w` with a value of 0, the write does not participate in causal consistency, even when executed with a :symbol:`mongoc_client_session_t`.
