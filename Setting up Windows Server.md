#ICT40120 #ICTNWK420 #VirtualMachine #Networking #Scott #Paul #info #vmware

---

### Setting up the Virtual Machine

The virtual machines we will set up are [Type 1 virtual machines](Type%201%20virtual%20machines.md). They will be running inside of VMware Workstation Professional, as it has a super user friendly UI, that is easy to navigate while still hosting many amazing features. 

To begin setting up a Windows Server 2022 / 2019 instance, you have to create a new [virtual machine](Virtual%20Machines.md). To create a new virtual machine, press the button with the plus icon, or, right click the left side panel and select `New virtual machine...`. 

1. In the new dialog window that opens, create a "Typical" machine. 
2. When asked to provide an installer disc or image, select `I will install the operating system later`. See [[#Footnotes#1]] for why.
3. The guest operating system is Microsoft Windows, and in the dropdown, select either Windows Server 2022, or 2019, dependent on your ISO. 
4. Set a virtual machine name that is easy to remember, and make sure its distinguishable from other virtual machines that may have been used for other tasks. Also choose a location off of the C:/ drive, to avoid filling your main SSD. 
5. Set a maximum disk size. I suggest making your disk size 60GB for the main drive. Select `Split virtual disk into multiple files`
6. Select `Customize Hardware`. This is where we can add more disks, ram, or other resources.
7. Under `memory`, you'll want to set the memory to at least 3GB (3072 MB) for a Windows machine. I recommend setting it to 4GB (4096 MB)
8. Under `Network Adapter`, make sure to set the network to `Host-Only`.
9. Under `New CD/DVD (SATA)`, set the connection to `Use ISO image file`, then select the `Browse` button to select your Windows Server ISO
10. Select the `Close` button
11. penis

### Powering on and Setting up

To power on the virtual machine, select it in the left side panel, then select `Power on this virtual machine` , or right click the machine in the left side panel, then `Power > Start up guest`. The machine will then boot. As soon as you power on the machine, click the center of the black screen and hit any key on your keyboard.

#### Installing windows server:
1. Hit `Next`, then `Install now`
2. When asked to select an operating system, click **Windows Server 2022 (Desktop Evaluation)**. 
3. Tick the `Accept` checkbox, then `Next`
4. When asked which type of installation you want, select `Custom`
5. Select your main drive. At this stage, there should only be one. Then, hit `Next`
6. If prompted, hit `Restart Now`

Make sure to create a snapshot! 

### Footnotes
##### 1: When asked to provide a installer disc, why select "do it later"?
The reason we select do it later is very simple. If you were to provide the ISO on that menu, VMware detects that we are trying to install windows server, and askes for the product key immediately. As we don't have one, we wouldn't be able to progress through this menu. 

