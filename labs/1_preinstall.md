01/05/2017

1. Swapiness
$ sudo cat /proc/sys/vm/swappiness
$ sudo sysctl vm.swappiness=1

<center> <img src="png/1_preinstall-swapiness.PNG"> </center>

2. Show Mount 
$ mount
$ mount -t ext

3. not required

4. Disable transparent hugepage support

$ cat /sys/kernel/mm/transparent_hugepage/enabled
$ echo never > /sys/kernel/mm/transparent_hugepage/enabled

02/05/2017