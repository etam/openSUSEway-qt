# openSUSEway-qt
dotfiles for Sway on openSUSE

## Screenshots
![Example screenshot](screenshot.png)

## Installation instructions

To install openSUSEway-qt, add home:etamPL:openSUSEway-kde repository:

```sh
sudo wget https://download.opensuse.org/repositories/home:/etamPL:/openSUSEway-kde/openSUSE_Tumbleweed/home:etamPL:openSUSEway-kde.repo \
    -O /etc/zypp/repos.d/home:etamPL:openSUSEway-kde.repo
sudo zypper ref
sudo zypper al \
    "gcr*" \
    "gvfs-backend*" \
    xdg-desktop-portal-gtk
sudo zypper in -t pattern openSUSEway-qt
sudo sed -i 's@/etc/greetd/sway-config@/etc/qtgreet/sway.cfg@' /etc/greetd/config.toml
sudo systemctl set-default graphical.target
sudo systemctl disable display-manager
sudo systemctl enable greetd
```

Also read the instructions in the Install section of
the [openSUSEway Portal](https://en.opensuse.org/Portal:OpenSUSEway),
but beware, that some things might be different.


## More resources
[openSUSEway Portal](https://en.opensuse.org/Portal:OpenSUSEway) for more details on the openSUSEway desktop environment for openSUSE.

[Sway openSUSE wiki page](https://en.opensuse.org/Sway) for more details about Sway on openSUSE.

Please check [Manage-dotfiles-with-Git](https://news.opensuse.org/2020/03/27/Manage-dotfiles-with-Git/) on how to use dotfiles.

## Other openSUSE sway customisation projects

  - https://sr.ht/~mcepl/moldavite/
  - https://github.com/ProjectGreybeard/Info
