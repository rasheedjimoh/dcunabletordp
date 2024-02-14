# Unable to remote into VM after promotion to Domain Controller

## Error

The logon attempt failed.

![image](https://github.com/rasheedjimoh/dcunabletordp/assets/157264080/cbe8cc51-c892-4a56-a235-60c0d6f87fba)


## Resolution

1. Go to the Azure Portal and navigate to your VM.
2. On the left menu:
Option 1: Type "run" in the search box, press Enter, then click on 'Run Command'.
Option 2: Go to Operations > Run command.
3. Click on 'EnableAdminAccount' and then click 'Run'. Close the window using the X button and wait for the notification indicating the script has finished. If needed, check the progress by selecting 'EnableAdminAccount' again.

![image](https://github.com/rasheedjimoh/dcunabletordp/assets/157264080/00581674-0f84-40df-ba04-0e1d0595b771)
  
4. If step 3 is successful, click on "RunPowerShellScript".
 
![Screenshot 2024-02-14 024719](https://github.com/rasheedjimoh/dcunabletordp/assets/157264080/f36c4e74-77a6-4a63-a861-0583bdd3b857)

5. In line 1, type "net user [Username] [Password]" and then click 'Run'. Replace [Username] with the RDP user you want to use with local owner/admin rights.

You're done! You should now be able to Remote Desktop Connection (RDC) to your server using the local admin [Username] as the login name (e.g., \username).




