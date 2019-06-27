# System

## Delete old kernel in /boot 

```
dpkg -l linux-{image,headers}-* | awk '/^ii/{print $2}' | egrep '[0-9]+\.[0-9]+\.[0-9]+' | grep -v $(uname -r | cut -d- -f-2) | xargs sudo apt-get -y purge
```


https://askubuntu.com/questions/1083882/trying-to-free-up-space-for-some-updates-but-havent-dependency-issues-trying-to
