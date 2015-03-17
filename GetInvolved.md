# Get involved #

Help us to improve and further develop this project, all the users will appreciate it. You can:

  * [report problems](Issues.md)
  * [translate](https://translations.launchpad.net/esmska) program to your native language
  * help to answer the questions in the [support forum](https://answers.launchpad.net/esmska) (you can subscribe as an answer contact)
  * [test beta-versions](#Betatesting.md) of Esmska and help to find and eliminate newly arisen problems by reporting them soon enough
  * provide a [new gateway support](GatewayHowto.md) ([list of requests](http://code.google.com/p/esmska/issues/list?q=label:Type-Gateway))
  * regularly create [installable packages](Download.md) for your favourite Linux distribution
  * create some [graphics](Banners.md) for the program (icons, banners, splash screen)
  * help with programming
  * [support project](Support.md)

## Announcements ##

If you want to get involved in Esmska, like being a translator, a betatester or a package maintainer, please subscribe to the ![http://wiki.esmska.googlecode.com/git/icons/feed.png](http://wiki.esmska.googlecode.com/git/icons/feed.png) [feed](http://feeds.launchpad.net/esmska/announcements.atom) of the [announcements](https://launchpad.net/esmska/+announcements). You could also be interested in some of the [project feeds](http://code.google.com/p/esmska/feeds).

## Betatesting ##

Betatesting means using unstable development releases instead of stable releases. You will have earlier access to new features, but program may be unstable. If you want to use beta versions, please subscribe to the [announcements](#Announcements.md) and download and use an [unstable release](Download#Unstable_releases.md). Consult the [changelog](Changelog.md) to see the list of changes. Please [report](Issues.md) all problems that you find, thank you!

## Package maintainers ##

If you want to build the package from program sources, you can check-out any program version from its git repository:

```
$ git clone git://github.com/kparal/esmska.git
$ git tag               # lists all tags
$ git checkout TAG
```

Be sure to read [README](https://github.com/kparal/esmska/raw/master/README) file to see instructions how to build it. You can also make use of some additional helpful files located at [resources](https://github.com/kparal/esmska/tree/master/resources) directory. Especially [esmska.desktop](https://github.com/kparal/esmska/raw/master/resources/esmska.desktop) is an important file, because it contains localized menu entries for operating systems. Be sure to always update this file in your package. If you make packages from program binaries you can use this command to get the latest version of the file:

```
$ wget https://github.com/kparal/esmska/raw/master/resources/esmska.desktop
```

Worth mentioning is also the [esmska.conf](https://github.com/kparal/esmska/raw/master/include/esmska.conf) file, which can be used for setting system-wide configuration.

If you are looking for RPM/DEB control files used for packaging Esmska, you can see them at [openSUSE Build Service](https://build.opensuse.org/package/files?package=esmska&project=Java%3Aesmska).

## Development ##

The development is conducted in [Java SE](http://www.oracle.com/technetwork/java/javase/overview/index.html) language and [Swing](http://docs.oracle.com/javase/tutorial/uiswing/) graphical toolkit, all of that with the use of [NetBeans IDE](http://www.netbeans.org/). You need to have some basic knowledge to help us with programming, particularly of Swing, but you certainly don't have to be an expert.

## Contact ##

If you want to get involved, you may contact me on email _kamil_ dot _paral_ at _gmail.com_. Insert the word _Esmska_ to the email subject.