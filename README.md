# What is SteamCMD?

The Steam Console Client or SteamCMD is a command-line version of the Steam client. Its primary use is to install and update various dedicated servers available on Steam using a command-line interface. It works with games that use the SteamPipe content system. All games have been migrated from the deprecated HLDSUpdateTool to SteamCMD. 

This image can be used as a base image for Steam-based dedicated servers.

# How to use this image

Whilst it's recommended to use this image as a base image of other game servers, you can also run it in an interactive shell using the following command:

```
$ docker run -it --name=steamcmd cm2network/steamcmd bash
$ ./home/steam/steamcmd/steamcmd.sh +login anonymous +force_install_dir /home/steam/squad-dedicated \
    +app_update 403240 +quit
```

This can prove useful if you are just looking to test a certain game server installation.

# Configuration:

The image's default user is `steam`, any command executed in a higher layer `Dockerfile` will therefor be executed as that user.

The `steamcmd.sh` can be found at the following path: `/home/steam/steamcmd`
