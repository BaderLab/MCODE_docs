=========================
Fine-Tuning Your Analysis
=========================

By default, MCODE analyzes networks using scoring and finding parameters that have been optimized to produce the best results for the average user and network.
However, you may achieve better results for your network by familiarizing yourself with these parameters and changing them appropriately.
Sometimes even slight customizations can produce considerable differences, reduce unwanted or false results, and increase relevance of results.
This is only an overview -- for detailed parameter information, consult the MCODE paper.

The user can analyze a network as many times as desired with varying parameters.
Each result is reported sequentially for reference and comparison.
Viewing different results will automatically rewrite the MCODE node attributes and re-visualize the network appropriately.

.. note:: For efficiency purposes, MCODE automatically determines which portion of the algorithm needs to be run based on the user's parameter modifications.
          
          For instance, if the scoring parameters are altered, the network will be re-scored,
          but if only the cluster finding parameters are altered, only the cluster finding portion will be run.
