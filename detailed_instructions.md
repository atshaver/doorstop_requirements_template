###Getting Doorstop Working

These steps were followed on a Windows 10 PC.
#Commands are bold.
*Download the Oracle VirtualBox application from the microsoft app store. This will act like a computer within your computer so you can run the rest of these steps independently of your windows operating system.
Follow the steps in this tutorial to install Ubuntu on Virtual Box.  https://www.youtube.com/watch?v=QbmRXJJKsvs
 Note: When prompted, set the base memory to about 4096 mb and the disk size(hard drive) to 20.0 GB. Disk space can be changed later but is difficult. Select “minimal” when asked what version of Ubuntu you would like to install.
*Click the lower left corner of Ubuntu screen and search for Terminal application. 
*Open the terminal. Type the following commands one at a time, pressing enter after each, and follow instructions for installing these items.
**sudo apt-get install graphviz**
**sudo apt-get install pandoc**
**pip install graphviz** (typing this command may prompt you to download one more thing, follow those instructions)
**sudo apt-get install libreoffice**
**install texlive-latex-extra**
8Open firefox inside Ubuntu, and search for Anaconda download. Anaconda contains tools that will allow doorstop to function. Download the latest python version in the browser.
8Move back to the terminal. Type:
**sha256sum /path/filename** (don’t worry if this returns file not found or similar)
**Bash ~/Downloads/Anaconda3-2019.10-Linux-x86_64.sh**
*Follow the instructions to get Anaconda installed. Press yes when asked about conda init. Then exit out of the terminal and reopen it.
*Now, if the doorstop repository is shared with you, you must clone the template into the terminal. Head to the Desktop folder (cd Desktop). Type:
**git clone https://github.com/douglase/doorstop**
**git clone git@github.com:douglase/doorstop.git**
*Navigate to the doorstop folder(cd .. press enter then cd doorstop). Type:
**python setup.py develop**
*Then navigate to the doorstop_requirements_template folder in the same way as above. Type:
**./doorstop_sync.sh**

Now the template will be working! If you head to the file explorer, and make a change to a .CSV file, then type the ./doorstop_sync.sh command, changes will be made to your output files, which are also located in the same folder in the file explorer.



