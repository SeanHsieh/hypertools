

.. _sphx_glr_auto_examples_plot_align.py:


=============================
Aligning matrices to a common space
=============================

In this example, we plot the trajectory of multivariate brain activity for
two groups of subjects that have been hyperaligned (Haxby et al, 2011).  First,
we use the align tool to project all subjects in the list to a common space.
Then we average the data into two groups, and plot.




.. image:: /auto_examples/images/sphx_glr_plot_align_001.png
    :align: center





.. code-block:: python


    # Code source: Andrew Heusser
    # License: MIT

    # import
    import hypertools as hyp
    import numpy as np

    # load example data
    data = hyp.load('weights', align='hyper')

    # average into two groups
    group1 = np.mean(data[:17], 0)
    group2 = np.mean(data[18:], 0)

    # plot
    hyp.plot([group1[:100, :], group2[:100, :]])

**Total running time of the script:** ( 0 minutes  5.365 seconds)



.. container:: sphx-glr-footer


  .. container:: sphx-glr-download

     :download:`Download Python source code: plot_align.py <plot_align.py>`



  .. container:: sphx-glr-download

     :download:`Download Jupyter notebook: plot_align.ipynb <plot_align.ipynb>`

.. rst-class:: sphx-glr-signature

    `Generated by Sphinx-Gallery <http://sphinx-gallery.readthedocs.io>`_
