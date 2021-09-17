############################################################
Joining, Smoothing, and Baking
############################################################

.. image:: ../images/baking_intro_before.jpg
  :alt: A Shipwright Object Before Baking

.. image:: ../images/baking_intro.jpg
  :alt: A Baked Shipwright Object

Because the Shipwright creates multiple objects, the joining and baking operations are designed to help you merge all these objects into one mesh and to apply smoothing operations if you choose to further sculpt or deform the image in any way.

*****************
Joining
*****************

.. image:: ../images/join_obj_btn.jpg
    :alt: Join Object button

The *Join* button when activated will automatically combine all the objects created in the Shipwright into one.

.. figure:: ../images/unjoined.jpg
  :alt: A Shipwright Joined

  The Shipwright unjoined with multiple objects.

.. figure:: ../images/joined.jpg
  :alt: A Shipwright Unjoined

  The Shipwright merged together with the Join operation.

*****************
Smoothing
*****************
.. warning::
    The Smoothing operation is a processor intensive operation at lower Voxel settings, and can cause Blender to freeze for a long period of time.

    Materials are not carried over during the operation as the object's topology is completely remapped.

.. figure:: ../images/smoothing_op.jpg
  :alt: A Shipwright with Smoothing Operations applied

  A Shipwright object with Smoothing Operations applied.

.. image:: ../images/smoothing_props.jpg
  :alt: A Shipwright with Smoothing Operations applied

When :ref:`Joined<Joining>` into one object, the Shipwright can automatically add the `Remesh <https://docs.blender.org/manual/en/latest/modeling/modifiers/generate/remesh.html>`_  and `Smooth <https://docs.blender.org/manual/en/latest/modeling/modifiers/deform/smooth.html>`_ modifiers to the object when the **Apply Smoothing** button is activated.  

This creates smoothed mesh that can then be used for sculpting.

Parameters are as follows:

* **Voxel Size**: The *Remesh* modifier uses Voxels (3D Pixels) to determine how to alter the mesh topology.  Smaller values will produce higher levels of detail but will take longer to process.  Be careful not to make the values too low (e.g., less than 0.01).
* **Smooth Iterations**:  This controls the number of times the *smooth* operation is applied to the retoplogised mesh.  Higher levels will produce a smoother result.

*****************
Baking
*****************

.. image:: ../images/baking_btns.jpg
  :alt: Final Baking Buttons

If you are ready for your Shipwright object to be taken to the next stage of editing in Blender and no longer wish for it to be changed through the panel, you can perform one of the following operations:

* **Remove Properties**:  This wll remove the properties from the object or objects so that the panel will no longer change it, leaving the deform lattice and any mirroring or other modifiers intact.
* **Collapse Shipwright**: This will remove the properties and also collapse all modifiers for the Shipwright object.