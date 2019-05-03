Client security And Recommendation
======================

Running Big Screen in a public space is sometimes necessary. It can bring a lot of benifits, but there a few things to be considered.

Physical Security
--------------------------

Physical security is very important, as the device that is connected to the display, will also be connected and access to the non-public internet. Therefor an intrusion can cause sensitive data leaks
or even damege, therefore we recommend that the device itself should be locked in a safe or a locker that is only accessable by staff members, 
and is connected to the monitor that displays big screen wirelessly. this can be done through chromecast, or if its a smart tv then the computer can connect to it using bluetooth.
Make sure to lock the screen after activating Big Screen for an extra secure usage. 


Network security
---------------------------

Network security is also important, since the device that is publicily display will be connected to the company network. Therefore we advice to a create an own wifi-network for the
the device or devices that will be runnin big picture. This network should have the properties of a guest network, but is password protected so that only the machines that are running big picture can access it.
Another alternative is to use a dedicated network, that is completly seperate from the company network for this device. Such options can be purchased at service-providers 
and often comes in the form of a USB stick or router that will be soly connected to the device running Big Picture.


Recommend ways to setup Big Picture
---------------------------------------------------

Since Big Picture can be seen as an only-display extension, meaning that it does not require much or any user interaction once its setup, therefore we recommend a few ways to set it up:


**Operating system level Kiosk Mode (Recommended)**

Kiosk Mode that is also called Assigned Access is a mode that comes with windows, and that allows the user to configure an account that is only allowd to use a specific
software without access to anything else like the start menu or the task manager for example, and forces the app to be in fullscreen mode. This way when a person uses the computer
that is logged in to the kiosk account, the person can only access the specified app. In this case the app will be Microsoft Edge that will run Big Screen.

In order to setup kiosk mode, we need to be logged in as Administrator, and we need to setup a new user account. This can be simply done by creating a new user in Settings > Accounts > Other people > Add someone else to this PC.
Note that the account does not have to be a microsoft account, but can also be just a local account with a password. Make sure to name the account Kiosk.

- Once that is done, open up Windows Powershell which can be found when searched for in the start menu.
- Make sure to right click and run it as Administrator.
- Type in the exact sentence following sentence: 
- Set-AssignedAccess -AppUserModelId Microsoft.MicrosoftEdge_8wekyb3d8bbwe!MicrosoftEdge -UserName Kiosk

Incase of an error, make sure to check the spelling of the sentence above, as the spelling and even the amount of spaces between each word has to be exact. 

Now that kiosk mode is up and running, it can be used by logging into the Kiosk user account which will automatically launch Microsoft Edge in full screen. All that is left to do
is to Navigate to the Big Screen page in Sharepoint, and launch Big Screen.

In order to remove the kiosk account, go to Settings > Accounts > Other people > Set up assigned Access > Click Turn off assigned access and sign out of the selected account.

**Browser-level Kiosk Mode**

Basic Kiosk Mode is a kiosk mode that is implemented in the browser Google chrome. it allows the user 


**Browser security and tips and tricks**

Additional Security
---------------------------------------------

**Startpage** 

The browser should have the startpage set to the page of big picture. Using the query string fullscreen=true (For example �https://tenant.sharepoint.com?fullscreen=true#/start/big-picture�) will cause big picture to go into full screen mode automatically.
 This will enable the computer to be rebooted but still end up on the correct page and put the browser in the correct mode.


**O365 Security**

To Run big picture, a normal user account that can login to O365 and Omnia is needed. This account should have a minimal amount of permissions. For big picture to work the account needs permissions in the following ways:

- Access to the page where the big picture Glue control is placed
- Access to any data it will show (The news center for example)
- Access to the Glue site system page (The welcome page of the Glue site called Omnia.aspx)