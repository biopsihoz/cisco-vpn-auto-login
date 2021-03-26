# cisco-vpn-auto-login
Apple Script to auto-login to your Cisco AnyConnect VPN Client.
Works only on macOS

1. Clone the repository and open the script `cisco-vpn-auto-login.scpt` with AppleScript Editor. 
2. Open cisco-vpn-auto-login.scpt with AppleScript Editor.
3. Search for `YOUR_PASSWORD_HERE` and replace it with your password. 
4. Search for `DUO_2ND_PASSWORD_HERE` and replace it with your 2nd password. Or you can use the word "push" for some applications for a one-tap approve connection from your phone.
5. Go to file and export it as an application marking it "Run Only".
6. [OPTIONAL] Right-click on the application > Show Package Contents > Contents > Resources. Replace `applet.icns` with your own icon file. Cisco's icon file is provided.
7. Give Accessibility permissions to this app from System Preferences > Security > Privacy > Accessibility. Click on add, browse for application and select it.
8. Run the application to automatically login to your VPN.
9. Since most companies have MFA, the application pauses for the user to press on YubiKey (or likewise).
10. The press on the Yubikey should connect the user to VPN and hide the VPN window. 

**PS:** Do a manual login for the first time after installing the application to set the defaults.   

**Note:** 
* Your password is safe with the application and is not exposed. But in the script, you will have to explicitly remove the password. The script is anyways not needed after the export unless you want to update the password later. 
* Make sure you make a successful login through the Cisco AnyConnect manually before using automated script so that the username is set and you know everything needed is working fine.  

**ToDo:**
* Failure handling - to close while loops after certain tries to avoid memory clogging or have a timeout. 
* Handling cases when AnyConnect is not installed or is already logged in. 
