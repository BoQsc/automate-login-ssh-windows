# automate-login-ssh-windows


Updated
```
@ECHO OFF
SET "ssh_password="
CD "%~DP0"
IF NOT EXIST plink.exe curl --location https://the.earth.li/~sgtatham/putty/latest/w64/plink.exe -O
cls
REM  echo y - confirms on storing the host key in the putty/plink cache. [required on first connection to the server.]
echo y | plink -no-antispoof root@78.140.136.25 -pw %ssh_password% dir
pause
```


```
curl https://the.earth.li/~sgtatham/putty/latest/w64/plink.exe -O
plink -batch -no-antispoof root@78.140.136.25 -pw password dir
```
Executes `dir command`


Multiple commands can be sent:
```
plink -batch -no-antispoof root@78.140.136.25 -pw boqsc1793 -m test.txt
```
Alternate version
```
plink -batch -no-antispoof root@78.140.136.25 -pw password < test.txt
```

`test.txt`
```
echo ok
dir
exit

```


## https://superuser.com/questions/1621783/putty-plink-how-to-execute-command-and-keep-shell-alive
https://github.com/cyd01/KiTTY/releases
