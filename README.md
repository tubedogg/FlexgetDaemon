FlexgetDaemon
=============

Flexget daemon Mac OS X launcher

Download the [zip file](https://github.com/tubedogg/FlexgetDaemon/archive/master.zip). Unzip and move the .app file whereever you would like it. Double-click on it to run. It should flash a small window then disappear. You can confirm the daemon is running from Terminal:
{{{sh
flexget daemon status
}}}
You should see something like this appear:
{{{sh
2014-02-05 02:04 INFO     manager                       Daemon running. (PID: 6452)
}}}

To stop the daemon, run this command in Terminal:
{{{sh
flexget daemon stop
}}}
