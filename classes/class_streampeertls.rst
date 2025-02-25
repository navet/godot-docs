:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/StreamPeerTLS.xml.

.. _class_StreamPeerTLS:

StreamPeerTLS
=============

**Inherits:** :ref:`StreamPeer<class_StreamPeer>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

TLS stream peer.

Description
-----------

TLS stream peer. This object can be used to connect to an TLS server or accept a single TLS client connection.

\ **Note:** When exporting to Android, make sure to enable the ``INTERNET`` permission in the Android export preset before exporting the project or using one-click deploy. Otherwise, network communication of any kind will be blocked by Android.

Tutorials
---------

- :doc:`TLS certificates <../tutorials/networking/ssl_certificates>`

Properties
----------

+-------------------------+----------------------------------------------------------------------------+----------+
| :ref:`bool<class_bool>` | :ref:`blocking_handshake<class_StreamPeerTLS_property_blocking_handshake>` | ``true`` |
+-------------------------+----------------------------------------------------------------------------+----------+

Methods
-------

+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Error<enum_@GlobalScope_Error>`    | :ref:`accept_stream<class_StreamPeerTLS_method_accept_stream>` **(** :ref:`StreamPeer<class_StreamPeer>` stream, :ref:`CryptoKey<class_CryptoKey>` private_key, :ref:`X509Certificate<class_X509Certificate>` certificate, :ref:`X509Certificate<class_X509Certificate>` chain=null **)**      |
+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Error<enum_@GlobalScope_Error>`    | :ref:`connect_to_stream<class_StreamPeerTLS_method_connect_to_stream>` **(** :ref:`StreamPeer<class_StreamPeer>` stream, :ref:`bool<class_bool>` validate_certs=false, :ref:`String<class_String>` for_hostname="", :ref:`X509Certificate<class_X509Certificate>` valid_certificate=null **)** |
+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                     | :ref:`disconnect_from_stream<class_StreamPeerTLS_method_disconnect_from_stream>` **(** **)**                                                                                                                                                                                                   |
+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Status<enum_StreamPeerTLS_Status>` | :ref:`get_status<class_StreamPeerTLS_method_get_status>` **(** **)** |const|                                                                                                                                                                                                                   |
+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`StreamPeer<class_StreamPeer>`      | :ref:`get_stream<class_StreamPeerTLS_method_get_stream>` **(** **)** |const|                                                                                                                                                                                                                   |
+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                     | :ref:`poll<class_StreamPeerTLS_method_poll>` **(** **)**                                                                                                                                                                                                                                       |
+------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Enumerations
------------

.. _enum_StreamPeerTLS_Status:

.. _class_StreamPeerTLS_constant_STATUS_DISCONNECTED:

.. _class_StreamPeerTLS_constant_STATUS_HANDSHAKING:

.. _class_StreamPeerTLS_constant_STATUS_CONNECTED:

.. _class_StreamPeerTLS_constant_STATUS_ERROR:

.. _class_StreamPeerTLS_constant_STATUS_ERROR_HOSTNAME_MISMATCH:

enum **Status**:

- **STATUS_DISCONNECTED** = **0** --- A status representing a ``StreamPeerTLS`` that is disconnected.

- **STATUS_HANDSHAKING** = **1** --- A status representing a ``StreamPeerTLS`` during handshaking.

- **STATUS_CONNECTED** = **2** --- A status representing a ``StreamPeerTLS`` that is connected to a host.

- **STATUS_ERROR** = **3** --- A status representing a ``StreamPeerTLS`` in error state.

- **STATUS_ERROR_HOSTNAME_MISMATCH** = **4** --- An error status that shows a mismatch in the TLS certificate domain presented by the host and the domain requested for validation.

Property Descriptions
---------------------

.. _class_StreamPeerTLS_property_blocking_handshake:

- :ref:`bool<class_bool>` **blocking_handshake**

+-----------+---------------------------------------+
| *Default* | ``true``                              |
+-----------+---------------------------------------+
| *Setter*  | set_blocking_handshake_enabled(value) |
+-----------+---------------------------------------+
| *Getter*  | is_blocking_handshake_enabled()       |
+-----------+---------------------------------------+

.. container:: contribute

	There is currently no description for this property. Please help us by :ref:`contributing one <doc_updating_the_class_reference>`!

Method Descriptions
-------------------

.. _class_StreamPeerTLS_method_accept_stream:

- :ref:`Error<enum_@GlobalScope_Error>` **accept_stream** **(** :ref:`StreamPeer<class_StreamPeer>` stream, :ref:`CryptoKey<class_CryptoKey>` private_key, :ref:`X509Certificate<class_X509Certificate>` certificate, :ref:`X509Certificate<class_X509Certificate>` chain=null **)**

Accepts a peer connection as a server using the given ``private_key`` and providing the given ``certificate`` to the client. You can pass the optional ``chain`` parameter to provide additional CA chain information along with the certificate.

----

.. _class_StreamPeerTLS_method_connect_to_stream:

- :ref:`Error<enum_@GlobalScope_Error>` **connect_to_stream** **(** :ref:`StreamPeer<class_StreamPeer>` stream, :ref:`bool<class_bool>` validate_certs=false, :ref:`String<class_String>` for_hostname="", :ref:`X509Certificate<class_X509Certificate>` valid_certificate=null **)**

Connects to a peer using an underlying :ref:`StreamPeer<class_StreamPeer>` ``stream``. If ``validate_certs`` is ``true``, ``StreamPeerTLS`` will validate that the certificate presented by the peer matches the ``for_hostname``.

\ **Note:** Specifying a custom ``valid_certificate`` is not supported in Web exports due to browsers restrictions.

----

.. _class_StreamPeerTLS_method_disconnect_from_stream:

- void **disconnect_from_stream** **(** **)**

Disconnects from host.

----

.. _class_StreamPeerTLS_method_get_status:

- :ref:`Status<enum_StreamPeerTLS_Status>` **get_status** **(** **)** |const|

Returns the status of the connection. See :ref:`Status<enum_StreamPeerTLS_Status>` for values.

----

.. _class_StreamPeerTLS_method_get_stream:

- :ref:`StreamPeer<class_StreamPeer>` **get_stream** **(** **)** |const|

Returns the underlying :ref:`StreamPeer<class_StreamPeer>` connection, used in :ref:`accept_stream<class_StreamPeerTLS_method_accept_stream>` or :ref:`connect_to_stream<class_StreamPeerTLS_method_connect_to_stream>`.

----

.. _class_StreamPeerTLS_method_poll:

- void **poll** **(** **)**

Poll the connection to check for incoming bytes. Call this right before :ref:`StreamPeer.get_available_bytes<class_StreamPeer_method_get_available_bytes>` for it to work properly.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
