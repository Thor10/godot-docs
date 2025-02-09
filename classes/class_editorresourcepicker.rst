:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/EditorResourcePicker.xml.

.. _class_EditorResourcePicker:

EditorResourcePicker
====================

**Inherits:** :ref:`HBoxContainer<class_HBoxContainer>` **<** :ref:`BoxContainer<class_BoxContainer>` **<** :ref:`Container<class_Container>` **<** :ref:`Control<class_Control>` **<** :ref:`CanvasItem<class_CanvasItem>` **<** :ref:`Node<class_Node>` **<** :ref:`Object<class_Object>`

**Inherited By:** :ref:`EditorScriptPicker<class_EditorScriptPicker>`

Godot editor's control for selecting :ref:`Resource<class_Resource>` type properties.

.. rst-class:: classref-introduction-group

Description
-----------

This :ref:`Control<class_Control>` node is used in the editor's Inspector dock to allow editing of :ref:`Resource<class_Resource>` type properties. It provides options for creating, loading, saving and converting resources. Can be used with :ref:`EditorInspectorPlugin<class_EditorInspectorPlugin>` to recreate the same behavior.

\ **Note:** This :ref:`Control<class_Control>` does not include any editor for the resource, as editing is controlled by the Inspector dock itself or sub-Inspectors.

.. rst-class:: classref-reftable-group

Properties
----------

.. table::
   :widths: auto

   +---------------------------------+-----------------------------------------------------------------------------+-----------+
   | :ref:`String<class_String>`     | :ref:`base_type<class_EditorResourcePicker_property_base_type>`             | ``""``    |
   +---------------------------------+-----------------------------------------------------------------------------+-----------+
   | :ref:`bool<class_bool>`         | :ref:`editable<class_EditorResourcePicker_property_editable>`               | ``true``  |
   +---------------------------------+-----------------------------------------------------------------------------+-----------+
   | :ref:`Resource<class_Resource>` | :ref:`edited_resource<class_EditorResourcePicker_property_edited_resource>` |           |
   +---------------------------------+-----------------------------------------------------------------------------+-----------+
   | :ref:`bool<class_bool>`         | :ref:`toggle_mode<class_EditorResourcePicker_property_toggle_mode>`         | ``false`` |
   +---------------------------------+-----------------------------------------------------------------------------+-----------+

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`                           | :ref:`_handle_menu_selected<class_EditorResourcePicker_method__handle_menu_selected>` **(** :ref:`int<class_int>` id **)** |virtual|          |
   +---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+
   | void                                              | :ref:`_set_create_options<class_EditorResourcePicker_method__set_create_options>` **(** :ref:`Object<class_Object>` menu_node **)** |virtual| |
   +---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`PackedStringArray<class_PackedStringArray>` | :ref:`get_allowed_types<class_EditorResourcePicker_method_get_allowed_types>` **(** **)** |const|                                             |
   +---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+
   | void                                              | :ref:`set_toggle_pressed<class_EditorResourcePicker_method_set_toggle_pressed>` **(** :ref:`bool<class_bool>` pressed **)**                   |
   +---------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Signals
-------

.. _class_EditorResourcePicker_signal_resource_changed:

.. rst-class:: classref-signal

**resource_changed** **(** :ref:`Resource<class_Resource>` resource **)**

Emitted when the value of the edited resource was changed.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_signal_resource_selected:

.. rst-class:: classref-signal

**resource_selected** **(** :ref:`Resource<class_Resource>` resource, :ref:`bool<class_bool>` inspect **)**

Emitted when the resource value was set and user clicked to edit it. When ``inspect`` is ``true``, the signal was caused by the context menu "Edit" or "Inspect" option.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Property Descriptions
---------------------

.. _class_EditorResourcePicker_property_base_type:

.. rst-class:: classref-property

:ref:`String<class_String>` **base_type** = ``""``

.. rst-class:: classref-property-setget

- void **set_base_type** **(** :ref:`String<class_String>` value **)**
- :ref:`String<class_String>` **get_base_type** **(** **)**

The base type of allowed resource types. Can be a comma-separated list of several options.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_property_editable:

.. rst-class:: classref-property

:ref:`bool<class_bool>` **editable** = ``true``

.. rst-class:: classref-property-setget

- void **set_editable** **(** :ref:`bool<class_bool>` value **)**
- :ref:`bool<class_bool>` **is_editable** **(** **)**

If ``true``, the value can be selected and edited.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_property_edited_resource:

.. rst-class:: classref-property

:ref:`Resource<class_Resource>` **edited_resource**

.. rst-class:: classref-property-setget

- void **set_edited_resource** **(** :ref:`Resource<class_Resource>` value **)**
- :ref:`Resource<class_Resource>` **get_edited_resource** **(** **)**

The edited resource value.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_property_toggle_mode:

.. rst-class:: classref-property

:ref:`bool<class_bool>` **toggle_mode** = ``false``

.. rst-class:: classref-property-setget

- void **set_toggle_mode** **(** :ref:`bool<class_bool>` value **)**
- :ref:`bool<class_bool>` **is_toggle_mode** **(** **)**

If ``true``, the main button with the resource preview works in the toggle mode. Use :ref:`set_toggle_pressed<class_EditorResourcePicker_method_set_toggle_pressed>` to manually set the state.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_EditorResourcePicker_method__handle_menu_selected:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **_handle_menu_selected** **(** :ref:`int<class_int>` id **)** |virtual|

This virtual method can be implemented to handle context menu items not handled by default. See :ref:`_set_create_options<class_EditorResourcePicker_method__set_create_options>`.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_method__set_create_options:

.. rst-class:: classref-method

void **_set_create_options** **(** :ref:`Object<class_Object>` menu_node **)** |virtual|

This virtual method is called when updating the context menu of **EditorResourcePicker**. Implement this method to override the "New ..." items with your own options. ``menu_node`` is a reference to the :ref:`PopupMenu<class_PopupMenu>` node.

\ **Note:** Implement :ref:`_handle_menu_selected<class_EditorResourcePicker_method__handle_menu_selected>` to handle these custom items.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_method_get_allowed_types:

.. rst-class:: classref-method

:ref:`PackedStringArray<class_PackedStringArray>` **get_allowed_types** **(** **)** |const|

Returns a list of all allowed types and subtypes corresponding to the :ref:`base_type<class_EditorResourcePicker_property_base_type>`. If the :ref:`base_type<class_EditorResourcePicker_property_base_type>` is empty, an empty list is returned.

.. rst-class:: classref-item-separator

----

.. _class_EditorResourcePicker_method_set_toggle_pressed:

.. rst-class:: classref-method

void **set_toggle_pressed** **(** :ref:`bool<class_bool>` pressed **)**

Sets the toggle mode state for the main button. Works only if :ref:`toggle_mode<class_EditorResourcePicker_property_toggle_mode>` is set to ``true``.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
