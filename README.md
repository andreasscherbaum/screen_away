screen_away irssi module

written by Andreas 'ads' Scherbaum <ads@ufp.de>

changes:
 07.02.2004 fix error with away mode
            thanks to Michael Schiansky for reporting and fixing this one
 07.08.2004 new function for changing nick on away
 24.08.2004 fixing bug where the away nick was not storedcorrectly
            thanks for Harald Wurpts for help debugging this one
 17.09.2004 rewrote init part to use $ENV{'STY'}
 05.12.2004 add patch for remember away state
            thanks to Jilles Tjoelker <jilles@stack.nl>
            change "chatnet" to "tag"
 18.05.2007 fix '-one' for SILC networks
 2016-05-21: minor cleanups, upload to GitHub


usage:

place this script in your autorun directory and/or load it with
 /SCRIPT LOAD <name>

there are 5 settings available:

/set screen_away_active ON/OFF/TOGGLE
/set screen_away_repeat <integer>
/set screen_away_message <string>
/set screen_away_window <string>
/set screen_away_nick <string>

active means, that you will be only set away/unaway, if this
  flag is set, default is ON
repeat is the number of seconds, after the script will check the
  screen status again, default is 5 seconds
message is the away message sent to the server, default: not here ...
window is a window number or name, if set, the script will switch
  to this window, if it sets you away, default is '1'
nick is the new nick, if the script goes away
  will only be used if set

normally you should be able to rename the script to something other
than 'screen_away' (as example, if you dont like the name) by simple
changing the 'name' parameter in the %IRSSI hash at the top of this script
