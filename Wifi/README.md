# Configure Wifi

## Install wireless-tools

	aptitude install wireless-tools

## Get card informations

	lspci -nn | grep Network
	# 03:00.0 Network controller [0280]: Intel Corporation Centrino Wireless-N 1030 [Rainbow Peak] [8086:008a] (rev 34)


## Installer iwlwifi

[https://wiki.debian.org/iwlwifi] https://wiki.debian.org/iwlwifi

### Add a "non-free" component to /etc/apt/sources.list, for example:

	# Debian 8 "Jessie"
	deb http://httpredir.debian.org/debian/ jessie main contrib non-free

### Update the list of available packages and install the firmware-iwlwifi package:

	# apt-get update && apt-get install firmware-iwlwifi

### As the iwlwifi module is automatically loaded for supported devices, reinsert this module to access installed firmware:

	# modprobe -r iwlwifi ; modprobe iwlwifi
