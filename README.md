# BsxOc1_
A set of PNG files wrapped in Apple .icns file format suitable for using as a theme for OpenCanopy which is part of OpenCore.

<img src="https://github.com/blackosx/BsxOc1_/blob/main/preview.jpg" alt="theme_preview" border="0">

<img src="https://github.com/blackosx/BsxOc1_/blob/main/preview2.jpg" alt="theme_preview" border="0">

**Requirements**<br>
[OpenCore](https://github.com/acidanthera/OpenCorePkg) with OpenCanopy installed and configured.

**Initial Setup of OpenCanopy**<br>
Please refer to [OpenCore beauty treatment](https://dortania.github.io/OpenCore-Post-Install/cosmetic/gui.html#setting-up-opencore-s-gui) at dortania.

**Using this theme**<br>
The Resources directory from this repo contains just the Image dir for the EFI/OC/Resources/Image dir you will have setup for OpenCanopy (if not, see the above setup link.)

Each .icns file here begins with 'BsxOc1_'. The idea here is you can move the contents of this Image directory in to your existing OC/Resources/Image/ directory so these new files sit along side your existing theme files. 

Before you do though, you will want to select your background image from the thirteen different sized files in the /Resources/Image/BsxOc1_Backgrounds directory. Choose the one for your display resolution that OpenCanopy uses and move it in with the other .icns files. You can then remove the BsxOc1_Backgrounds directory as these files will generally be the largest and due to limited space on the EFI System Partition you won't want to store redundant image files.

Once your EFI/OC/Resources/Image dir contains the necessary BsxOc1_ .icns files you can switch the icon set used by OpenCanopy by changing the 'PickerVariant' key in OpenCore's config.plist to match the preceding name of the icon set you want to display. So to instruct OpenCanopy to use this icon set you want to set the PickerVariant key to BsxOc1_

```
                <key>PickerVariant</key>
                <string>BsxOc1_</string>
```

**Recommended Config changes**<br>
For the best experience using this theme you will want the text to display in white. This can be achieved by setting NVRAM->Add->4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14->DefaultBackgroundColor to any colour other than Apple Grey, #BFBFBF or as used on config.plist, v7+/AA==

```
        <key>NVRAM</key>
        <dict>
            <key>Add</key>
            <dict>
                <key>4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14</key>
                <dict>
                    <key>DefaultBackgroundColor</key>
                    <data>AAAAAA==</data>
```