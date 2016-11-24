# Interesting links

Linux performance: http://www.slideshare.net/brendangregg/linux-performance-tools-2014
TCP TIME-WAIT & les serveurs Linux à fort trafic: https://vincent.bernat.im/fr/blog/2014-tcp-time-wait-state-linux.html


# Interesting commands

Mount a RAM disk:
```shell
$ mount -t tmpfs -o size=8g tmpfs /mnt/ramdisk
```

Measure network perf:
    On the target
```shell
$ nc -l 1234 > tmpfile2
```

On the source
```shell
$ sudo  dd if=/dev/zero of=tmpfile1 bs=1M  count=4000
$ cat tmpfile1 | nc MachineCible 1234
```
