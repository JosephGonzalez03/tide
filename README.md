# Tide

## Introduction
Tide is a terminal menu app that wraps around your tmux installation. It allows you to create tmux sessions from 
projects in a local directory and manage those sessions from within the app. In additon, sessions can be lauched
with user-created configuraiton scripts to start tmux sessions with environments just how you like them.

## Demo
![Tide Demo](demo/tide_demo.gif)

## Installation
1. Create tide/ in $HOME/.config/ and run the following command from this cloned repo. It will copy the required
scripts in scripts/, example config scripts in configs/, and settings.yaml into $HOME/.config/tide/.
```
cp -r -t $HOME/.config/tide scripts configs settings
```

2. Ensure the tide script is executable by running the following command on it:
```
chmod +x tide
```

3. Run the following command from this repo to copy the tide script to your local bin where it will be discoverabl
by your system:
```
cp -t $HOME/../../usr/local/bin
```

4. Navigate to settings.yaml in $HOME/.config/tide/ and edit proejct.directory to point to your local directory
with all of your git repos.

## Creating Config Scripts
Config scripts are just executable shell scripts which run tmux commands. They're really nifty for starting up a
tmux session with the windows and panes already set up for how you like to work. Refer to the tmux man page to
learn how to work with tmux windows and panes from the command line.

For making your own config scripts, know that tide creates the named session for you. This means you will have 1
window in the session to start with. Also, tide always passes 2 arguments to the script. $1 is the project
directory path from settings.yaml. $2 is the project name which is used for the session's name. So, you'll need
to use the second argument for referencing the tmux session. Once done writing the script, make it executable with
the chmod command and move it to $HOME/.config/tide/configs/.
