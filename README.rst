################
i3 configuration
################


Installation
------------

Clone to ``~/.i3``

Status bar setup
----------------


Default status bar
##################

Delete the ``bar {{ .. }}`` code in ``config`` and put::

    bar {
        status_command i3status
    }


i3pystatus
##########

Note: this is a tricky installation. See the ``Default Status bar``
section.

Project page: https://github.com/enkore/i3pystatus.git
Pip: ``$ [sudo] pip install i3pystatus``
Requirements: python3.3 + modules + header libs (see below)

Tested on debian jessie:

.. code-block:: bash

    # clone pip
    $ git clone https://github.com/pypa/pip.git

    # Change dir:
    $ cd pip

    # Setup and install to python3 interpreter:
    $ [sudo] python3.3 setup.py install

    # a.) Install i3pystatus (latest):
    $ [sudo] pip3.3 install git+https://github.com/enkore/i3pystatus.git#egg=i3pystatus
    # b.) Install i3pystatus (stable):
    $ [sudo] pip3.3 install i3pystatus

    # install necessary modules for retrieving data:
        
    # basiciw (required for wireless):
    $ [sudo] apt-get install libiw-dev
    $ [sudo] pip3.3 install basiciw

    # netifaces
    $ [sudo] pip3.3 install netifaces-py3

    # alsa
    $ [sudo] apt-get install libasound2-dev
    $ [sudo] pip3.3 install pyalsaaudio

    # pyweather
    $ [sudo] sudo pip3.3 install https://launchpad.net/python-weather-api/trunk/0.3.8/+download/pywapi-0.3.8.tar.gz

Config details
--------------

==============  ==========================================================
Requirements    python3.3
i3 Version      i3 version 4.7.2 (2014-01-23, branch "tags/4.7.2")
Distribution    Debian GNU/Linux testing (jessie)
License         MIT
Author          Tony Narlock < tony at git-pull dot com >
==============  ==========================================================
