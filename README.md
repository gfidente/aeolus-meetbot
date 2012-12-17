aeolus-meetbot
==============

With this repo we intend to share and store the [MeetBot](http://meetbot.debian.net/Manual.html) configuration we use for the #aeolus-meeting channel.

### Installation ###

You can install MeetBot on Fedora using yum:

```
yum install supybot-meetbot
```

After the install completed, there is no need to be root to execute supyboy. As a non privileged user you can run it by checking out the repo and launching `supybot` with the `ambot.conf` file as argument:

```
git clone git://github.com/giulivo/aeolus-meetbot.git
cd aeolus-meetbot
supybot ambot.con
```

### Administration ###

For security reasons there is no administrative user defined by default in such a shared config. If you want to change the MeetBot configuration at runtime or change how it behaves without restarting, you can add one with the `supybot-adduser` command:

```
supybot-adduser conf/users.conf
```

Don't forget to give your user the `admin` capability.
