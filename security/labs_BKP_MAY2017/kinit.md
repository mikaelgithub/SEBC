Command to test user
```
kinit root/admin
```

Output from Klist
```
[ec2-user@ip-172-31-17-69 ~]$ klist
Ticket cache: KEYRING:persistent:1000:krb_ccache_azmV0mT
Default principal: root/admin@AMAZONAWS.COM

Valid starting       Expires              Service principal
05/03/2017 11:57:06  05/04/2017 11:57:06  krbtgt/AMAZONAWS.COM@AMAZONAWS.COM
        renew until 05/10/2017 11:57:06
```