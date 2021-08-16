 **LetsHaveKiddos** | **Installation Guide**
===========================


First time writing this kind of guide I'm gonna make it as simple as possible to limit the amount of questions asked, that said I'm genuinely the worst candidate to explain how anything works. So bare with me.




Things you will need:
===========================

* [Timeshift](https://github.com/teejee2008/timeshift) | Or any tool for making backups I prefer Timeshift. Should be available from your package manager.

* A couple of dependencies.

* A little patience.


Dependencies
===========================

Assuming you know how to use your package manager. apt-get yay pacman etc.

You'll want to download and install these dependencies they're quite popular and very customizable so feel free to give my dots a good edit or two if you'd like but for now




* Kitty

* Dunst

* polybar-git

* BetterDiscord

**(optional)** (only necessary if you want to use the custom css for discord.)

* betterlockscreen

* i3lock-color or i3lock-fancy

* i3-gaps

* xrandr

* feh

**(technically you can use these files, this theme on most desktop environments, window managers you want, but this guide is for my setup specifically)**

* rofi

* picom-ibhagwan-git

* xrandr




Backup
===========================

This part is technically optional, but seriously recommended if youre prone to screwing something up.

I use Timeshift and I think it's safe to say it's highly recommeneded.

It's already in whatever package manager you're using so just sudo apt-get timeshift, or yay timeshift or pacman -S timeshift, or whatever package manager youre using. Just get Timeshift installed.

Here's a guide if you're unsure how to use Timeshift.

https://ostechnix.com/how-to-backup-and-restore-linux-system-with-timeshift/



Drag and drop
===========================

PLEASE PROCEED **ONLY** AFTER MAKING A **BACKUP**.

**Leave out the fonts folder, we will deal with them later.**

**You want to copy the following:**

* .config

* .icons

* .themes

* Pictures

![filescopy](filescopy.png)


Paste into your home folder.

It will overrite some files so when it asks to replace just click "replace all" or "yes to all" or whatever prompt comes your way.

![replaceall](replaceall.png)

Just a reminder your home folder is /home/"your name"/ not just /home/

In my case it is /home/christian/


Installing Fonts
===========================

Now back to the fonts. Back in the zip, copy the fonts folder into .local/share/fonts

![fontsinstall](fontsinstall.png)


After installing copying the "fonts" folder to .local/share/fonts/

Open up yourself a terminal (kitty preferably)

Run this command to rebuild your font cache.

`fc-cache -f -v`

It will look something like this.

![fontrebuildcache](fontrebuildcache.png)


Getting display to work
===========================

My resolution is 1920x1080.

We will need find your resolution and monitor to get correct displays.

First open a terminal and enter xrandr.

![xrandr](xrandr.png)

Once you've determined which monitor is yours copy it somewhere, memorize it, save it.

Next you're gonna want to open up an editor vim, neovim, sublime, geany, vscode doesn't matter.

You're gonna navigate to ~/.config and youre gonna open these files:

* ~/.config/i3/config

        In this file you want to check in keybindings for rofi, xrandr outputs, and where workspaces are kept.  Obviously a findall and replace all function is best here, but if you don't know how I made it pretty easy to find all the locations you should look for. I've made a big commented out **IMPORTANT** text, find that and the "DP-2" you need to replace with your monitor follows.

* ~/.config/polybar/config
    
    
        In this file you want to look for [bar/main] and [bar/sensors]. Swap DP-2 with your monitor.
        

Find in the files where it says **DP-2** and replace with your main monitor.

*And if you have two or more monitors I recommend also replacing HDMI-0 with your second monitor.*

![replacedp2](replacedp2.png)


Reboot **or** logout **and** switch to i3 on your login manager.


Ignore this section for now skip to finished
===========================
**IGNORE THIS SECTION PLEASE**

/boot/grub/themes/default/

open terminal blah blah 

cp dotfiles/boot/ > /boot/grub/themes/default/ 

Applying icons and themes
===========================

I use lxapperance and qt5ct for applying themes. 
You can find them in your package manager.

Here's a screenshot.

![lxappearance qt5ct](lxappearance qt5ct.png)


It's pretty straight forward, you just choose your icons, themes, cursors etc. Hit apply and you're on your way.


Finished
===========================

After that, should be it. Logout log back in (if youre using a login manager) switch to i3 and boom you're set.

If you are curious about shortcuts for my config just open (with any editor of your choosing) ~/.config/i3/config

Some common ones are mod4+Enter to bring up a terminal. Mod4+d to open up the rofi launcher. You'll want to go through that config 100%.

I prettied up my config recently so should be a breeze to go in and out changing whatever you'd like.



