# Flatpak

ATM the flatpak manifest for the chat app has not been updated for a while. This branch can be used to build a more recent version, the latest as of this writing: v2.7.1. The result seems to work for me, but no garanties :) 

## Changes

The app was renamed, to reflect the current version, so that it will not clash with a previously installed flatpak of an earlier version. Installed as per below, the data folder for the app (e.g. models) it will end-up in the user's home folder, under e.g.: `/home/<user>/.var/app/io.gpt4all.gpt4all.v2.7.1/data/nomic.ai/GPT4All/`.

You may want to remove any older version to save disk space, see further below

## Build / Install 

```bash
flatpak install flathub com.riverbankcomputing.PyQt.BaseApp//6.5
flatpak install flathub org.kde.Platform//6.5
flatpak install flathub org.kde.Sdk//6.5
flatpak-builder --user --install --force-clean build-dir io.gpt4all.gpt4all.yml
```

# Other flatpak commands

Some other commands that may be useful:

```bash
flatpak update
flatpak list
flatpak run <app id>
flatpak uninstall <app id>
```

