aeolus-meetbot
==============

With this repo we intend to share and store the [MeetBot](http://meetbot.debian.net/Manual.html) configuration we use for the #aeolus-meeting channel.

### Installation ###

You can install MeetBot on Fedora using yum:

```
yum install supybot-meetbot
```

After the install completed, there is no need to be root to execute supybot. As a non privileged user, after you've checked out the repo, you can run MeetBot launching `supybot` and passing the `ambot.conf` file as argument:

```
git clone git://github.com/giulivo/aeolus-meetbot.git
cd aeolus-meetbot
supybot ambot.conf
```

### Administration ###

For security reasons there is no administrative user defined by default in such a shared config. If you need to change the MeetBot configuration at runtime or if you want to change how it behaves without restarting the bot, you can add an administrative user with the `supybot-adduser` command:

```
supybot-adduser conf/users.conf
```

Don't forget to give your user the `admin` capability.

### Publishing ###

The minutes and log files from every meeting are save under `aeolus-meeting/$YEAR/`. We push only the `*html` files on the main site via a pull request against https://github.com/aeolusproject/aeolusproject.github.com , placing the logs under `cabals/release/minutes`.
