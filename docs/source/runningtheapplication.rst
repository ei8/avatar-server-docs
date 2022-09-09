Running the Application
=======================

#.  Browse to http://LOCAL_IP_ADDRESS:64101/cortex/neurons.

#.  Regenerate the Graph:

    * Go to Docker → running sample container.

    * Browse to the CLI of the ``sample-cortex.graph.in.api-1`` container.

    * Run the below curl command to regenerate the graph.

    * ``curl --location --request POST 'http://127.0.0.1:80/cortex/graph/regenerate/' --header 'Content-Type:application/json;charset=UTF-8' --data-raw ''``
    
#.  Ensure that it executes successfully, if not, copy ``events.db`` file from ``sample-data`` folder and overwrite in the ``sample`` folder.

        .. image:: images/Picture10.png
            :width: 400

#.  The neuron app will be accessible at → http://LOCAL_IP_ADDRESS:64103/tree.

        .. image:: images/Picture11.png
            :width: 400

#.  Copy the URL → http://LOCAL_IP_ADDRESS:64101/cortex/neurons?pagesize=1000 and paste it into the neuron app and refresh.

        .. image:: images/Picture12.png
            :width: 400

#.  The app should display a valid UI.