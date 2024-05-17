# Step-by-Step-Guide-to-Changing-the-Root-Password-on-Ubuntu
### Step 1: Open a Terminal

First, you need to open a terminal. You can do this by searching for "Terminal" in your applications menu or using the keyboard shortcut Ctrl+Alt+T.
### Step 2: Switch to Root User

You need to switch to the root user or use sudo to change the root password. If you are already logged in as a root user, you can skip this step.

To switch to the root user, enter the following command and provide your current user password when prompted:
```
sudo -i

```
### Step 3: Change the Root Password

Once you have root privileges, change the root password using the passwd command:
```
passwd
```
You will be prompted to enter a new password for the root user and then confirm it. Make sure to use a strong and secure password.
### Step 4: Verify the Password Change

To ensure the password has been successfully changed, you can log in as the root user with the new password. First, log out from the current session or open another terminal.
```
su -

```
Then enter the new root password to log in as the root user.
### Optional: Enable Root Login (Not Recommended)

By default, Ubuntu disables root login via SSH for security reasons. If you need to enable it (not recommended), you will need to edit the SSH configuration file.

Open the SSH configuration file:
```
sudo nano /etc/ssh/sshd_config
```
Find the line:
```
PermitRootLogin prohibit-password
````
Change it to:
```
PermitRootLogin yes
```
Save and close the file (press Ctrl+X, then Y, and Enter).

Restart the SSH service to apply the changes:
```
sudo systemctl restart ssh

```

