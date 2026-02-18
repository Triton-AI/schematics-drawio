# LTspice Instructions

>This folder contains the LTspice schematic and its components, and instructions needed to properly change and update the schematic.

## Folder Contents

>In the folder, there are individual component files, which are then utilized by the actual schematic file called `Wiring_Chart.asc`. Each individual component used by the schematic must be its own `.asy` file to be shown in the schematic.

## Downloading LTspice

>To download LTspice, go to the official download page at `https://www.analog.com/en/resources/design-tools-and-calculators/ltspice-simulator.html` and select the correct download file for your computer's operating system. 
The download is free and does not require extra packages.

## Opening the Schematic

>To open the schematic, go to LTspice, and select `File` > `Open...` and navigate to the folder where you have the wiring chart `.asc` file.

## Creating New Components

>To create new components, open LTspice, and select `File` > `New Symbol` and an empty workspace should open up. 
>To create the symbol, in the tool bar you should select `Draw` and select the shape you would like to draw and place in the empty workspace. 
>To add the actual pins, right-click on your component as select `Add Pin` and then give the pin a label and select where in relation to the pin you would like the label visible. Then select `OK` and move the pin where you would like it to be placed. 
>To add text, in the toolbar, there is a blue lowercase `t` called the `Place Comment Text (T)`. Once you click it, a dialogue box will open up, select the appropriate justification (point positioning in relation to the text) and size, as well as type what text you wish to add to the component. 
>When done, save the component to the same folder that the wiring schematic is located so that it can access the component. Save by selecting `File` > `Save As...` and navigate to the folder where you have the wiring chart `.asc` file.

## Adding New Components

>To add new components to the actual schematic, open your schematic and then select the symbol in the toolbar that looks like a circuit chip with a play button on it, labeled `Component (P)` or just press `P`. This will open a dialogue box with components. In the menu, it may show general circuit components, however, we want the custom components we created so under `Show:` instead of `All`, select the `Schematic Directory` which will show the custom part `.asy` files that are in the folder with the schematic. Click on the one you would like to add and hit `Place`. Then place in the schematic where you would like and when done placing, press the `esc` button. 
>To place wires to and from the component pins, click the pins, click where you would like the wires to be routed and then click the next pin you would like to connect to. 
>To save the changes, go to `File` > `Save` or simply press `Ctrl + s`.

## Updating Existing Components

>Once you have edited an existing component file `.asy`, save it and go to the schematic file `.asc` and the components already placed will already change to the new version of the component. 
>However, new pins added will not be connected to any wires and moved or deleted pins will not have any connections either, but the wires that used to connect them will still be in the same placement as before but not connected to anything. Make sure to delete these hanging wires or reconnect them.

## Uploading Changes to GitHub

>There are two main ways to upload the changes you have made to the GitHub. One way, easier for beginners, is GitHub Desktop, or if you do not want to download GitHub Desktop, you can use git via the command line.

#### GitHub Desktop

>If you have GitHub Desktop downloaded, under `Current repository`, make sure it says `schematics-drawio` and that under `Current branch` it is the correct branch you would like to upload to. Then, in `Changes` select the changes you would like to upload and add a title and an optional description to your commit, and then commit the change to the branch, and do not forget to push to the repository.

#### Command Line

If you use command line, go to the folder where the repository is located in command line and check status:
```bash
git status
```

Stage the Changes:

```bash
git add .
```

Commit Changes:

```bash
git commit -m "Describe your changes here"
```

Push to GitHub:

```bash
git push
```

### Clone this repository
Use the SSH clone (recommended if you have SSH keys configured):

```bash
git clone git@github.com:Triton-AI/schematics-drawio.git
```

Then open the repository in VS Code:

```bash
code .
```

>If you have GitHub Desktop, instead copy the GitHub url `https://github.com/Triton-AI/schematics-drawio.git` and in the desktop app, go to `File` > `Clone Repository` and go to the `URL` tab, and paste the url and choose a local folder to hold the repository and then click clone.

### Reminder

>Other people will be using these schematics and may edit at the same time as you. Remember to pull from the repository often to make sure your repository is up to date with the most recent changes.

To do this in command line, simply type in the command line in that repository directory...

```bash
git pull
```

In GitHub Desktop in the tool bar, press `Fetch Origin`, which will make sure you are up to date with the repository.


