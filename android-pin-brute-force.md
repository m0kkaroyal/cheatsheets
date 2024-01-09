### Copy the `hid-keyboard` executable into the `/sbin/` directory

```sh
sudo cp /data/data/com.offsec.nethunter/scripts/bin/hid-keyboard /sbin/hid-keyboard
```

### Change the config file within the `Android-PIN-Bruteforce` directory

```sh
HID_KEYBOARD=/sbin/hid-keyboard
```

### Change the `/dev/hidg0` authorizations file

```sh
sudo chmod 777 /dev/hidg0
```

### Test sending keys from the NetHunter phon

In this example, the 'enter' key is sent.

```sh
echo "enter" | /sbin/hid-keyboard /dev/hidg0 keyboard
```

In this example, 'abc' keys are sent (US keyboard).

```sh
echo a b c | /sbin/hid-keyboard /dev/hidg0 keyboard
```
