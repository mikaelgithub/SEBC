[root@mel2 mikael_dauzet]# cat /var/kerberos/krb5kdc/kdc.conf
[kdcdefaults]
 kdc_ports = 88
 kdc_tcp_ports = 88
[realms]
 MIKAELGITHUB.PA = {
  #master_key_type = aes256-cts
  acl_file = /var/kerberos/krb5kdc/kadm5.acl
  dict_file = /usr/share/dict/words
  max_renewable_life = 7d
  max_life = 1d
  admin_keytab = /var/kerberos/krb5kdc/kadm5.keytab
  supported_enctypes = aes128-cts:normal des3-hmac-sha1:normal arcfour-hmac:normal ca
mellia256-cts:normal camellia128-cts:normal des-hmac-sha1:normal des-cbc-md5:normal d
es-cbc-crc:normal
  default_principal_flags = +renewable, +forwardable
 }