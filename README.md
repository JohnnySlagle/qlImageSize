## Announcement 

The origin developer of this app is [@Nyx0uf](https://github.com/Nyx0uf/qlImageSize)

This is a fork of the [origin repo](https://github.com/Nyx0uf/qlImageSize)

# qlImageSize

This is a **QuickLook** plugin for OS X *10.11+* to display the dimensions of an image and its file size in the title bar.

![https://static.whine.fr/images/2014/qlimagesize4.jpg](https://static.whine.fr/images/2014/qlimagesize4.jpg)

This plugin can also preview and generate Finder thumbnails for unsupported images formats like :

- [bpg](http://bellard.org/bpg/ "bpg")
- [WebP](https://developers.google.com/speed/webp/ "WebP")

![https://static.whine.fr/images/2014/qlimagesize3.jpg](https://static.whine.fr/images/2014/qlimagesize3.jpg)

![https://static.whine.fr/images/2014/qlimagesize2.jpg](https://static.whine.fr/images/2014/qlimagesize2.jpg)


# mdImageSize

It's a **Spotlight** plugin to display informations of unsupported images (**WebP**, **bpg**, **Portable Pixmap**) in the Finder's inspector window.

![https://static.whine.fr/images/2014/mdimagesize1.jpg](https://static.whine.fr/images/2014/mdimagesize1.jpg)


# Installation

### -Install via Homebrew

 Launch Terminal.app and run `brew cask install qlimagesize`

### -Manually install 

 1.Download the file from [here](https://github.com/L1cardo/qlImageSize/releases)

 2.Unzip the file you have just downloaded and you will get a file named `qlImageSize.qlgenerator`

 3.Copy the `qlImageSize.qlgenerator` to the `/Users/⁨<your-user-name>⁨/Library/QuickLook⁩/` (You may need a password permission)

 4.Launch Terminal.app and run `qlmanage -r`


# Uninstall

### -Uninstall via Homebrew
 
 Launch Terminal.app and run `brew cask uninstall qlimagesize`
 
### -Manually uninstall

 1.Launch Terminal.app (in `/Applications/Utilities`)
     
 2.Copy and paste the following line into the Terminal :

 `sudo rm -rf "/Library/Application Support/qlimagesize" "/Users/⁨<your-user-name>/⁨Library/QuickLook⁩/qlImageSize.qlgenerator" "~/Library/Spotlight/mdImageSize.mdimporter"`
 
 Press Enter.
 
 Type your password and press Enter.


# Limitations

If you are a **Pixelmator** user, its own QuickLook plugin might get in the way when previewing **WebP** files. To fix this you need to edit the file `/Applications/Pixelmator.app/Contents/Library/QuickLook/PixelmatorLook.qlgenerator/Contents/Info.plist` and remove the dict entry that handles **webp**.

After editing the `Info.plist`, the QuickLook for Pixelmator file format (such as `.pxm`) might not work due to Code Signing, you can unsign the Pixelmator's QuickLook binary using this tool, [unsign](https://github.com/steakknife/unsign). After downloading and `make` the tool, unsign the binary inside `MacOS/` , it will create another binary with the extension `unsigned`, rename the orignal binary for backup then remove the extension for the unsigned binary.

`./unsign /Applications/Pixelmator.app/Contents/Library/QuickLook/PixelmatorLook.qlgenerator/Contents/MacOS/PixelmatorLook`

### License

***qlImageSize*** is released under the *Simplified BSD license*, see **LICENSE**.
