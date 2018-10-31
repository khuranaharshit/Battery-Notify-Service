
#!/README

* HARSHIT KHURANA
* 20.07.18

* Battery-Notify : Shell script to get the current battery status , compare with the upper/lower bounds and execute certain instruction depending on the condition.

		-> Whatever instruction you want to execute you can add/modify here.
		-> Lower bounds and upper bounds can be changed here. ( Visible in the script)

* BatteryNotify.service : A linux service created for notifying users when their battery level hits either the lower bound or the upper bound of the threshold value. 

		-> It further execute the "Battery-Notify" shell script.
	-> The Parameters are self-explanatory.
	-> One can always the some parameters of the scripts depending on their needs.
	

* DEPENDENCIES 
	
	* Depends on packages :

				1. espeak 

				2. notify-osd

				3. acpi

	* Based on your Linux distro these dependencies might be present or might needed to be explicitly installed.
	* Its always better to take the easy way out and explicitly install these , your smart package manager will figure out whether or not these are present or not.
	* Require systemd on your linux machine.

* Currently tested on Rpi/Ubuntu/Debian/RHEL.
* Keep 'BatteryNotify.service' in '/etc/systemd/system/' directory and once done reload the systemd via
		
		-> sudo systemctl daemon-reload
		-> sudo systemctl status BatteryNotify.service 
		-> sudo systemctl enable BatteryNotify.service 
