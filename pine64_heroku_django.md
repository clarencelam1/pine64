Following setup 24 from pine64_setup.md:

1. Install pip3 and install virtualenv:

  ```
  $ sudo apt-get install python3-pip
  $ # Prefix the next command with sudo if it gives a permission denied error
  $ pip3 install virtualenv
  ```
  
2. Install postgresql:

  ```
  $ sudo apt-get install postgresql
  ```

3. Install Heroku CLI:

  ```
  # Run this from your terminal.
  # The following will add our apt repository and install the CLI:
  $ sudo add-apt-repository "deb https://cli-assets.heroku.com/branches/stable/apt ./"
  $ curl -L https://cli-assets.heroku.com/apt/release.key | sudo apt-key add -
  $ sudo apt-get update
  ```
4. Download file from https://toolbelt.heroku.com/install-ubuntu.sh, save it as install-ubuntu.sh in the current directory, then run

  ```
  $ ./install-ubuntu.sh
  ```
  
5. 
