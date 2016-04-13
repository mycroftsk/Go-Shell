#GoTo#

Allows PowerShell users to navigate to a specific directory in a quick and easy way using bookmarks.

##Installation##

####Manual Install####

1. Copy `Go.psm1` to your modules folder (e.g. `$Env:PSModulePath\Go\`)
2. Execute `Import-Module goto` (or add this command to your profile)
3. Bookmark away!

####Customization####
Go-Shell stores its data normally in two files located in the `~\AppData\Local\Go\`-folder.

This is changeable by setting this in your profile:

<pre>$Global:GoDataDirectory = "$([Environment]::GetFolderPath('LocalApplicationData'))\GoTo\"
$Global:GoRememberFileName = "goto-remember-last.txt"
$Global:GoBookmarkFileName = "goto.txt"
</pre>

The values above are the defaults.

##How to Use GoTo##

<pre>Usage:
    goto label
    goto label -delete or -d
    goto label -show or -s
    goto label -add or -a
    goto label C:\SomePath -add or -a
    goto -showAll or -sa
    goto -clear or -c
    goto -last or -l

Switches:
    -add or -a             Adds the current directory.
    -delete or -d          Remove the given key from the directory.
    -showAll or -sa        Show all the keys and values in the directory.
    -show or -s            Show the specific key and value.
    -clear or -c           Clears all the keys and values in the directory.
    -last or -l            Goes to the last used go key.
    -help or -h            Displays this screen.

Tips:
    - Pressing the tab button after a few letters will auto fill the rest of the bookmark keyword.</pre>
