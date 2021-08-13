 **LetsHaveKiddos** | **Installation Guide**
===========================


First time writing this kind of guide I'm gonna make it as simple as possible to limit the amount of questions asked, that said I'm genuinely the worst candidate to explain how anything works. So bare with me.




Things you will need:
===========================

* [Timeshift](https://github.com/teejee2008/timeshift) | Or any tool for making backups I prefer Timeshift.

Should be available from your package manager.

* A couple of dependencies.

* A little patience.


Dependencies
===========================

Assuming you know how to use your package manager. apt-get yay pacman etc.   
  
You'll want to download and install these dependencies they're quite popular and very customizable so feel free to give my dots a good editor or two if you'd like but for now 




* Kitty (I can provide color confs for your any terminal if requested)

Kitty is my prefered terminal. (terminal emulator technically.) 

* Dunst

Solid notification daemon, highly customizable.

* polybar-git

Git version of polybar.

* BetterDiscord 

**(optional)** I use this in order to get the fancy shmancy css to work on discord.

* betterlockscreen

Lock script depends on this.

* i3lock-color

Lock script depends on this.

* i3-gaps
* 
**(optional)** If you want my desktop for desktop setup you will need i3-gaps.

* rofi

Used for various menus primarily powermenu and the launcher.

* picom-ibhagwan-git

Super dope fork of picom, used for shadows and other eye candies. 

* 



Backup
===========================

This part is technically optional, but seriously recommended if youre prone to screwing something up. 

For starters I always recommend making backups first just because I myself have a tendency of screwing things up. 

I use Timeshift and I think it's safe to say it's highly recommeneded. 

It's already in whatever package manager you're using so just sudo apt-get timeshift, or yay timeshift or pacman -S timeshift, or whatever package manager youre using. Just get Timeshift installed. 

Once 


Drag and drop
===========================

PLEASE PROCEED **ONLY** AFTER MAKING A **BACKUP**.

**Leave out the fonts folder, we will deal with them later.** 

**You want to copy the following:**

* .config

* .icons

* .themes

* Pictures

![filescopy](media/filescopy.png)


Paste into your home folder.

It will overrite some files so when it asks to replace just click "replace all" or "yes to all" or whatever prompt comes your way.

![replaceall](media/replaceall.png)

Just a reminder your home folder /home/"your name"/ not just /home/. 

In my case it is /home/christian/.


**Installing Fonts**
===========================
After installing copying the "fonts" folder to .local/share/fonts/

Run this command to rebuild your font cache.

`fc-cache -f -v`


