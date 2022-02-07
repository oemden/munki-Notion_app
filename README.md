# Installing Motion.app in User's Applications folder via munki

Motion.app does not work if it's installed in /Applications folder on a computer with multiple accounts.

### 3 scripts :

### Notion_install_preinstallCheck.sh

The script will check if any Motion.app is installed in the User's Applications folder and compare the `CFBundleVersion` to determine if munki hgas to install the app or not.
 
> NOTE: you HAVE to edit this script with the correct version of the App.
>
> At the time of writing:
> 
> version `2.0.19` for  `x86_64` and version `20.0.18` for `arm64`


### Notion_preinstall-script.sh

Will simply remove the old app - if precheck script above munki has determined the App to be installed.
### Notion_postinstall-script.shWill simply install the app - if precheck script above munki has determined the App to be installed.

> Note: [This script can finally be used for Any app needed to be installed via munki but in user's own Application directory.](https://github.com/oemden/munki-installSomeAppInUserApplicationsFolder)

