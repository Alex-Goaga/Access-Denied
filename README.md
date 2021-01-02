![Logo](https://github.com/Alex-Goaga/Access-Denied/blob/main/includes/logo.png)

# Project !Access - Denied
----
[![HitCount](http://hits.dwyl.com/Alex-Goaga/Access-Denied.svg)](http://hits.dwyl.com/Alex-Goaga/Access-Denied) <img src="https://img.shields.io/github/repo-size/Alex-Goaga/Access-Denied?label=Repo%20Size&color=orange" alt="repo size" >  <img src="https://tokei.rs/b1/github/Alex-Goaga/Access-Denied">  [![Release](https://img.shields.io/github/release/Alex-Goaga/Access-Denied.svg)](https://github.com/Alex-Goaga/Access-Denied/releases/latest)   <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Alex-Goaga/Access-Denied">  <img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/y/Alex-Goaga/Access-Denied">  [![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)




----

##  🏁 **Take Note!**
* This is a work in progress and is being actively developed (for now).
* This project gathers all banned IPs from different server logs and honey pots around the plain and compress them into one compatible file for any <img src="https://raw.githubusercontent.com/Alex-Goaga/Access-Denied/main/includes/pihole-logo.png" alt="Pi-hole" height="24"/> PiHole Project or <img src="https://raw.githubusercontent.com/Alex-Goaga/Access-Denied/main/includes/synology-logo.png" alt="Pi-hole" height="24"/>  Synology DSM - Auto Block Feature
* Versions the file, and tests, are updated every week 
* Yes, any user can contribute with his honey pot list. ( *With any exception of issues regarding changes to `Access-Denied/main/deny-ip-list.txt`, all other issues regarding the content of the produced hosts files should be made with the appropriate data source that contributed the content in question. The contact information for all of the data sources can be found in the `Contributors` sections.* )
----

# 📰 Unified hosts file additional informations:

* Last updated: **January 02 2021**.
* Here's the [raw hosts file with base extensions](https://raw.githubusercontent.com/Alex-Goaga/Access-Denied/main/deny-ip-list.txt) containing 0,007 entries.

**Expectation**: This host file should serve all devices, regardless of OS ( *with a little thinkering from the end-user* ).

## Authors

* 🍻 **Alex-Goaga** - *Initial work* - (https://github.com/Alex-Goaga)

## 🔍 What is a hosts file?

A hosts file, named `hosts` (with no file extension), is a plain-text file
used by all operating systems to map hostnames to IP addresses.

In most operating systems, the `hosts` file is preferential to `DNS`.
Therefore if a domain name is resolved by the `hosts` file, the request never
leaves your computer.

Having a smart `hosts` file goes a long way towards blocking malware, adware,
and other irritants.

For example, to nullify requests to some doubleclick.net servers, adding these
lines to your hosts file will do it:

```text
# block doubleClick's servers
0.0.0.0 ad.ae.doubleclick.net
0.0.0.0 ad.ar.doubleclick.net
# etc...
```

## 🛡️ We recommend using `0.0.0.0` instead of `127.0.0.1`

Traditionally most host files use `127.0.0.1`, the *loopback address*, to establish an IP connection to the local machine.

We prefer to use `0.0.0.0`, which is defined as a non-routable meta-address used to designate an invalid, unknown, or non-applicable target.

Using `0.0.0.0` is empirically faster, possibly because there's no wait for a timeout resolution. It also does not
interfere with a web server that may be running on the local PC.

## 🛡️ Why not use `0` instead of `0.0.0.0`?

We tried that.  Using `0` doesn't work universally.


## 🔍 Location of your hosts file

To modify your current `hosts` file, look for it in the following places and modify it with a text
editor.

**macOS (until 10.14.x macOS Mojave), iOS, Android, Linux**: `/etc/hosts` file.

**macOS Catalina:** `/private/etc/hosts` file.

**Windows**: `%SystemRoot%\system32\drivers\etc\hosts` file.

## 🐌 Limitations :
*  Adding to many entries in the host file ( For example Windows C:\Windows\System32\drivers\etc\hosts ) in order to block intrusions you can end as a result, on startup, with an initial super-slow connection to the internet. ⚠️ I get the globe icon (no connection) for about 2 minutes on some tests in the Virtual Machine, then it works fine so WE DO RECOMMEND buying a separate machine for the computing DNS process such as a cheap Raspberry Pi 0 (zero) and setup the <img src="https://raw.githubusercontent.com/Alex-Goaga/Access-Denied/main/includes/pihole-logo.png" alt="Pi-hole" height="24"/> PiHole Project 


## 📜 Other

### Helpful links
* https://pi-hole.net - A great network-wide ad blocker project.

### 🏔️ TODO
- [X] Setup multiple machines around the network
- [X] Give the machines juicy names 
- [X] Open and redirect ports to public network
- [ ] Add cron script to run from cron daily/weekly/monthly
- [ ] Add additional lists to combine into one mega list
- [ ] Add installation script for automated install to PiHole
- [ ] Possibly generizie script to accept any list
- [ ] Add instructions to host the list on the pi-host itself
- [ ] Reach 10,000-caught milestone
- [ ] Reach 100,000-caught milestone
- [ ] Reach 1,000,000-caught milestone


## 📜 License

This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.

### 📜 Disclaimer
This project is in no way affiliated with the core Pi-Hole project or organization neither with Synology Systems. This project was created as a contribution to the community. Use at your own risk.
