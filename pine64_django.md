Following setup 24 from pine64_setup.md:

1. Go to https://docs.djangoproject.com/en/1.10/intro/contributing/ enter the following commands:

  ```
  $ sudo apt-get install python3-pip
  $ # Prefix the next command with sudo if it gives a permission denied error
  $ pip3 install virtualenv
  $ virtualenv --python=`which python3` ~/.virtualenvs/djangodev
  ```
  
2. Activate it:

  ```
  $ source ~/.virtualenvs/djangodev/bin/activate
  ```

3. Install virutalenvwrapper:

  ```
  $ export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3.5
  ```
