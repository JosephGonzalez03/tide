# tide

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

4. Navigate to settings.yaml in $HOME/.config/tide/ and edit proejct.directory to point to your local directory with all of your git repos.
