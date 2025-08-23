# somerouter
Exploit of a router 

This repository is about exploiting a router to escalate to superuser access . Both web and Telnet shell access.
I am not disclosing the router as the router is actively being patched thorough software updates so, this repository is only a note to myself .

# Escalating to Web superuser
As the router is heavily locked down but there is a way to escalate privilage . 

goto 

``` http://192.168.101.1/index.html#/login ``` 

login thourgh your normal credentials

Open Developer Tools in your browser (F12 key or right-click → Inspect)

Go to the Console tab

Paste this code and press Enter:

```
localStorage.setItem("role", "2"); 
sessionStorage.setItem("role", "2");
location.reload();

```

 if pasting is not enabled type the following and press enter :

 ``` 'allow pasting' ```

 now there will me more options than your regular account . now go to management and Backup and restore
 export your config and you can get passwords to various accounts there

 Note: The there are various telnet accounts . The one with root is not actually root and is very limited . use user ```manu``` . Password is listed in the config but not the username . You can figure it out. 
 

