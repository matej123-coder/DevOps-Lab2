**Homework 2 For DevOps**

Matej Minoski 211217

**Chapter 3**

1. docker info
```
Server:

Containers: 0

Running: 0

Paused: 0

Stopped: 0

Images: 0

Server Version: 27.5.1

Storage Driver: overlayfs

driver-type: io.containerd.snapshotter.v1

Logging Driver: json-file

Cgroup Driver: cgroupfs

Cgroup Version: 1

Plugins:

Volume: local

Network: bridge host ipvlan macvlan null overlay

Log: awslogs fluentd gcplogs gelf journald json-file local splunk syslog CDI spec directories:

/etc/cdi

/var/run/cdi

Swarm: inactive

Runtimes: io.containerd.runc.v2 nvidia runc

Default Runtime: runc

Init Binary: docker-init

containerd version: bcc810d6b9066471b0b6fa75f557a15a1cbf31bb

runc version: v1.1.12-0-g51d5e946

init version: de40ad0

Security Options:

seccomp

Profile: unconfined

Kernel Version: 5.15.167.4-microsoft-standard-WSL2

Operating System: Docker Desktop

OSType: linux

Architecture: x86\_64

CPUs: 8

Total Memory: 2.846GiB

Name: docker-desktop

ID: 6e6ac08b-9b9f-4019-8d73-189f16332343

Docker Root Dir: /var/lib/docker

Debug Mode: false

HTTP Proxy: http.docker.internal:3128

HTTPS Proxy: http.docker.internal:3128

No Proxy: hubproxy.docker.internal

Labels:

com.docker.desktop.address=unix:///var/run/docker-cli.sock Experimental: false

Insecure Registries:

hubproxy.docker.internal:5555

127\.0.0.0/8

Live Restore Enabled: false

WARNING: No blkio throttle.read\_bps\_device support WARNING: No blkio throttle.write\_bps\_device support WARNING: No blkio throttle.read\_iops\_device support WARNING: No blkio throttle.write\_iops\_device support WARNING: daemon is not using the default seccomp profile
```

2. docker run -i -t ubuntu /bin/bash
```
Unable to find image 'ubuntu:latest' locally

latest: Pulling from library/ubuntu

5a7813e071bf: Download complete

Digest: sha256:72297848456d5d37d1262630108ab308d3e9ec7ed1c3286a32fe09856619a782 Status: Downloaded newer image for ubuntu:latest

root@837916abefed:/#

root@837916abefed:/# hostname -l

hostname: invalid option -- 'l'

Usage: hostname [-b] {hostname**|**-F file} set host name **(**from file**)**

hostname [-a**|**-A**|**-d**|**-f**|**-i**|**-I**|**-s**|**-y] display formatted name

hostname display host name

{yp,nis,}domainname {nisdomain**|**-F file} set NIS domain name **(**from file**)** {yp,nis,}domainname display NIS domain name

dnsdomainname display dns domain name hostname -V**|**--version**|**-h**|**--help print info and exit

Program name:

{yp,nis,}domainname=hostname -y dnsdomainname=hostname -d

Program options:

-a, --alias alias names

-A, --all-fqdns all long host names **(**FQDNs**)**

-b, --boot set default hostname if none available

2

-d, --domain

-f, --fqdn, --long -F, --file

-i, --ip-address

-I, --all-ip-addresses -s, --short

-y, --yp, --nis

DNS domain name

long host name **(**FQDN**)**

read host name or NIS domain name from given file addresses for the host name

all addresses for the host

short host name

NIS/YP domain name

3

Description:

This command can get or set the host name or the NIS domain name. You can

also get the DNS domain or the FQDN **(**fully qualified domain name**)**.

Unless you are using bind or NIS for host lookups you can change the

FQDN**(**Fully Qualified Domain Name**)** and the DNS domain name **(**which is

part of the FQDN**) in** the /etc/hosts file.

root@837916abefed:/# apt-get update**;** apt-get install vim

Get:1 http://security.ubuntu.com/ubuntu noble-security InRelease [126 kB]

Get:2 http://archive.ubuntu.com/ubuntu noble InRelease [256 kB]

Get:3 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 Packages [34.0 kB]

Get:4 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Packages [1062 kB]

Get:5 http://security.ubuntu.com/ubuntu noble-security/main amd64 Packages [841 kB]

Get:6 http://archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]

Get:7 http://security.ubuntu.com/ubuntu noble-security/restricted amd64 Packages [909 kB]

Get:8 http://archive.ubuntu.com/ubuntu noble-backports InRelease [126 kB]

Get:9 http://archive.ubuntu.com/ubuntu noble/restricted amd64 Packages [117 kB]

Get:10 http://archive.ubuntu.com/ubuntu noble/main amd64 Packages [1808 kB]

Get:11 http://archive.ubuntu.com/ubuntu noble/universe amd64 Packages [19.3 MB]

Get:12 http://archive.ubuntu.com/ubuntu noble/multiverse amd64 Packages [331 kB]

Get:13 http://archive.ubuntu.com/ubuntu noble-updates/restricted amd64 Packages [955 kB]

Get:14 http://archive.ubuntu.com/ubuntu noble-updates/multiverse amd64 Packages [38.7 kB]

Get:15 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [1163 kB]

Get:16 http://archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [1345 kB]

Get:17 http://archive.ubuntu.com/ubuntu noble-backports/universe amd64 Packages [16.0 kB]

Fetched 28.6 MB in 8s **(**3384 kB/s**)**

Reading package lists... Done

Reading package lists... Done

Building dependency tree... Done

Reading state information... Done

The following additional packages will be installed:

libexpat1 libgpm2 libpython3.12-minimal libpython3.12-stdlib libpython3.12t64 libreadline8t64 libsodium23 libsqlite3-0 media-types netbase readline-common tzdata vim-common vim-runtime xxd

Suggested packages:

gpm readline-doc ctags vim-doc vim-scripts

The following NEW packages will be installed:

libexpat1 libgpm2 libpython3.12-minimal libpython3.12-stdlib libpython3.12t64 libreadline8t64 libsodium23 libsqlite3-0 media-types netbase readline-common tzdata vim vim-common vim-runtime xxd

0 upgraded, 16 newly installed, 0 to remove and 18 not upgraded.

Need to get 16.3 MB of archives.

After this operation, 72.1 MB of additional disk space will be used.

Do you want to continue? [Y/n] y

Get:1 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libexpat1 amd64 2.6.1-2ubuntu0.2 [87.4 kB]

Get:2 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libpython3.12-minimal amd64 3.12.3-1ubuntu0.5

Get:3 http://archive.ubuntu.com/ubuntu noble/main amd64 media-types all 10.1.0 [27.5 kB]

Get:4 http://archive.ubuntu.com/ubuntu noble/main amd64 netbase all 6.4 [13.1 kB]

Get:5 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 tzdata all 2024b-0ubuntu0.24.04.1 [274 kB]

Get:6 http://archive.ubuntu.com/ubuntu noble/main amd64 readline-common all 8.2-4build1 [56.5 kB]

Get:7 http://archive.ubuntu.com/ubuntu noble/main amd64 libreadline8t64 amd64 8.2-4build1 [153 kB]

Get:8 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libsqlite3-0 amd64 3.45.1-1ubuntu2.1 [701 kB]

Get:9 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libpython3.12-stdlib amd64 3.12.3-1ubuntu0.5

Get:10 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 vim-common all 2:9.1.0016-1ubuntu7.6 [385

Get:11 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 xxd amd64 2:9.1.0016-1ubuntu7.6 [63.3 kB]

Get:12 http://archive.ubuntu.com/ubuntu noble/main amd64 libgpm2 amd64 1.20.7-11 [14.1 kB]

Get:13 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libpython3.12t64 amd64 3.12.3-1ubuntu0.5 [2339

Get:14 http://archive.ubuntu.com/ubuntu noble/main amd64 libsodium23 amd64 1.0.18-1build3 [161 kB]

Get:15 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 vim-runtime all 2:9.1.0016-1ubuntu7.6 [7281

Get:16 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 vim amd64 2:9.1.0016-1ubuntu7.6 [1880 kB]

Fetched 16.3 MB in 4s **(**3944 kB/s**)**

debconf: delaying package configuration, since apt-utils is not installed

Selecting previously unselected package libexpat1:amd64.

**(**Reading database ... 4383 files and directories currently installed.**)**

Preparing to unpack .../00-libexpat1\_2.6.1-2ubuntu0.2\_amd64.deb ...

Unpacking libexpat1:amd64 **(**2.6.1-2ubuntu0.2**)** ...

Selecting previously unselected package libpython3.12-minimal:amd64.

Preparing to unpack .../01-libpython3.12-minimal\_3.12.3-1ubuntu0.5\_amd64.deb ...

Unpacking libpython3.12-minimal:amd64 **(**3.12.3-1ubuntu0.5**)** ...

Selecting previously unselected package media-types.

Preparing to unpack .../02-media-types\_10.1.0\_all.deb ...

Unpacking media-types **(**10.1.0**)** ...

Selecting previously unselected package netbase.

Preparing to unpack .../03-netbase\_6.4\_all.deb ...

Unpacking netbase **(**6.4**)** ...

Selecting previously unselected package tzdata.

Preparing to unpack .../04-tzdata\_2024b-0ubuntu0.24.04.1\_all.deb ...

Unpacking tzdata **(**2024b-0ubuntu0.24.04.1**)** ...

Selecting previously unselected package readline-common.

Preparing to unpack .../05-readline-common\_8.2-4build1\_all.deb ...

Unpacking readline-common **(**8.2-4build1**)** ...

Selecting previously unselected package libreadline8t64:amd64.

Preparing to unpack .../06-libreadline8t64\_8.2-4build1\_amd64.deb ...

Adding 'diversion of /lib/x86\_64-linux-gnu/libhistory.so.8 to /lib/x86\_64-linux-gnu/libhistory.so.8.usr-is-merged by Adding 'diversion of /lib/x86\_64-linux-gnu/libhistory.so.8.2 to /lib/x86\_64-linux-gnu/libhistory.so.8.2.usr-is-merged Adding 'diversion of /lib/x86\_64-linux-gnu/libreadline.so.8 to /lib/x86\_64-linux-gnu/libreadline.so.8.usr-is-merged Adding 'diversion of /lib/x86\_64-linux-gnu/libreadline.so.8.2 to /lib/x86\_64-linux-gnu/libreadline.so.8.2.usr-is-merged

Unpacking libreadline8t64:amd64 **(**8.2-4build1**)** ...

Selecting previously unselected package libsqlite3-0:amd64.

Preparing to unpack .../07-libsqlite3-0\_3.45.1-1ubuntu2.1\_amd64.deb ...

Unpacking libsqlite3-0:amd64 **(**3.45.1-1ubuntu2.1**)** ...

Selecting previously unselected package libpython3.12-stdlib:amd64.

Preparing to unpack .../08-libpython3.12-stdlib\_3.12.3-1ubuntu0.5\_amd64.deb ...

Unpacking libpython3.12-stdlib:amd64 **(**3.12.3-1ubuntu0.5**)** ...

Selecting previously unselected package vim-common.

Preparing to unpack .../09-vim-common\_2%3a9.1.0016-1ubuntu7.6\_all.deb ...

Unpacking vim-common **(**2:9.1.0016-1ubuntu7.6**)** ...

Selecting previously unselected package xxd.

Preparing to unpack .../10-xxd\_2%3a9.1.0016-1ubuntu7.6\_amd64.deb ...

Unpacking xxd **(**2:9.1.0016-1ubuntu7.6**)** ...

Selecting previously unselected package libgpm2:amd64.

Preparing to unpack .../11-libgpm2\_1.20.7-11\_amd64.deb ...

Unpacking libgpm2:amd64 **(**1.20.7-11**)** ...

Selecting previously unselected package libpython3.12t64:amd64.

Preparing to unpack .../12-libpython3.12t64\_3.12.3-1ubuntu0.5\_amd64.deb ...

Unpacking libpython3.12t64:amd64 **(**3.12.3-1ubuntu0.5**)** ...

Selecting previously unselected package libsodium23:amd64.

Preparing to unpack .../13-libsodium23\_1.0.18-1build3\_amd64.deb ...

Unpacking libsodium23:amd64 **(**1.0.18-1build3**)** ...

Selecting previously unselected package vim-runtime.

Preparing to unpack .../14-vim-runtime\_2%3a9.1.0016-1ubuntu7.6\_all.deb ...

Adding 'diversion of /usr/share/vim/vim91/doc/help.txt to /usr/share/vim/vim91/doc/help.txt.vim-tiny by vim-runtime'

Adding 'diversion of /usr/share/vim/vim91/doc/tags to /usr/share/vim/vim91/doc/tags.vim-tiny by vim-runtime'

Unpacking vim-runtime **(**2:9.1.0016-1ubuntu7.6**)** ...

Selecting previously unselected package vim.

Preparing to unpack .../15-vim\_2%3a9.1.0016-1ubuntu7.6\_amd64.deb ...

Unpacking vim **(**2:9.1.0016-1ubuntu7.6**)** ...

Setting up libexpat1:amd64 **(**2.6.1-2ubuntu0.2**)** ...

Setting up media-types **(**10.1.0**)** ...

Setting up libsodium23:amd64 **(**1.0.18-1build3**)** ...

Setting up libgpm2:amd64 **(**1.20.7-11**)** ...

Setting up libsqlite3-0:amd64 **(**3.45.1-1ubuntu2.1**)** ...

Setting up libpython3.12-minimal:amd64 **(**3.12.3-1ubuntu0.5**)** ...

Setting up xxd **(**2:9.1.0016-1ubuntu7.6**)** ...

Setting up tzdata **(**2024b-0ubuntu0.24.04.1**)** ...

debconf: unable to initialize frontend: Dialog

debconf: **(**No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm debconf: falling back to frontend: Readline

debconf: unable to initialize frontend: Readline

debconf: **(**Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC

debconf: falling back to frontend: Teletype

Configuring tzdata

\------------------

```
3. docker ps -a
```
CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS 837916abefed ubuntu "/bin/bash" 4 minutes ago Exited **(**0**)** About a minute ago

```

4. docker run –name bob\_the\_container -i -t ubuntu /bin/bash
```
root@544f13d3c909:/# exit exit
```


5. docker start bob\_the\_container
```
bob\_the\_container

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker ps

CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES 544f13d3c909 ubuntu "/bin/bash" 26 minutes ago Up 5 seconds bob\_the\_container
```

6. docker attach bob\_the\_container
```
matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker attach bob\_the\_container root@544f13d3c909:/# exit

exit
```


7. docker run –name dave -d ubuntu /bin/sh -c “while true; do echo hello world; sleep 1; done”

docker run --name dave -d ubuntu /bin/sh -c "while true; do echo hello world; sleep 1; done" 09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e

8. docker logs dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker logs dave hello world

hello world

hello world

hello world

hello world hello world

9. docker logs -ft dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker logs -ft dave 2025-03-09T17:51:05.650584476Z hello world 2025-03-09T17:51:06.651761155Z hello world 2025-03-09T17:51:07.653183757Z hello world 2025-03-09T17:51:08.654597204Z hello world

2025-03-09T17:51:09.655967573Z hello world 2025-03-09T17:51:10.654168511Z hello world

10. docker logs -f dave

hello world hello world hello world hello world

11. docker top dave

8

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker top dave

UID PID PPID C TIME CMD

root 1201 1182 0 00:00:00 /bin/sh -c while true**; do** echo hello world**;** sleep root 1878 1201 0 00:00:00 sleep 1

STIME

17:45 1**; done**

17:55

9

12. docker stats dave

CONTAINER ID NAME CPU % MEM USAGE / LIMIT MEM % NET I/O BLOCK I/O PIDS 09ee16511e86 dave 0.16% 836KiB / 2.846GiB 0.03% 1.05kB / 0B 0B / 0B 2

13. docker exec -t -i dave /bin/bash

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker exec -t -i dave /bin/bash

root@09ee16511e86:/# exit

exit

14. docker stop dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker stop dave

dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker ps

CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS NAMES

15. docker run –restart=always –name daemon\_alice -d ubuntu /bin/sh -c “while true; do echo hello world; sleep 1; done”

docker run --restart=always --name daemon\_alice -d ubuntu /bin/sh -c "while true; do echo hello world; sleep 1; done" 58cccd969abc35c45e8f2b2c5e5fe1e2c7353a41e3c5467dacad7d2972b49edc hello world

hello world

hello world

hello world

16. docker inspect dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker inspect dave

[

{

"Id": "09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e", **"Created": "2025-03-09T17:45:22.928889289Z",**

"Path": "/bin/sh",

"Args": [

"-c",

"while true; do echo hello world; sleep 1; done"

],

"State": {

"Status": "exited",

"Running": false,

"Paused": false,

"Restarting": false,

"OOMKilled": false,

"Dead": false,

"Pid": 0,

"ExitCode": 137,

"Error": "",

"StartedAt": "2025-03-09T17:45:23.203716124Z",

"FinishedAt": "2025-03-09T18:12:54.331962001Z"

**}**,

"Image": "sha256:72297848456d5d37d1262630108ab308d3e9ec7ed1c3286a32fe09856619a782",

"ResolvConfPath": "/var/lib/docker/containers/09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e/resolv.conf"

"HostnamePath": "/var/lib/docker/containers/09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e/hostname"

"HostsPath": "/var/lib/docker/containers/09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e/hosts"

"LogPath": "/var/lib/docker/containers/09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e/09ee16511e864837f6c1d95e2732a35031ad4966b8bad5f2ee08b843a19b782e-json.log" "Name": "/dave",

"RestartCount": 0,

"Driver": "overlayfs",

"Platform": "linux",

"MountLabel": "",

"ProcessLabel": "",

"AppArmorProfile": "",

"ExecIDs": null,

...

17. docker rm dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker rm dave

dave

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker ps -a

CONTAINER ID IMAGE COMMAND CREATED STATUS PORTS 58cccd969abc ubuntu "/bin/bash" 5 minutes ago Restarting **(**0**)** 52 seconds ago 544f13d3c909 ubuntu "/bin/bash" About an hour ago Exited **(**0**)** 41 minutes ago

**\*\* Chapter 4 \*\***

18. docker images

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker images REPOSITORY TAG IMAGE ID CREATED SIZE ubuntu latest 72297848456d 5 weeks ago 117MB

19. docker pull ubuntu:18.04

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker pull ubuntu:18.04

18\.04: Pulling from library/ubuntu

7c457f213c76: Download complete

Digest: sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e43c98 Status: Downloaded newer image for ubuntu:18.04

docker.io/library/ubuntu:18.04

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker images

REPOSITORY TAG IMAGE ID CREATED SIZE

ubuntu latest 72297848456d 5 weeks ago 117MB

ubuntu 18.04 152dc042452c 21 months ago 97.5MB

20. docker ps -a

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker run -t -i --name matej\_the\_container ubuntu:18.04 root@70a22754d115:/# exit

exit

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker ps -a

CONTAINER ID IMAGE COMMAND CREATED STATUS

70a22754d115 ubuntu:18.04 "/bin/bash" 9 seconds ago Exited **(**0**)** 5 seconds ago

21. docker search puppet

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate$ docker search puppet

NAME DESCRIPTION puppet/continuous-delivery-for-puppet-enterprise Automated testing and promotion of infrastru… 7 puppet/puppetserver A Docker Image for running Puppet Server. Wi… puppet/puppetboard The Puppet Board dashboard for PuppetDB puppet/puppetdb A Docker image for running PuppetDB puppet/puppet-dev-tools Puppet development tools such as PDK, onceov… puppet/puppet-agent Puppet Agent as a Docker Image. puppet/puppet-agent-ubuntu Puppet Agent as a Docker Image. Based on the… puppet/puppet-agent-alpine Puppet Agent as a Docker Image. Based on Alp… puppet/pdk Puppet Development Kit **(**PDK**)**

puppet/r10k r10k on a Docker image. Based on Alpine puppet/puppet-bolt Puppet Bolt as a docker image

puppet/facter Facter as a Docker Image

puppet/puppetexplorer The Puppet Explorer dashboard for PuppetDB puppet/lumogon Lumogon is the best way to inspect, analyze … puppet/tlser A tiny utility for ensuring TLS certificates… 0 puppet/kubetool

puppet/gogrpc A container for building golang projects tha… puppet/discocoreui A Docker container used to build Discovery C… puppet/iac\_release

jumanjiman/puppet Use Puppet to configure CoreOS hosts puppet/pipelines Puppet Pipelines

puppet/puppet-inventory

puppet/autogenic

puppet/kerminator-build-image

puppet/cd4pe-beta Beta release builds of Continuous Delivery f…

22. docker build -t=“matmin01/static\_web” .

docker build -t="matmin01/static\_web" .

[+] Building 11.5s **(**7/7**)** FINISHED

=> [internal] load build definition from Dockerfile

=> => transferring dockerfile: 232B

=> [internal] load metadata for docker.io/library/ubuntu:18.04 => [internal] load .dockerignore

=> => transferring context: 2B

=> [1/3] FROM docker.io/library/ubuntu:18.04@sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e4 => => resolve docker.io/library/ubuntu:18.04@sha256:152dc042452c496007f07ca9127571cb9c29697f42acbfad72324b2bb2e4 => CACHED [2/3] RUN apt-get update**;** apt-get install -y nginx

=> CACHED [3/3] RUN echo'Hi, I am in your container' >/var/www/html/index.html

=> exporting to image

=> => exporting layers

=> => exporting manifest sha256:b5315df8502750cf5ceb4900c872aec182d9a5094b8b88586f6ee682dc99427e

=> => exporting config sha256:a010ed7be80a33992823a160a2d1f901903af6f89760e45e0e234f52d21ee0e2

=> => exporting attestation manifest sha256:1fefa62f462fac922758a64aacbfbc292b44dbae4bc374e3e0ac57183b8849fe

=> => exporting manifest list sha256:11b7d068ba108e8bf43bb12a893d661b69c0bace4064a3436991ad7ff8a2e1fd

=> => naming to docker.io/matmin01/static\_web:latest

=> => unpacking to docker.io/matmin01/static\_web:latest

23. docker run -d -p 80 –name hoban matmin01/static\_web ngnix -g “daemon off;”

docker run -d -p 8080:80 --name boban matmin01/static\_web nginx -g "daemon off;" 568ec6ffefd34e533ea4a5f30c38621cc132031dc2279290e70a96c421c26fca

24. docker ps -l

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate/static\_web$ docker ps -l

CONTAINER ID IMAGE COMMAND CREATED STATUS 568ec6ffefd3 matmin01/static\_web "nginx -g 'daemon of…" About a minute ago Up About a

25. docker rmi matmin01/static\_web

matej123@DESKTOP-KFSETTO:/mnt/c/Users/mmate/static\_web$ docker rmi matmin01/static\_web Untagged: matmin01/static\_web:latest

Deleted: sha256:1af92010fa223547fe8a4e9e7f2f7360b5e5218ae97a1d2c89b4156f41425af3
12
