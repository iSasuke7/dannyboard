# dannyboard
A simpler alternative to [razercfg](http://bues.ch/cms/hacking/razercfg.html),
tailored specifically for the DeathAdder 2013 for Synapse-like seamless setting
changes.

## Compiling
```
$ cargo build --release
```

## Installing
Create the group `razer` and add yourself to it then:
```
# cargo install --root /usr/local
# sudo install -m644 50-da2013.rules /etc/udev/rules.d
# udevadm control --reload
# udevadm trigger
```

## Dependencies
Only `libudev` is required. This will only work on Linux kernels since it relies
on the `hidraw` API.

## Usage
See `dannyboard --help` for more info.

## Distro packages
- PKGBUILDs are available in the AUR for Arch Linux and most derivatives:
  [stable](https://aur.archlinux.org/packages/dannyboard/), [git](https://aur.archlinux.org/packages/dannyboard-git).
