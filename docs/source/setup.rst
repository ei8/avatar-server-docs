Setup
=====

Avatar Server Pack
------------------

#.  Clone the **avatar-server-pack** repository.
        
        .. image:: images/Picture1.png
            :width: 400

#.  Browse to the ``avatars/prod/sample`` directory.


#.  Update the values in the following files:


    * .env - set **AVATAR_IP** and **D23_IP** to local IP address

        .. image:: images/Picture2.png
            :width: 400

    * d23-variables.env - set **BASE_PATH** to empty string

        .. image:: images/Picture3.png 
            :width: 400

    * Correct the ``d23.db`` data → delete records 2 to 4

        .. image:: images/Picture4.png
            :width: 400

ArangoDB
--------

#.  Install ``ArangoDB 3.3.7-1_win64.exe`` from https://download.arangodb.com/arangodb33/Windows7/x86_64/index.html.

#.  Navigate to http://127.0.0.1:8529/ ArangoDB in your browser.

    * Username → **root**
    * Password → **blank**
    * Database → **_system**

        .. image:: images/Picture5.png
            :width: 400

            
        .. image:: images/Picture6.png
            :width: 400

#.  Using File Explorer, browse to the path ``C:/Program Files/arangoDB 3.3.7/etc/arangodb3``.


#.  Open the file ``arango.conf`` and update the endpoint to ``tcp://0.0.0.0:8529``.

        .. image:: images/Picture7.png
            :width: 400

#.  Restart **arangodb** service.

        * Press ``Windows Key + R``.
        * Type ``services.msc``.
        * Choose ``ArangoDB > (Re)start service``. 

Docker Desktop
--------------

#.  Ensure Docker Desktop is up and online, check WSL status, and take remediation steps if Docker does not work.

        .. image:: images/Picture8.png
            :width: 400

#.  Ensure to switch on virtualization at the BIOS level if needed.

#.  Ensure Docker is running under Linux containers.

        .. image:: images/Picture9.png
            :width: 400

#.  Open the ``variables.env`` file from ``C:\ei8\avatars\prod\sample`` and update the contents from the dowloadable `variables.env <https://github.com/ei8/avatar-server-pack/blob/master/avatars/prod/sample/variables.env>`_.

#.  Using the Command Prompt, start the **sample** avatar by navigating to ``C:\ei8\avatars\prod\sample`` and using the command ``docker-compose -f docker-compose.yml up``.
