# qcows

## About

These qcows were made for use with [PANDA](https://github.com/panda-re/panda) and were tested as such. They are largely cloud images that have been modified.

## Properties

### Files

Usually there will be two files. A qcow and a snapshot. If you don't plan to use the snapshot there is no need to download it.

- qcows: This is the actual disk image. 
- snapshots: Usually img. Distributed for ease of use with pypanda.
- json: generated [volatility3](https://github.com/volatilityfoundation/volatility3) json symbols.

Snapshot files are generated because git lfs has a max size of 2GB. This works fine until you start adding in snapshots.

### Login

```
username: root
password: root
```

### Snapshots

`cmdline` - Logged in as root in shell. Usually run with mem=1G.


## On generating images

- Download cloud image as qcow from daily server build.
- Use tool of choice to change root password (e.g. `virt-customize -a rhel-guest-image-7.2-20160302.0.x86_64.qcow2 --root-password password:PASSW0RD`)
- Boot up device and log in. Take snapshot and save as `cmdline`.


## On PRs

Out of concern for distributing malware I will only accept PRs from known sources.
