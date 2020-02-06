# Internal-Rainbow-Six-Cheat
###### Utilizes a kernel driver for hooking steams overlay than manual mapping our dll to the games memory
###### The hook itself is detected - battle eye checks the function (its a pretty commonly hooked place) if you have a brain you can fix that

**THE OFFSETS ARE OUTDATED, YOUR GAME WILL CRASH WHEN INJECTING**
- also the address for steams GameOverlayRenderer64.dll present virtual method table is definitely outdated (the sig might work idk)   
^ you will need this to inject

- The driver itself is mapped via any vuln driver mapper aka kd or drvmap.
     - Once mapped it creates a system thread (really the  only detection vector besides the two hooks)

- **Features** 	
     - nuklear menu
     - ESP 
          - Box and health (health is kind of fucked)
     - Speed
     - Instant reload
     - Fov stuff
     - Aimbot
     - No flash
     - Chams
     - Bullet mulitpler 
     - Spread and no recoil

**Compiling**

1. Right click on "OverflowKernelInjector.sln" in the first folder.
2. Open it in a text editor such as notepad++
3. Go to the 8th or so line where it says "OverflowDLL" with the path to the right. Change the directory path to the correct one on your system
4. Re-open or reload the solution in visual studio.
5. Compile in x64 Debug - make sure you have the windows driver development kit downloaded and configured correctly.

**credits**
- Alxbrn for ez nuklear pasta https://github.com/alxbrn/d3d11-minhook-nuklear
- mactec0 for hook manual map injecting thing idea https://github.com/mactec0/Kernelmode-manual-mapping-through-IAT/tree/swapchain_vmt_example
