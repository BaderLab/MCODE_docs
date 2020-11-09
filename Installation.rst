============
Installation
============

1. Install **Cytoscape**

  * Download and install the latest version of Cytoscape at `cytoscape.org <https://cytoscape.org/download.html>`_.

  .. note:: Cytoscape minimum version **3.8** is required for this version of MCODE.

            If you want to run MCODE on older versions of Cytoscape, the **App Manager** (see below)
            should show the latest compatible version of MCODE.

2. Install **MCODE**

  2.1. Automated Installation (via the **App Manager**)

    * Open Cytoscape.
    * In the main menu select **Apps > App Manager**.
    * In the App Manager select *MCODE* in the list of **all apps** and click the **Install** button.

    .. note:: MCODE can also be installed from the `Cytoscape App Store <https://apps.cytoscape.org/apps/mcode>`_.

  2.2. Manual Installation

    * Download the MCODE ``jar`` file from the `Cytoscape App Store <https://apps.cytoscape.org/apps/mcode>`_, where you have two options:

      a) Click the **Download** button on the MCODE app page to get the latest version.
      b) Go to the **Release History** section and click on the specific version you want to download.

    * Copy the downloaded *jar* file (e.g. ``mcode-app-2.0.0.jar``) to your ``[...]/CytoscapeConfiguration/3/apps/installed`` directory.
    * Check that **MCODE** appears in the **Apps** menu of Cytoscape. It may take a few seconds for the app to load up and appear in the menu.
      If it still does not appear, the most common causes are:

      a) You placed the MCODE *jar* file in the wrong directory.
      b) You may have one or more newer versions of MCODE already installed, in which case you just need to delete
         all the other ``mcode-[...].jar`` files you find in the ``installed`` directory.
      c) The downloaded version is not compatible with the running version of Cytoscape.
