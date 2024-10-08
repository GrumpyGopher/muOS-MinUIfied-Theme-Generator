# MinUIfied Theme Generator for muOS Systems
This script helps you create and customize themes for your muOS system, creating a consistent look and feel across your system. This tool should work on Windows, MacOS and Linux.

![Themes Example Image](https://github.com/user-attachments/assets/68cfb45d-b260-4fa0-bab1-b13a6d7d282a)

![Program Example Image](https://github.com/user-attachments/assets/e3c42ffc-cba3-4898-bc8e-86fe90e24204)

## Prerequisites for running from Downloaded Binary [Windows]:
 - None

## Prerequisites for running the script from source
Before running this script, ensure you have the following installed:
 - Python (Tested with version 3.12)
 - All Required Required Python Libraries
 
       python3 -m pip install -r requirements.txt 

Individual Libraries:
 - Pillow library
   
       pip install pillow
 - Tkinter library
   
       pip install tk

 - python-bidi library
   
       pip install python-bidi

 - numpy library
   
       pip install numpy
   
 ### For Debian Linux:
```
apt install python3-pil.imagetk python3-pil python3-bidi python3-tk python3-numpy
```


## Getting Started
 - Insert your SD card into your computer.
 - If you want to keep the **box art**, copy the **MUOS/info/catalogue** folder from the SD card to your computers local storage
 - To use the tool without the SD card, copy your **ROMS** folder from the card to your computers local storage for future use.
 - **Make sure** your box art on your device is set to **fullscreen+front**, otherwise the content explorer UI can behave strangely
 - To run the program from the prebuilt binaries, go to the latest release and download the program from the assets. [Windows Only]
 - To run the program from source you must download this repo as a zip, unzip it, and then run the .py file with python

# Configuration

## Global Configurations
Customize the overall look and feel of the theme. A visual preview will be available to help you see the changes in real-time.

## Theme Specific Configurations
Adjust settings that only affect the theme (excluding the content explorer).

## Box Art Specific Configurations
Specify the box art folder copied from your card.

Adjust text placement to prevent it from overlapping with the box art.

Set the muOS console name to see the box art in the preview.

## Content Explorer Specific Configurations
Modify settings specific to the content explorer menus (e.g., removing brackets from game names, generating themes for games and folders).

# Generation
After configuring your settings, you can generate the theme. There are three methods to do this:

## Archive Manager [Recommended for refried beans or later]
 1. Set the output directory for the Archive Manager (leave blank to generate files in the script's directory).
 2. Optionally, choose to generate only the theme or content explorer files.

## Theme Only
Specify the theme output directory (can be on the SD card, your computer, or **leave blank to generate in the script's directory**).

## Content Explorer Only
Select the catalogue folder where the image files will be generated (recommended to back up the folder before this step).

**For all methods, click "Generate" and the program will handle the rest.**

## Removing MinUI Theming
To remove all MinUI theming from your system:

Choose a different theme in muOS.

**Then either [Recommended]:**

 - Using this tool
 - [Optionally] select your backed up box art directory (As you would for merging)
 - Select your Archive Manager Output Directory
 - Press 'Backup Box Art into Archive Manager File'
 - This will create a file called 'Restore Backed Up Artwork' in your Archive Manager
 - You can use this as an archive restore your content explorer to the state it was before theming

**Or:**

 - Disable Box art in your muOS devices settings to remove all content explorer themeing

## Build instructions

 - Install pyinstaller


       pip install pyinstaller
 - To build, run*:


       pyinstaller ".\Custom MinUI Theme Generator for muOS.spec"
*where the .spec file is the one in the github page, modify the .spec file to work on macOS and Linux if you are able to/want to, and put it on a PR.
  

## Experimental Settings
 - Show hidden files is experimental as I'm not sure how it should work if you don't select to generate game list as well
 - Also Generate Images for Game List is experimental as it will mess up your favourites and history menus

## Credits and thanks
 - Thanks to [@JCR64](https://github.com/JCR64) for the inspiration for the theme and horizontal logo
 - Credits and thanks to [@GrumpyGopher](https://github.com/GrumpyGopher) for the work he's been putting into making the project better
 - Thanks to [@damagedspline](https://github.com/damagedspline) for the Hebrew translation file

**muOS Discord Server:** https://discord.gg/USS5ybVtDz

**Where to talk about this project:** https://discord.com/channels/1152022492001603615/1253933788078014586
