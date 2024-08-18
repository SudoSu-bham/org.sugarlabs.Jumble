# Jumble Activity Flatpak

Jumble is a picture matching activity, where a child learns to identify the object in a picture card and picks it from the clutter of objects behind.

To know more refer https://github.com/sugarlabs/jumble-activity.git

## How To Build

```
git clone https://github.com/SudoSu-bham/org.sugarlabs.Jumble.git
cd org.sugarlabs.Jumble
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.Jumble.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.Jumble
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.Jumble.json
```
