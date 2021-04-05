# TPLINK Tl-WR804N Exploit
This is Proof Of Concept based on CVE-2018-11714 which was found by *Thouid Shaikh*. This Issue is caused by broken session handling on firmware /cgi/ directory. That allow us to download the configuration file and gain access to admin configuration panel.

This issue affect firmware 0.9.1 3.16 v0001.0 Build 170608 Rel.58696n. And it hasn't been repaired until this time (0.9.1 4.16 v0001.0 Build 180614 Rel.40494n)
So, I would like to ask all of you for help to contact the vendor to report this issue so they can fix it as soon as possible.

## CVE Source 
https://blog.securelayer7.net/time-to-disable-tp-link-home-wifi-router/

## Requierments
- curl, bash (if you use unix).

## install the prerequisites

### Linux(Debian, Ubuntu, Kali, etc.)

```
apt-get install curl
```
