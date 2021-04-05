# TPLINK Tl-WR804N Exploit
This is Proof Of Concept based on CVE-2018-11714 which was found by *Thouid Shaikh*. This Issue is caused by broken session handling on firmware /cgi/ directory. That allow us to download the configuration file and gain access to admin configuration panel.

firmware 0.9.1 3.16 v0001.0 Build 170608 Rel.58696n. And it hasn't been repaired until right now (0.9.1 4.16 v0001.0 Build 180614 Rel.40494n) 

## CVE Source 
https://blog.securelayer7.net/time-to-disable-tp-link-home-wifi-router/
