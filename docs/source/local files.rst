Local Files Setup
=================

* Checkout avatar-server-pack repo on GitHub (https://github.com/ei8/avatar-server-pack.git)
* Overwrite existing database files with blank databases

  * Go to ``avatar-server-pack\avatars\prod\blank``
  * Copy all ``.db`` files
  * Paste all to ``avatar-server-pack\avatars\prod\sample``

* Open ``.env`` file
* Change the ``AVATAR_IP`` and ``D23_IP`` to your own local machine's IP Address
* Open ``d23-variables.env``
* Delete ``BASE_PATH`` values (it should show as ``BASE_PATH=``)
* Run Docker Compose

  * ``docker-compose -f docker-compose.yml up``

