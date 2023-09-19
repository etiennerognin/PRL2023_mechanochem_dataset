Supporting information and dataset for the paper "Theory of flow-induced covalent polymer mechanochemistry in dilute solutions"
===============================================================================================================================

This is the dataset and software supporting the study Theory of flow-induced
covalent polymer mechanochemistry in dilute solutions*
by Etienne Rognin, Niamh Willis-Fox, Ronan Daly, Institute for Manufacturing,
Department of Engineering, University of Cambridge, 17 Charles Babbage Road,
Cambridge CB3 0FS, United Kingdom.


Contents
--------

Main file
^^^^^^^^^

Use the Jupyter Notebook ``Supporting information.ipynb`` to run the data analysis
and recreate the figures of the paper.

Alternatively, open ``Supporting information.pdf`` to view the notebook outputs
in a PDF reader without having to install and run the scripts.

Raw data
^^^^^^^^

The folder ``bead-rod_dataset`` contains the results of bead-rod model simulations.
For each simulation there is binary Python ``.npz`` file containing the data, and
a text ``.json`` file containing metadata (such as date of the simulation, parameters...)

The data is imported using ``np.load`` function which creates a Python dictionary
for each simulation file. This dictionary contains the following labels:

1. ``t`` the time axis.
2. ``gradU`` the time series of velocity gradients used as forcing terms in the bead-rod simulation.
3. ``g_max`` the time series of the maximum tensile force, for each molecule of the simulation ensemble.
4. ``i_max`` the time series of the positions of the maximum force in the chain (not used in this study)
5. ``g_12`` the time series of the tensile force at the center of the chain, for each molecule.
6. ``A_average`` the time series of the average conformation tensor (second-order moment of the end-to-end vector). Used in section 4 for model validation.

Note that the bead-rod algorithm and dimension normalization are described in a
previous study (see Rognin et al. https://www.repository.cam.ac.uk/bitstream/1810/279443/1/multiscale_revision_clean.pdf)


License
-------
CC-BY-4.0

To view the full license, visit: https://creativecommons.org/licenses/by/4.0/legalcode


Installation
------------
In the target directory, clone this repository::

  git clone https://github.com/etiennerognin/flowmechanochem_dataset.git


Usage
-----

Run the notebook ``Supporting information.ipynb`` (you will need to have
Jupyter installed, see https://jupyter.org/)
