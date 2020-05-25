# penguinsOnWhale

Helps develop scripts and software by automatizing test runs in multiple Docker images at the same time.


### Dependencies

Works with the following setup:

 - Python 3.6.9 as `python3` in $PATH
 - Docker 19.03.9 as `docker` in $PATH
 - GNOME Terminal 3.28.2 as `gnome-terminal` in $PATH

But it is likely to work with similar versions on any GNU Linux with the `gnome-terminal` available on bash4, probably bash5.


### Installation

Download and run:

```bash
./penguinsOnWhale --install
```

Follow the instructions


### Usage

Help output:

```
Usage: penguinsOnWhale [--here] <image>
  or:  penguinsOnWhale [OPTION]

Runs a given docker <image> in a new terminal identified by section name in the config file as per configuration.
When used with --here key, runs in current terminal without invoking new one

 Options:
 --help                displays this message
 --version             displays general info about the program
 --reinstall           runs "/opt/penguinsOnWhale/installator.sh" script
 --all                 runs all images defined in the config file as per configuration
 --create-config       creates new config file
 --create-config-full  creates new config file with all possible configs specified
```


Default config file (created with `penguinsOnWhale --create-config`):

```
[Program settings]
docker_images_prefix = 
docker_mount_source = 
docker_mount_destination = 
terminal_profile = penguinsOnWhale
cmd = ls
cmd_arg1 = -la

[ubuntu18.04]
docker_image = ubuntu:18.04
terminal_name = Ubuntu 18.04

[fedora31]
docker_image = fedora:31
terminal_name = Fedora 31

[amazonlinux2]
docker_image = amazonlinux:2
terminal_name = Amazon Linux 2

```



