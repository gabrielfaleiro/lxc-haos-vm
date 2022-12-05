# lxc-haos-vm

Run HA OS as a LXC

Hardware platform is a Raspberry Pi

## Conclusion

Home Assistant cannot be easily virtualised.

## Motivation

I want to use a raspberry pi for more applications than just Home Automation.

The most complete deployment is using the operating system (https://www.home-assistant.io/installation/#compare-installation-methods)

## LXC

Not supported: https://www.home-assistant.io/more-info/unsupported/lxc/

## Multipass

REFs:
- https://www.home-assistant.io/installation/linux/
- https://github.com/home-assistant/operating-system/releases/download/9.3/haos_ova-9.3.qcow2.xz

*multipass set local.bridged-network=wlan0*

*multipass launch -vvvv -c 1 -d 32G -m 1G -n haos --network wlan0 https://github.com/home-assistant/operating-system/releases/download/9.3/haos_ova-9.3.qcow2.xz*

multipass launch -vvvv -c 1 -d 32G -m 1G -n haos --timeout 1200 https://github.com/home-assistant/operating-system/releases/download/9.3/haos_ova-9.3.qcow2.xz


# Testing
multipass launch -vvvv -d 32G -n haos --timeout 1200 file:///home/gfaleiro/Downloads/test/haos_ova-9.3.qcow2


multipass launch -vvv -c 2 -d 32G -m 4G -n haos --timeout 1200 file:///home/gfaleiro/Downloads/test/haos_ova-9.3.qcow2

