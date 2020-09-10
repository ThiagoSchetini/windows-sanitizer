# Windows Sanitizer

This mod is made on the original ameliorated.info great code and we perceive their efforts to remove all windows backdoors. Visit them and try their ready mod Windows and skip all this steps.

*All credits for them:* https://ameliorated.info

### Important notes before using it:

Install a new and fresh windows with a original key and them made this changes.

We preserve original features like the new "Windows Explore" and the new "Menu".
	
We do not try to delete all backdoors because windows is the backdoor.

Windows updates as you know will be completely destroyed, **forever**!

There is no guarantee, we are alone, we are one!

Everything is a backdoor, starting with your Alexa toys and your smartphone =(

Nevermind...

### Let's sanitize the monster!
	
After and only after a new and fresh Windows install, run as admin and wait it to finish:

	sanitizer.bat
	choose >>> 1. Execute Sanitizer

Wait it to finish. Maybe you are gonna see some errors, maybe it appears to be stucked, but wait, that's normal, remember ... nevermind.

After finish, don't do anything, just do the next steps using a trick.

### Time for Windows TRICK! (read and use on the next step to remove windows junk)

Assume the control of **ANY WINDOWS DIRECTORY** to do some activities and them restore it with some **SAFE** steps.

Let's start on.... C:/Windows:

	01 go to C:/Windows
	02 right click on "Windows" folder properties
	03 select "Security" tab
	04 click on "Advanced"
	05 the trick start now: click "change" (owner)
	06 wait a weird box display
	07 look for the "Enter the object name to select" blank box 
	08 type there "Administrators"
	09 click on the right button "Check Names" 
	10 it will appear a name like "MY-MACHINE\Administrators"
	11 click "OK"
	12 now look for a checkbox "Replace owner on subcontainers and objects" and check it!
	13 click "Apply"
	14 wait for a successfull message (maybe appears some warning, click OK, nevermind...)
	15 click "OK" on the entire box
	16 click "Advanced" again
	17 search for the "Administrators(YOUR-MACHINE-NAME)"
	18 is the Access "Full Control" or only "Ready & execute"?
	19 if not Full Control, click on "Change permissions"
	20 double click on yours "Administrators(YOUR-MACHINE-NAME)" line
	21 click on "Full control" checkbox
	22 finish, click "OK"

How to restore the original permissions and owners:

	repeat steps 01 to 04 
	jump and execute steps 19 and 20
	remove "Full control" checkbox, then check others checkbox like this beautiful "table" below:
	__________________________________________________________________________________________________________________________
	|folder |owner |administrators permissions
	|"Windows" |"NT Service\TrustedInstaller" |"Read & execute", "List folder contents", "Read"
	__________________________________________________________________________________________________________________________
	|folder |owner |administrators Permissions
	|"Program Files" |"NT Service\TrustedInstaller" |"Read & execute", "List folder contents", "Read", "Modify", "Write"
	__________________________________________________________________________________________________________________________
	|folder |owner |administrators permissions
	|"Program Files (x86)" |"NT Service\TrustedInstaller" |"Read & execute", "List folder contents", "Read", "Modify", "Write"
	__________________________________________________________________________________________________________________________
	|folder |owner |administrators permissions
	|"Program Data" |"SYSTEM" |"Read & execute", "List folder contents", "Read", "Modify", "Write"
	__________________________________________________________________________________________________________________________

	then "Apply"
	click "OK"

	repeat again steps 01 to 07
	on step 08 type the original owner "NT Service\TrustedInstaller" or "SYSTEM" (for "Program Data)
	go ahead with steps 09 to 15

### Deleting junk using the TRICK
	
Using our *TRICK* on "Windows", "Program Files", "Program Files (x86)" and "Program Data" search and remove:

	"Program Files/Internet Explorer"
	"Program Files/ModifiableWindowsApps"
	"Program Files/UNP"
	"Program Files/WindowsApps"
	"Program Files/Windows Defender"
	"Program Files/Windows Defender Advanced Threat Protection"
	"Program Files/Windows Photo Viewer"
	"Program Files/Windows Mail"
	"Program Files/Windows Media Player"

	"Program Files (x86)/Internet Explorer"
	"Program Files (x86)/Windows Photo Viewer"
	"Program Files (x86)/Windows Defender"
	"Program Files (x86)/Windows Mail"
	"Program Files (x86)/Windows Media Player"

	Windows/System32/wua*
	Windows/System32/wups*
	"Windows/System32/SecurityHealthAgent.dll"
	"Windows/System32/SecurityHealthService.exe"
	"Windows/System32/SecurityHealthSystray.exe"
	Windows/SystemApps/*CloudExperienceHost*
	Windows/SystemApps/*ContentDeliveryManager*
	Windows/SystemApps/Microsoft.MicrosoftEdge*
	Windows/SystemApps/Microsoft.Windows.Cortana*
	Windows/SystemApps/Microsoft.XboxGameCallableUI*
	Windows/SystemApps/Microsoft.XboxIdentityProvider*
	Windows/diagnostics/system/Apps
	Windows/diagnostics/system/WindowsUpdate

	"Program Data/Packages"
	"Program Data/PackageCache"

Restore the original permissions and owners.

Reboot your windows.

### Time to a security step

Run as admin again:

	sanitizer.bat
	choose >>> 2. User Permissions
	put a password on Administrator account!
	done!

### Time to learn and use Chocolatey package manager

Chocolatey: https://chocolatey.org

To install, run as admin again:

	sanitizer.bat
	choose >>> 3. Install Chocolatey
	wait it to finish, reload your terminal and them check it with the command
	choco --help

Install basic packages (always open terminal as admin):

	freoffice (manual download at https://softmaker-freeoffice.en.softonic.com/)
	choco install vcredist-all (Microsoft Visual C++ Runtime - all versions)
	choco install 7zip
	choco install autohotkey (to use natural scroll on mouse)
	choco install ccleaner
	choco install firefox
	choco install winamp
	choco install spotify
	choco install jpegview (to see all image formats)
	choco install vlc (video player)
	choco install qalculate

#### Internet & Comunication

	choco install discord.install
	choco install microsoft-teams
	choco install teamviewer9
	choco install slack
	choco install zoom

#### NVIDIA driver (if you have a card/chip)

	choco install nvidia-display-driver

#### Gamers & Hardware Enthusiasts
	
	choco install performancetest (the passmark test)
	choco install superposition-benchmark (Unreal engine test and benchmark for GPU's/Games)
	choco install nvidia-geforce-now (streamers)
	choco install hwmonitor (monitor temps of our hardware)
	choco install rufus
	choco install cpu-z
	choco install gpu-z
	choco install partitionmasterfree (if you have/buy a license is better)

#### Developers

	choco install git (use the Git Bash as your terminal after this install!)
	choco install vim					
	choco install wget
	choco install sublimetext3
	choco install docker-desktop
	choco install openjdk11
	choco install maven
	scala (manual download at https://www.scala-lang.org/download/)
	sbt (manual download at https://www.scala-sbt.org/download.html)									
	choco install python
	choco install pypy3

Pycharm for python development:

	choco install pycharm-community

Create python3 and pypy3 virtual environments and add them to Pycharm: 

	mkdir ".venv" on your home directory

	Pycharm: Configure/Settings/Python Interpreter/+(Add)/Virtualenv Environment/New Environment
	check the checkbox "Make available to all projects"
	Location=C:\Users\YOURUSER\.venv\python3, base interpreter = C:\Python38\python.exe

	open terminal and: pypy3 -m venv ~/.venv/pypy3
	Pycharm: Configure/Settings/Python Interpreter/+(Add)/Virtualenv Environment/Existing Environment 
	check the checkbox "Make available to all projects"
	Interpreter=C:\Users\Xeon GTX Workstation\.venv\pypy3\Scripts\pypy3.exe

InteliJ for java/scala/JVM development:

	choco install intellijidea-community

#### More Chocolatey packages

Chocolatey is very complete, see some examples:

	choco install samsung-magician (Samsung ssd/Nvme)
	choco install logitechgaming (Logitech mouse or keyboard)
	choco install logitech-webcam-software (Logitech webcam)

### .NET basic framework

Download and run the last installer, if your windows has it updated the installer will stop:

	https://dotnet.microsoft.com/download/dotnet-framework

### DirectX

Check it, probably your Windows 10 has the latest version, maybe 12, on your terminal do:

	dxdiag.exe

### Power plans

Optimize performance/battery and options for the plan(s) that you need. On terminal open:

	powercfg.cpl
	select and adjust the options to the plan(s) that you are gonna use
	hint: explore all options!
	hint: on "Processor power management" put minimum to 5% and maximum to 100% to get CPU steps

Remove unused power plans:

	powercfg.exe /L
	get the "GUID"
	powercfg -delete "GUID"

### Dark mode and customization

Everything has DARK appearance, even Windows Explorer. It's time to darkenize: 

	go to Settings and explore the native dark features of windows 
	use dark theme on Firefox too
	some apps have dark mode like winamp, teams, office and more!
	add nightime (confortable screen at night) on settings
	config HW monitor to show some temps on your taskbar
	remember to always use the Git Bash as your terminal!

### Open SSH Server (optional for developers)

Use the Git Bash as your terminal and follow this tutorial:

	https://ameliorated.info/documentation.html#openssh

### Git & SSH keys (optional for developers)

Open git bash and config your git:

	 git config --global user.email "yourname@gmail.com"
	 git config --global user.name "Name LastName"

Generate the keys (public and private) to use on your github/bitbucket or another git:

	 ssh-keygen -o -a 300 -t ed25519 -f ~/.ssh/id_ed25519 -C "YOUR-MACHINE-NAME"

start the ssh agent on background (on windows it closes after session) and add the *private key* to it:

	 eval "$(ssh-agent -s)"
	 ssh-add ~/.ssh/id_ed25519

Copy the *public key value* and add it on your github/gitbucket or another git:
	
	cat ~/.ssh/id_ed25519.pub

Create a Repository home and clone something to test it:

	mkdir ~/Repositories/github

### FINAL CLEAN

Run the software CCleaner and explore it, remove startup apps (discord, teams and spotify).

Clean the cache of chocolatey:

	C:\Users\YOURUSER\AppData\Local\Temp\chocolatey

Finally run a trim on your SSD (complete with zeros not used part):
	
	Windows Explorer, right click on "C:(Windows)", then: Properties/Tools/Optimize/Optimize

### TODO Windows Updates

Identify the required KB number updates in the Windows 10 Update History https://support.microsoft.com/en-us/help/4099479

Search and Find the Updates Files like "KB4574727" http://www.catalog.update.microsoft.com/Home.aspx

Open downloaded .msu file, double click and install.

Is there any utility from chocolatey? https://chocolatey.org/packages/chocolatey-windowsupdate.extension

### CREDITS

credits from original source: https://ameliorated.info



**That's all Folks!**