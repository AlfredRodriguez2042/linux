## KDE-Plasma

transparency:
System Settings ---> Display and Monitor ---> Compositor.
conky:
Downgraded to 1.9.0 and modified /etc/pacman.conf to "IgnorePkg = conky". Working fine again.

### terminal vscode fontFamily

"terminal.integrated.fontFamily": "MesloLGS NF",

### git service error in vscode

Writing login information to the keychain failed with error 'The name org.freedesktop.secrets was not provided by any .service files'.
As a summary, the solution (I am on arch) was to do install gnome keyring and qtkeychain

```sh
$ yay -S qtkeychain gnome-keyring
```

- Verify it is present with

```sh
cat /usr/share/dbus-1/services/org.freedesktop.secrets.service
```

![img](/images/giterror.png)

### databse conflics

- So, I simply deleted the aforementioned file with command:

```sh
sudo rm /var/lib/pacman/db.lck && sudo pacman -Syu
```

### LibClamAV Error: cli_loaddbdir()

- All you have to do is run the commands below and then try again and everything should work as far as ClamAV is concerned:

```
sudo service clamav-freshclam stop
sudo freshclam
sudo service clamav-freshclam start
```

- scan

```
sudo clamscan -rv /home/you-user
```

### Virtual box

- usb problems
  add virtual box extencion pack
- usb problems persist

```
     sudo gpasswd -a user vboxusers
```
