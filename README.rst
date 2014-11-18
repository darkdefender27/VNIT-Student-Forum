=================
Student-Forum '15
=================

A **Web Application** intended to aid the freshmen of VNIT, Nagpur.

(Visvesvaraya National Institute of Technology, CSE Dept. Batch of 2015)

Clone
-----

- Make sure your Internet is working.
- Clone this repo by typing ::

    git clone https://github.com/darkdefender27/VNIT-Student-Forum.git


Installation
------------

- Install Virtual Environment using the following command ::

    sudo apt-get install python-virtualenv

- Create a Virtual Environment ::

    virtualenv /path/to/virtualenv

- Activate the virtualenv using the command ::

    source /path/to/virtualenv-name/bin/activate

- Change the directory to the `StudForum/` project using the command ::

    cd /path/to/StudForum

- Install pre-requisites using the command ::

    pip install -r requirement.txt

  or you can also type ::

    easy_install `cat requirement.txt`


Usage
-----

- Using sqlite3 (For development server only). Though, we recommend to use `MySQL` for deployment
  server. See `settings.py` file for usage.

  Open `AakashTechSupport/AakashTechSupport/settings.py` file and do the following changes ::

    DATABASES = {
        'default': {
        'ENGINE': 'django.db.backend.sqlite3',
        'NAME'  : 'studforum.db',
        #No need to mention below fields while using sqlite3
        'USER': '',
        'PASSWORD': '',
        'HOST': '',
        'PORT': '',
        }
    }


- Populate the database using the following command ::

    cd /path/to/StudForum
    python manage.py syncdb

- Run the script populate.py which enters details of remote center into the table Tabletinfo from the details_of_rc.csv file ::

    python populate.py

- Start the server using the command ::

    python manage.py runserver


Contributing
------------

- Never edit the master branch.
- Make a branch specific to the feature you wish to contribute on.
- Send me a pull request.
- Please follow `PEP8 <http://legacy.python.org/dev/peps/pep-0008/>`_
  style guide when coding in Python.

License
-------

GNU GPL Version 2, June 1991.

Please refer this `link <http://www.gnu.org/licenses/gpl-2.0.txt>`_
for detailed description.
