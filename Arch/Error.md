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