FlexgetDaemon.app
=============

Launches [Flexget](http://flexget.com) in daemon mode in the background.

#### Erroneus console traceback errors ####
**Please note** due to an apparent bug in the Flexget daemon implementation, this method employs something of a workaround to launch. If you run ```flexget execute``` commands from Terminal while the daemon is running, you may see lines like this: ```Traceback (most recent call last):``` They are safe to ignore.

#### Install ####

Download the [zip file](https://github.com/tubedogg/FlexgetDaemon/archive/master.zip). Unzip and move the .app file whereever you would like it.

#### Usage ####
Double-click on it to run. It should flash a small window then disappear. You can confirm the daemon is running from Terminal:
```flexget daemon status```

You should see something like this appear:
```
2014-02-05 02:04 INFO     manager                       Daemon running. (PID: 6452)
```

To stop the daemon, run this command in Terminal:
```flexget daemon stop```

#### Technical notes ####

If you have a ```.bash_profile``` file in your home directory, this app will source it when running. This is to allow certain environment variables to be set correctly (most notably ```PYTHONPATH``` for those running Deluge in a different ```site-packages``` directory than where Flexget is installed). If you don't want this to occur:

1. Right-click on the app file and choose Show Package Contents.
2. Click (or double-click) to open the Contents folder, then Resources.
3. Use your favorite text editor to open the ```script``` file.
4. Remove the line ```. ~/.bash_profile``` or edit it to suit your needs. You can also adjust the path to Python.

To set ```PYTHONPATH``` directly, add this line *before* the line that starts with ```/usr```:
```
export PYTHONPATH=/your/path/to/site-packages
```

#### Copyright ####

I am putting this into the public domain and to the fullest extent possible am relinquishing any copyright interest in the files in this repository.

This bundle contains a simple script that launches Flexget and **does not** contain any Flexget code or resources.
