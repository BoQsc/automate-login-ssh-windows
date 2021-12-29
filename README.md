# automate-login-ssh-windows
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
