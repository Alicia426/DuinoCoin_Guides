# DuinoCoin (DUCO) Setup for Trisquel GNU/Linux

[Trisquel GNU/Linux](https://trisquel.info/) is a fully free as in freedom Linux
distribution, based on Ubuntu but with a deblobbed Kernel to remove proprietary software.
Trisquel is a very lightweight distro. Its latest version is based on Ubuntu 18.04 LTS. It supports 32 bit systems as well.

With that philosophy in mind, it's important to note that Trisquel does not have any
repositories with proprietary software, by default.

This includes the Python Package Index also known as `pip`,
so to run DuinoCoin on Trisquel, we will have to do some tinkering.

## Steps:

1. We add this to `/etc/apt/sources.list` with our favorite editor:
```
  deb http://archive.ubuntu.com/ubuntu bionic main universe
  deb http://archive.ubuntu.com/ubuntu bionic-security main universe
  deb http://archive.ubuntu.com/ubuntu bionic-updates main universe
  ```

2. We add the following keys to prevent `apt update` from throwing errors:

```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 40976EAF437D05B5
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 3B4FE6ACC0B21F32
```

3. We run `sudo apt update`, and ignore any errors we might have.

4. We run `sudo apt install python3-pip` to install pip so `PCMiner.py` can do the auto setup.

5. We can now run `python3 PC_miner.py` and happily mine DuinoCoin.

## References:

* [Key Issue](https://chrisjean.com/fix-apt-get-update-the-following-signatures-couldnt-be-verified-because-the-public-key-is-not-available/)

* [pip not installing](https://askubuntu.com/questions/1254309/not-installing-pip-on-ubuntu-20-04)

* [Duino Coin Instructions](https://duinocoin.com/getting-started#pc)

* [Trisquel Download](https://trisquel.info/en/download)


**Thank you for reading.**
