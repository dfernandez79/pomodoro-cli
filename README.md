# Another Pomodoro Timer shell script

Stop looking for a Pomodoro Timer application, if you have a Unix-like shell you can hack one in one shell line:

```sh
sleep $[60*25]; echo "Pomodoro Finished!"
```

This script is based on that simple idea but adds a few features:
* Logs the pomodoro events to `$HOME/.pomodoro.log` so you can create nice work statistics.
* Uses the OSX notification center to inform about the pomodoro at start, 5 mins before the end, and at the end.
* Catches the Ctrl-C signal to cancel the pomodoro.
* Executes the screen saver for long breaks.

Usage
-----

* Start a pomodoro: `pomodoro "Task name"`
* Do a break: `pomodoro break`
* Do a long break: `pomodoro longbreak`
* You can use the shell to schedule your pomodoros: `pomodoro "Task" && pomodoro break && pomodoro "Task" && pomodoro longbreak`
* Show the entries of your pomodoro log: `pomodoro log`

Hack your own
-------------

The idea of using the shell for a pomodoro timer is not new, and you'll find a few in GitHub.
It's pretty simple to do, but more powerful than most of the Pomodoro Apps out there.

This script only works on OSX, because of the notification center/screen saver calls are made with AppleScript.

