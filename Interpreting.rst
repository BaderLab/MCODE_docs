================================
Getting and Interpreting Results
================================

This section covers some of the basic steps of running MCODE on a network.

--------------------
1. Load Your Network
--------------------

  To begin, load the network to be analyzed into Cytoscape.
  You can load as many networks as your computer system can handle, large or small.

  MCODE will analyze the *current* network, which is usually the network that is selected
  in Cytoscape's **Network** tab (left-hand panel) or the network *View* that is currently rendered.

------------------------------
2. Choose The Analysis Options
------------------------------

  2.1. Go to the **MCODE Panel**.

  2.2. Click the **New Analysis** button to open the *New Analysis Dialog*.

  2.3. Choose The Scope:

    Clusters can be found in the entire network or from a selection of nodes.
    Chose one of these options in the **Find Clusters** section of the *New Analysis Dialog*:

      - **Find Clusters in Whole Network**
        - MCODE will find and report all clusters in the entire network.
      - **Find Clusters from Selection**
        - Only those clusters which include the selected node(s) within them will be reported.
        - Selections can be made either directly in the view, the *Node Table* or Cytoscape's handy search tools.

    .. note:: The choice of scope is dependent on your familiarity with the network in question and the desired outcome.
              If you have a particular protein of interest within a network, for example, it may be appropriate to search
              for only those clusters involving such a protein.
              On the other hand, exploratory work will benefit most from analyzing the whole network.

-----------------------
3. Analyze Your Network
-----------------------

  3.1. Click the **Analyze Current Network** button:

    If everything is OK, this will display a progress meter of the scoring, finding, and drawing steps,
    provided that the task is not too quick.

    However, the analysis cannot be performed in some situations, where you may see these *Analysis Interrupted* messages:

      a) *No Selection* Message

        - This message appears when the *From Selection* scope is used without an actual node selection.
        - You must select the desired node(s) and try again before MCODE can attempt to find clusters.

      b) *Parameters Unchanged* Message

        - Parameters are discussed in detail in the following section.
          For now, you should know that if you attempt to analyze a network twice without changing any of the settings,
          such as the scope of the analysis, MCODE will let you know that this analysis was previously conducted.

----------------------
4. Browse Your Results
----------------------

  If the analysis finds clusters, the result will be added to MCODE's main panel as "1 - *NETWORK_NAME*".
