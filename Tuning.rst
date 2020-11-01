.. _fine-tuning:

=========================
Fine-Tuning Your Analysis
=========================

By default, MCODE analyzes networks using scoring and finding parameters that have been optimized to produce the best results for the average user and network.
However, you may achieve better results for your network by familiarizing yourself with these parameters and changing them appropriately.
Sometimes even slight customizations can produce considerable differences, reduce unwanted or false results, and increase relevance of results.
This is only an overview -- for detailed parameter information, consult the `MCODE paper <https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-4-2>`_.

  - The user can analyze a network as many times as desired with varying parameters.
  - Each result is reported sequentially for reference and comparison.
  - Each result creates a set of 3 "MCODE" *Node* columns, where ``n`` is the *result number*:

    - Score (``n``)
    - Node Status (``n``)
    - Clusters (``n``)

    .. figure:: images/mcode_columns.png
       :align: center

.. note:: For efficiency purposes, MCODE automatically determines which portion of the algorithm needs to be run based on the user's parameter modifications.

          - For instance, if the scoring parameters are altered, the network will be re-scored,
            but if only the cluster finding parameters are altered, only the cluster finding portion will be run.

These analyzes parameters are found in the *New Analysis Dialog*, as mentioned in the section :ref:`running`.

--------------------------
Network Scoring Parameters
--------------------------

  .. figure:: images/network_scoring_params.png
     :width: 40%
     :align: center

  1. **Include Loops**

    - When turned on, MCODE will include loops (self-edges) in the neighbourhood density calculation.
      This is expected to make a small difference in the results.

  2. **Degree Cutoff**

    - This value controls the minimum degree (number of connections) necessary in order for a node to be scored.

        - For example, nodes that share only one connection with one other node have a degree of *1*.
        - Valid values are *2* or higher to prevent singly connected nodes from getting an artificially high node score.

.. _cluster-finding-params:

--------------------------
Cluster Finding Parameters
--------------------------

  .. figure:: images/cluster_finding_params.png
     :width: 40%
     :align: center

  1. **Haircut**

    - Once a cluster has been found, some nodes which may have satisfied the **Degree Cutoff** parameter during scoring
      may only be connected to the cluster by one edge.
      When haircut is turned on, MCODE removes all such singly-connected nodes from clusters.
      In some cases, though rare, the cluster's seed node may be only singly connected to the cluster and removed by the Haircut.
      For example, Cluster 2 of the *galFiltered.gml* network with default settings is one such case.

  2. **Fluff**

    - When turned on, MCODE expands cluster cores by one neighbour shell outwards, according to the fluff
      **Node Density Cutoff** parameter and after the optional haircut step.
    - If this parameter is turned on, some nodes may belong to more than one cluster.

  3. **Node Density Cutoff**

    - Node density is calculated by dividing the node's connections by the maximum number of connections possible for that node.
      If Fluff is turned on, this parameter controls the neighbour inclusion criteria during 'fluffing'.
      Fluff expansion occurs after the cluster has already been defined by the algorithm and thus allows clusters to overlap at their edges.
      A higher value will expand clusters more.

  4. **Node Score Cutoff**

    - This is the most influential parameter for cluster size and is the basis for the **Size Threshold** slider in the :ref:`interpreting_results` section.
    - During cluster expansion, new members are added only if their node score deviates from the cluster's seed node's score by less than the set cutoff.
      This is a percentage, where a value of 0.2 allows for new members' node scores to be no more than 20% less than that of the seed node.
      Thus, smaller values create smaller clusters and vice versa.

  5. **K-Core**

    - This parameter filters out clusters that do not contain a maximally inter-connected sub-cluster of at least k degrees.
      For example, a triangle (3 nodes, 3 edges) is a 2-core (2 connections per node).
      Two nodes with 2 edges between them satisfy the 2-core rule as well. Since the default value is 2, this ensures that clusters must in the very least contain one of these two sub-clusters.
      Increasing this value will exclude smaller clusters.

  6. **Max. Depth**

    - Maximum depth limits the distance from the seed node within which MCODE can search for cluster members.
      By default this is set to an arbitrarily large number so that clusters are virtually unlimited.
      To limit cluster size, set this parameter to a small number.
