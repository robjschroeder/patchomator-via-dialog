<!-- markdownlint-disable-next-line first-line-heading no-inline-html -->
[<img align="left" alt="App Auto Patch" src="Images/AAPLogo.png" width="128" />](https://techitout.xyz/app-auto-patch)

# App Auto-Patch via Dialog

![GitHub release (latest by date)](https://img.shields.io/github/v/release/robjschroeder/App-Auto-Patch?display_name=tag) ![GitHub issues](https://img.shields.io/github/issues-raw/robjschroeder/App-Auto-Patch) ![GitHub closed issues](https://img.shields.io/github/issues-closed-raw/robjschroeder/App-Auto-Patch) ![GitHub pull requests](https://img.shields.io/github/issues-pr-raw/robjschroeder/App-Auto-Patch) ![GitHub closed pull requests](https://img.shields.io/github/issues-pr-closed-raw/robjschroeder/App-Auto-Patch)

## Introduction
App Auto-Patch combines local application discovery, an Installomator integration, and user-friendly swiftDialog prompts to automate application patch management across Mac computers.

[<img alt="App Auto Patch" src="https://github.com/robjschroeder/App-Auto-Patch/blob/6a7ace89d2f4fc6641b1829f04950bbf3401b6f1/Images/AAP-Demo.gif" />](https://techitout.xyz/app-auto-patch)


## Why Build This

App Auto-Patch was developed based on a similar concept as the Patchomator project, with a significant portion of its code borrowed from there. The main requirement for its use was to create a script deployable through Jamf Pro without the need for installing multiple dependencies on end-user computers. Since the original concept, it has since become an independent repository hosted here.

The script simplifies the process of taking an inventory of installed applications and patching them, eliminating the need for creating multiple Smart Groups, Policies, Patch Management Titles, etc., within Jamf Pro. It provides an easy solution for keeping end-users' applications updated with minimal effort.

This project has since been applied to MDMs outside of Jamf Pro, showcasing its versatility and adaptability. 

## Getting Started with 3.0

App Auto-Patch 3.0 automatically installs itself and necessary components anytime it's ran from outside the working folder `/Library/Management/AppAutoPatch/`
For more information on getting started and testing, please visit the [AAP 3.0.0 Wiki Pre-Release]([https://github.com/App-Auto-Patch/AAP3-Wiki/wiki/Getting-Started](https://github.com/App-Auto-Patch/AAP3-Wiki/wiki)) page for more information

- After installed, you can simply run `sudo appautopatch` from terminal with any parameters to configure as you'd like. Examples:

`sudo appautopatch --interactiveMode=2 --workflow-install-now --deadline-count-focus=2 --deadline-count-hard=4 --ignored-labels="microsoft* googlechrome* jamfconnect zoom* 1password* firefox* swiftdialog" --verbose-mode`

Or trigger from the script directly to perform an install with parameters as you'd like. Example:

`./App-Auto-Patch-via-Dialog.zsh --interactiveMode=2 --workflow-install-now --deadline-count-focus=2 --deadline-count-hard=4 --ignored-labels="microsoft* googlechrome* jamfconnect zoom* 1password* firefox* swiftdialog" --verbose-mode`

 - You can find a mapping of 2.x variables to 3.0.0 configuration and command line options from the following TSV file: [Migration Options](https://github.com/App-Auto-Patch/App-Auto-Patch/blob/3.0/Resources/App-Auto-Patch%203.0.0-Migration-Options.tsv)
 - An example configuration profile can be found here: [xyz.techitout.appAutoPatch.plist](https://github.com/App-Auto-Patch/App-Auto-Patch/blob/3.0/App-Auto-Patch-Managed-Config-xyz.techitout.appAutoPatch.plist)

- To reset AAP to defaults:
  `./App-Auto-Patch-via-Dialog.zsh --reset-defaults`

- Clear Ignored, Required, and Optional Labels:
  `./App-Auto-Patch-via-Dialog.zsh --reset-labels`

- Uninstall App Auto Patch:
  `./App-Auto-Patch-via-Dialog.zsh --uninstall`

## Learn More 

A Pre-Release of ther 3.0.0 Wiki can be found here: [App Auto-Patch Wiki](https://github.com/App-Auto-Patch/AAP3-Wiki/wiki)

- [Getting Started](https://github.com/App-Auto-Patch/AAP3-Wiki/wiki/Getting-Started)

- [Deferral Behavior](https://github.com/App-Auto-Patch/AAP3-Wiki/wiki/Deferral-Behavior)

- [Configuration Settings](https://github.com/App-Auto-Patch/AAP3-Wiki/wiki/Configure-Settings)


***

You can also join the conversation at the [Mac Admins Foundation Slack](https://www.macadmins.org) in channel [#app-auto-patch](https://macadmins.slack.com/archives/C05D69E7SBH).

## Thank you
To everyone who has helped contribute to App Auto-Patch, including but not limited to:

- Dan Snelson ([@dan-snelson](https://github.com/dan-snelson))
- Andrew Spokes ([@TechTrekkie](https://github.com/TechTrekkie))
- Andrew Clark ([@drtaru](https://github.com/drtaru))
- Andrew Barnett ([@andrewmbarnett](https://github.com/AndrewMBarnett))
- Trevor Sysock ([@bigmacadmin](https://github.com/bigmacadmin))
- Bart Reardon ([@bartreardon](https://github.com/bartreardon))
- Charles Mangin ([@option8](https://github.com/option8))
- Gil Burns ([@gilburns](https://github.com/gilburns))
### And special thanks to the Installomator Team
- Armin Briegel ([@scriptingosx](https://github.com/scriptingosx))
- Isaac Ordonez ([@issacatmann](https://github.com/issacatmann))
- Søren Theilgaard ([@Theile](https://github.com/Theile))
- Adam Codega ([@acodega](https://github.com/acodega))
