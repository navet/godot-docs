:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/modules/openxr/doc_classes/OpenXRHand.xml.

.. _class_OpenXRHand:

OpenXRHand
==========

**Inherits:** :ref:`Node3D<class_Node3D>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

Node supporting finger tracking in OpenXR.

Description
-----------

This node enables OpenXR's hand tracking functionality. The node should be a child node of an :ref:`XROrigin3D<class_XROrigin3D>` node, tracking will update its position to where the player's actual hand is positioned. This node also updates the skeleton of a properly skinned hand model. The hand mesh should be a child node of this node.

Properties
----------

+-------------------------------------------------+---------------------------------------------------------------+------------------+
| :ref:`Hands<enum_OpenXRHand_Hands>`             | :ref:`hand<class_OpenXRHand_property_hand>`                   | ``0``            |
+-------------------------------------------------+---------------------------------------------------------------+------------------+
| :ref:`NodePath<class_NodePath>`                 | :ref:`hand_skeleton<class_OpenXRHand_property_hand_skeleton>` | ``NodePath("")`` |
+-------------------------------------------------+---------------------------------------------------------------+------------------+
| :ref:`MotionRange<enum_OpenXRHand_MotionRange>` | :ref:`motion_range<class_OpenXRHand_property_motion_range>`   | ``0``            |
+-------------------------------------------------+---------------------------------------------------------------+------------------+

Enumerations
------------

.. _enum_OpenXRHand_Hands:

.. _class_OpenXRHand_constant_HAND_LEFT:

.. _class_OpenXRHand_constant_HAND_RIGHT:

.. _class_OpenXRHand_constant_HAND_MAX:

enum **Hands**:

- **HAND_LEFT** = **0** --- Tracking the player's left hand.

- **HAND_RIGHT** = **1** --- Tracking the player's right hand.

- **HAND_MAX** = **2** --- Maximum supported hands.

----

.. _enum_OpenXRHand_MotionRange:

.. _class_OpenXRHand_constant_MOTION_RANGE_UNOBSTRUCTED:

.. _class_OpenXRHand_constant_MOTION_RANGE_CONFORM_TO_CONTROLLER:

.. _class_OpenXRHand_constant_MOTION_RANGE_MAX:

enum **MotionRange**:

- **MOTION_RANGE_UNOBSTRUCTED** = **0** --- When player grips, hand skeleton will form a full fist.

- **MOTION_RANGE_CONFORM_TO_CONTROLLER** = **1** --- When player grips, hand skeleton conforms to the controller the player is holding.

- **MOTION_RANGE_MAX** = **2** --- Maximum supported motion ranges.

Property Descriptions
---------------------

.. _class_OpenXRHand_property_hand:

- :ref:`Hands<enum_OpenXRHand_Hands>` **hand**

+-----------+-----------------+
| *Default* | ``0``           |
+-----------+-----------------+
| *Setter*  | set_hand(value) |
+-----------+-----------------+
| *Getter*  | get_hand()      |
+-----------+-----------------+

Specifies whether this node tracks the left or right hand of the player.

----

.. _class_OpenXRHand_property_hand_skeleton:

- :ref:`NodePath<class_NodePath>` **hand_skeleton**

+-----------+--------------------------+
| *Default* | ``NodePath("")``         |
+-----------+--------------------------+
| *Setter*  | set_hand_skeleton(value) |
+-----------+--------------------------+
| *Getter*  | get_hand_skeleton()      |
+-----------+--------------------------+

Set a :ref:`Skeleton3D<class_Skeleton3D>` node for which the pose positions will be updated.

----

.. _class_OpenXRHand_property_motion_range:

- :ref:`MotionRange<enum_OpenXRHand_MotionRange>` **motion_range**

+-----------+-------------------------+
| *Default* | ``0``                   |
+-----------+-------------------------+
| *Setter*  | set_motion_range(value) |
+-----------+-------------------------+
| *Getter*  | get_motion_range()      |
+-----------+-------------------------+

Set the motion range (if supported) limiting the hand motion.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
