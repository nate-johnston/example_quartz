---
title: "Control Center"
---

## Host-Specific Services

### Containerized

| IP Address | Site | HTTP | coloctl | supervisord |
| ---- | ---- | ---- | ---- | ---- |
| 203.0.113.65 | Wiki | [web](http://203.0.113.65:4000/) | [ctl](http://203.0.113.65:4001/) | [supctl](http://203.0.113.65:4002/) |
| 203.0.113.66 | Gogs | [web](http://203.0.113.66:3000) | [ctl](http://203.0.113.66:4001/) | [supctl](http://203.0.113.66:4002/) |
| 203.0.113.67 | Diary | [web](http://203.0.113.67:4000/) | [ctl](http://203.0.113.67:4001/) | [supctl](http://203.0.113.67:4002/) |
| 203.0.113.68 | Start | [web](http://203.0.113.68:4000/) | [ctl](http://203.0.113.68:4001/) | [supctl](http://203.0.113.68:4002/) |
| 203.0.113.69 | Providence | [web](http://203.0.113.69:4000/) | [ctl](http://203.0.113.69:4001/) | [supctl](http://203.0.113.69:4002/) |
| 203.0.113.70 | Resume | - | - | - |
| 203.0.113.73 | hmjStudios | [web](http://203.0.113.73:4000/) | [ctl](http://203.0.113.73:4001/) | [supctl](http://203.0.113.73:4002/) |
| 203.0.113.75 | Public | [web](http://203.0.113.75:4000/) | [ctl](http://203.0.113.75:4001/) | [supctl](http://203.0.113.75:4002/) |
| 203.0.113.76 | cghoa | [web](http://203.0.113.76:4000/) | [ctl](http://203.0.113.76:4001/) | [supctl](http://203.0.113.76:4002/) |
| 203.0.113.77 | nexushome | [web](http://203.0.113.77:4000/) | [ctl](http://203.0.113.77:4001/) | [supctl](http://203.0.113.77:4002/) |
| 203.0.113.78 | johnstonfi | [web](http://203.0.113.78:4000/) | [ctl](http://203.0.113.78:4001/) | [supctl](http://203.0.113.78:4002/) |
| 203.0.113.250 | meshtest | [web](http://203.0.113.250:4000/) | [ctl](http://203.0.113.250:4001/) | [supctl](http://203.0.113.250:4002/) |

### Hostbased Services

| IP Address | Site | cockpit | monitorix | description |
| ---- | ---- | ---- | ---- | ---- |
| 203.0.113.1 | anomia | [cp](https://203.0.113.1:9090/) | [here](http://203.0.113.1:5000/monitorix) | Cloud: watchtower |
| 203.0.113.2 | munchkin | [cp](https://203.0.113.2:9090/) | - | Unifi Controller |
| 203.0.113.3 | risk | [cp](https://203.0.113.3:9090/) | - | Desktop machine |
| 203.0.113.4 | laptop | - | - | Work laptop |
| 203.0.113.5 | blackjack | [cp](https://203.0.113.5:9090/) | - | Mac Mini workhorse |
| 203.0.113.6 | catan | - | - | Mac desktop |
| 203.0.113.9 | colo | - | [here](http://203.0.113.9:8080/monitorix) | Cloud: Our websites |
| 203.0.113.10 | iphone | - | - | Nate's iPhone |
| 203.0.113.11 | kindle | - | - | Kindle Fire |
| 203.0.113.12 | ipad | - | - | old iPad |
| 203.0.113.13 | glen | - | - | Cloud: CGHOA website |
| 203.0.113.14 | wesley | - | - | Cloud: DUMC website |
| 203.0.113.15 | scarface | - | - | old MacBook laptop |


### External IP Addresses
- 51.68.197.78 - hmjstudiosllc.com / nmj3e.org / Colo main
    - 51.38.74.231 - johnston.fi
    - 51.195.140.92 - natejohnston.info
    - 54.37.241.121 - git.natejohnston.info
    - 51.195.130.253 - DECOMMISSIONED
- 54.37.241.121 - calvertsglenhoa.com (glen)

### Other Services
#### colo

- [OVH Control Panel](https://ca.ovh.com/auth/)
- [Cockpit](http://203.0.113.1:9090/)
- [Monitorix](http://203.0.113.1:8080/monitorix)
- [consul](http://203.0.113.1:8500/ui/home/kv)

#### firewall
- [Cockpit](http://203.0.113.2:9090/)
- [consul](http://203.0.113.2:8500/ui/home/kv)

#### risk
- [Home test server iLO](https://10.0.1.172) - login is iloman
    - [Commands](https://www.golinuxcloud.com/hp-ilo4-command-line-interface-cli-cheatsheet/)
    - [ssh howto](https://blog.marquis.co/posts/2016-02-13-how-to-access-hps-ilo-remote-console-via-ssh/)

#### raven
- [Ubiquiti Unifi Controller](https://192.168.1.70:8443)

## General Resources

### Home Resources

- Email
    - [POBox Control Panel](https://www.pobox.com/home)
        - [filters](https://www.pobox.com/services/filters)
        - [stats](https://www.pobox.com/home/stats)
    - [Tutanota](https://mail.tutanota.com/mail/) for pythonic@tuta.io
- [GoDaddy](https://sso.godaddy.com/?realm=idp&path=%2Fproducts&app=account)
- [Google Analytics](https://analytics.google.com/analytics/web/?authuser=1#/report-home/a3716736w221495795p210548192)
- Syncthing [localhost](http://127.0.0.1:8384/) - in case you need it
- [Fios Router](https://192.168.199.1/)
- [Front Door Camera](https://home.nest.com/camera/727e94c97f724e919cd43d6ca3a296ba)

### Google

- [nmj3e.org admin panel](https://admin.google.com/nmj3e.org/AdminHome?hl=en&pli=1&fral=1)
- [manage user accounts](https://admin.google.com/u/2/ac/users)
- [manage email lists](https://admin.google.com/u/2/ac/groups)
- [Google Search console for natejohnston.info](https://search.google.com/search-console?resource_id=https%3A%2F%2Fnatejohnston.info%2F&hl=en)
- [SyncSelect for Calendar](https://calendar.google.com/calendar/syncselect)
- [Google Analytics](https://analytics.google.com/analytics/web/?authuser=1#/report-home/a3716736w221495795p210548192)

Back to [[Nexushome]]