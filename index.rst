MCODE Cytoscape App 2.0
===============================

.. _The EnrichmentMap Protocol: https://baderlab.github.io/Cytoscape_workflows/EnrichmentMapPipeline/index.html

|screenshot1| |screenshot2|

MCODE is a `Cytoscape <https://cytoscape.org/>` app that finds clusters (highly interconnected regions) in a network.
Clusters mean different things in different types of networks.
For instance, clusters in a protein-protein interaction network are often protein complexes and parts of pathways,
while clusters in a protein similarity network represent protein families.
Cytoscape is freely available network visualization and analysis software.

MCODE is a relatively fast method of clustering.
With an intuitive interface, it is suited for both computationally and biologically oriented researchers.
Current features include:

* Fast network clustering
* Fine-tuning of results with numerous node-scoring and cluster-finding parameters
* Interactive cluster boundary and content exploration
* Multiple result set management
* Cluster sub-network creation and plain text export

Currently, MCODE does not provide any statistical score on the resulting clusters
but can be used as a discovery tool in network analysis.
Please see the `MCODE paper <https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-4-2>` for more information.


.. |screenshot1| image:: images/index/screenshot_1.png
   :width: 45%

.. |screenshot2| image:: images/index/screenshot_2.png
   :width: 45%


Feature Requests and Reporting Bugs
-----------------------------------

The MCODE GitHub issue tracker can be used to report a bug or request a feature.

To Report a bug:

* Go to https://github.com/BaderLab/MCODE/issues
* Click on *New Issue*
* Write a short description of the issue. It is very helpful to provide a series of steps
  that can be taken to reproduce the issue.
* If possible attach a session file (.cys) or example input files.
* Enter App version, Cytoscape version and operating system.
* Click on *Submit new issue*


Cite MCODE
------------------

. . BMC Bioinformatics. 2003 Jan 13;4:2. doi: 10.1186/1471-2105-4-2. Epub 2003 Jan 13. PMID: 12525261; PMCID: PMC149346.

* | **An automated method for finding molecular complexes in large protein interaction networks**
  | Bader GD, Hogue CW
  | `BMC Bioinformatics. 2003 Jan 13;4:2 <https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-4-2>`_.
  | `PubMed Abstract <https://pubmed.ncbi.nlm.nih.gov/12525261/>`_.



.. toctree::
   :maxdepth: 2
   :caption: User Guide:

   Installation
   Running
   Interpreting
   Tuning
   Exploring
   Outputting


.. toctree::
   :maxdepth: 2
   :caption: Links:

   Cytoscape.org <https://cytoscape.org>
   Cytoscape App Store <https://apps.cytoscape.org/apps/mcode>
   Baderlab.org <http://baderlab.org>
   GitHub <https://github.com/BaderLab/MCODE>
