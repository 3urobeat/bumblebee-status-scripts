# bumblebee-status-scripts
My self-made bumblebee-status scripts 
  
These scripts do not follow the [coding guidelines](https://bumblebee-status.readthedocs.io/en/main/development/module.html#coding-guidelines) of bumblebee-status and are quite low-quality in general to just work in my environment.  
Feel free to use them in your setup but you might have to tweak a few things.  
  
## Scripts:
  
### cpu3
Description: Gets the utilization (load), temperature and cpu fan speed from 'mpstat' & 'sensors' to be used as module for bumblebee-status.

Parameters: 
cpu3.format     -> The script will replace the keywords in your format string with the corresponding values. You can also simply leave out keywords to not display them. Keywords: {load}, {temp} & {fan}
cpu3.chip       -> Provide the chip flag with the sensor of your CPU temp as String. Be sure to run 'sudo sensors-detect' in order to find and probe your CPU temp sensor. For me (AMD Ryzen) it is 'k10temp-pci-00c3' or 'thinkpad-isa-0000' on my Thinkpad.
cpu3.tempsensor -> If your PC uses a different sensor for the CPU temperature then you can provide it with this flag. Default is 'temp1_input'
cpu3.fansensor  -> If your PC uses a different sensor for the fan readout then you cna provide it with this flag. Default is 'fan1_input'
  
### gpu
Description: Gets the utilization (load), temperature & vram usage from nvidia-settings to be used as module for bumblebee-status.  
  
Parameter:  
gpu.format -> The script will replace the keywords in your format string with the corresponding values. Keywords: {load}, {temp} & {vram}  
  
### updates
Description: Gets the amount of available package updates (+AUR). Click the module to see which packages can be updated (notification).  
  
Disclaimer: Needs 'checkupdates+aur' package from the AUR to work.  
  
### uptimetext
Description: Very simple uptime script that gets the output from 'uptime -p' for bumblebee-status.  
  