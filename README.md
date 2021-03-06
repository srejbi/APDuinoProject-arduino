APDuinoProject-arduino
======================

Eclipse+AVR plugin based workspace with Arduino_Mega_2560 configuration

This is the official repo for the APDuino Project's Arduino sources.
For more information, visit the APDuino Project at http://apduino.org.

Pre-requisites:
* Arduino IDE 1.0 installed, USB communications to Arduino Mega 2560 established
* Eclipse + AVR plugin installed
* git or Eclipse egit plugin installed

Links:
=====
* http://arduino.cc/en/Main/Software - download Arduino 1.0 (find it under the Previous IDE versions)
* http://www.arduino.cc/playground/code/eclipse
* http://www.baeyens.it/eclipse/	- AVR Plugin by Jantje 
* http://www.baeyens.it/eclipse/Install.html	- Eclipse+AVR plugin install guide by Jantje
* "If you would like to support Jantje; buy Jantje an Arduino.":http://www.baeyens.it/eclipse/donate.html
* http://git-scm.com/
* http://www.eclipse.org/egit/	- EGit plugin
* http://www.vogella.com/articles/EGit/article.html - a nice EGit tutorial

Install from sources
====================

Normally the APDuino Project aims to provide a programming free experience (for ready-to-flash builds visit http://apduino.com/firmwares).
However, if you need to build from sources (eg. trying to use hardware components not supported by the official APDuinOS releases), this repo is for you.
_(And 3 more, pulled in as submodules.)_

There are two main methods to get & build the sources (once pre-requisites met):

# mostly shell-based with git:
<pre>
mkdir ${WORKSPACE_DIR}
cd ${WORKSPACE_DIR}

# symlink or copy Arduino IDE files, choose between the following
ln -s [path to Arduino IDE 1.0] ./arduino	# symlink Arduino IDE 1.0 to ${WORKSPACE_DIR}/arduino
cp -r [path to Arduino IDE 1.0] ./arduino	# copy Arduino IDE 1.0 to ${WORKSPACE_DIR}/arduino

git clone https://github.com/srejbi/APDuinoProject-arduino.git
git submodule init
git submodule update
</pre>

# In Eclipse, using egit
* switch to a new workspace
* import > Git > https://github.com/srejbi/APDuinoProject-arduino.git
* tick submodule import and project creation

> _Additional steps:_
> * _In any case, configure AVR plugin (Preferences/Arduino) after, set the Arduino IDE location to '${WORKSPACE_DIR}/arduino' and Arduino libraries to '${WORKSPACE_DIR}/arduino/libraries'_
> * _Also, select the 'Arduino Mega 2560 or Mega ADK'/'16000000' values on the Arduino project prefs of the 'arduino_headless' project in the workspace._

> _Build should work after._

A more detailed guide can be found here: http://apduino.org/projects/apduinos/wiki/Building_From_Sources
