# README #

### ShadowSocks on Debian Draft ###

* Version 15.07.17

### How do I get set up? ###

* 

* First step - `add repository key wget -O- http://shadowsocks.org/debian/1D27208A.gpg | sudo apt-key add -`

* For Debian Wheezy, Ubuntu 12.04 with libssl > 1.0.0

`echo "deb http://shadowsocks.org/debian wheezy main" >> /etc/apt/sources.list`

* For Debian Squeeze, Ubuntu 11.04 with libssl > 0.9.8, but < 1.0.0

`echo "deb http://shadowsocks.org/debian squeeze main" >> /etc/apt/sources.list`

* `apt-get update && apt-get install shadowsocks-libev`

* Copy /etc/shadowsocks-libev/config.json

* Then key in `service shadowsocks-libev restart`

* Check service `netstat -tulpan | grep ss-server`

* Copy config to client (config.json)

* And start local service `shadowsocks-local -c="config.json"`

* Edit browser settings: change proxy type to SOCKS5, use address 127.0.0.1, port 1080

* Connect to Internet, enjoy

UPD: https://shadowsocks.com (latest alive site)

### Who do I talk to? ###

* Repo owner CyberManiac