### Install ffmpeg to Ubuntu

##### Precondition:
Ubuntu 14.04

##### Related reference:
[*One*](http://askubuntu.com/questions/432542/is-ffmpeg-missing-from-the-official-repositories-in-14-04)
[*Two*](https://lists.ubuntu.com/archives/technical-board/2011-June/000911.html)
[*Three*](https://launchpad.net/~mc3man/+archive/ubuntu/trusty-media)

##### Procedure:

+ nano /etc/apt/sources.list<p>
`deb http://ppa.launchpad.net/mc3man/trusty-media/ubuntu trusty main`<p>
`deb-src http://ppa.launchpad.net/mc3man/trusty-media/ubuntu trusty main`<p>

+ apt-get update<p>
PS: It will show some information below:
`W: GPG error: http://ppa.launchpad.net trusty InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 90BD7EACED8E640A`<p>

+ apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 90BD7EACED8E640A<p>

        Executing: gpg --ignore-time-conflict --no-options --no-default-keyring --homedir /tmp/tmp.xR6qd3C9Z9 --no-auto-check-trustdb --trust-model always --keyring /etc/apt/trusted.gpg --primary-keyring /etc/apt/trusted.gpg --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 90BD7EACED8E640A
        gpg: requesting key ED8E640A from hkp server keyserver.ubuntu.com
        gpg: key ED8E640A: public key "Launchpad PPA for Doug McMahon" imported
        gpg: Total number processed: 1
        gpg:               imported: 1  (RSA: 1)

+ apt-get update
+ apt-get install ffmpeg
