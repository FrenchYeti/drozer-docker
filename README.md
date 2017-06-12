# How to use ?
An up-to-date fork of abstractj's Drozer dockerfile


## Troubleshooting

### ADB doesn't detect my device
It's can be a conflict between an ADB instance running on the host and ADB running from the container.
I suggest to kill ADB from the host. Identify it with the command `ps aux | grep adb` and kill it.
Now, run `adb devices` from the container, you should be show your device.

### ADB can't view USB
Ensure `/dev/mapper/usb` is binded and the parameter `--privileged` setted.
Run your container using something like it :
``
