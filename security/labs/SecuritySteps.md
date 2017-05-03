Create user
sudo useradd mikaelgithub


Install MIT KDC

```
sudo yum install -y krb5-server
sudo yum install  -y openldap-clients
sudo yum -y install krb5-workstation

```
KRB5 Set the realm
```
sudo sed -i.orig 's/EXAMPLE.COM/AMAZONAWS.COM/g' /etc/krb5.conf
sudo sed -i.m1 's/kerberos.example.com/ip-172-31-17-69.us-west-2.compute.internal/g' /etc/krb5.conf
sudo sed -i.m2 's/example.com/amazonaws.com/g' /etc/krb5.conf
```
then manually uncomment required lines
Update KDC.conf
```
sudo sed -i.orig 's/EXAMPLE.COM/AMAZONAWS.COM/g' /var/kerberos/krb5kdc/kdc.conf
sudo sed -i.m1 '/dict_file/a max_life = 1d' /var/kerberos/krb5kdc/kdc.conf
sudo sed -i.m2 '/dict_file/a max_renewable_life = 7d' /var/kerberos/krb5kdc/kdc.conf
sudo sed -i.m3 's/^max_/  max_/' /var/kerberos/krb5kdc/kdc.conf
sudo sed -i.m3 '/supported_enctypes/a default_principal_flags = +renewable, +forwardable' /var/kerberos/krb5kdc/kdc.conf
sudo sed -i.m4 's/^default_principal_flags/  default_principal_flags/' /var/kerberos/krb5kdc/kdc.conf

```
Update KADM5.acl
```
sudo sed -i 's/EXAMPLE.COM/AMAZONAWS.COM/' /var/kerberos/krb5kdc/kadm5.acl

sudo kdb5_util create -s

sudo service krb5kdc start
sudo service kadmin start
```
Add admin principal and principal on KDC
```
sudo kadmin.local 
addprinc root/admin
addprinc -randkey host/kdc.amazonaws.com
ktadd host/kdc.amazonaws.com

sudo yum -y install krb5-workstation
kinit mikaelgithub/admin
klist




Create a user in Hue:
mikaelgithub / cloudera

