Debugging using Visual Studio
=============================

#.  Browse to the ``docker-compose.yml`` file of **avatar-server-pack** repository.

#.  Comment the whole ``d23.api`` section.

        .. image:: images/Picture13.png
            :width: 400

#.  Restart the docker containers and remove the orphans ``docker-compose -f docker-compose.yml up –remove-orphans``.
 
        .. image:: images/Picture14.png
            :width: 400

#.  Clone the **cortex-diary** repository.

        .. image:: images/Picture15.png
            :width: 400

#.  Open the solution in Visual Studio 2022 and perform the below steps:

    * Check ``var1.env`` file for any anomaly.
    * Check ``docker-compose.yml`` file for any anomaly.
    * Browse to the ``docker-compose-overrides.yml`` file and perform the below mentioned changes:

        * Update the Local IP.
        * Change the network name to ``sample_default``.
        * Change the avatars dB to point to the dB present in the ``\prod\sample`` directory of the **avatar-server-pack** directory.

                .. image:: images/Picture16.png
                    :width: 400

#.  Set start-up project as **docker-compose** project and run the project.

#.  Browse to http://LOCAL_IP_ADDRESS:64103/tree, the UI should be up.

#.  Open Port.Adapter project → UI → Views → Blazor → Pages → Tree.razor and put a breakpoint to the Reload() method.

#.  Refresh the UI and the breakpoint should hit.
