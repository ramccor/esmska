## Select your operating system ##

<table align='center' cellspacing='10'>
<thead>
<tr><th>Linux</th><th>Windows</th><th>Other</th><th>Special</th></tr>
</thead>
<tbody valign='middle'>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/arch-32.png' /> <a href='#Arch.md'>Arch</a></td><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/windows-32.png' /> <a href='#Windows.md'>Windows installer</a></td><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/freebsd-32.png' /> <a href='http://www.freshports.org/comms/esmska/'>FreeBSD</a></td><td><img src='http://wiki.esmska.googlecode.com/git/icons/package-32.png' /> <a href='#Multi-platform_package.md'>Multi-platform package</a></td></tr>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/fedora-32.png' /> <a href='#Fedora.md'>Fedora</a></td><td><img src='http://wiki.esmska.googlecode.com/git/icons/portable-32.png' /> <a href='#Windows_Portable.md'>Portable version</a></td><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/macosx-32.png' /> <a href='#Mac_OS_X.md'>Mac OS X</a></td><td><img src='http://wiki.esmska.googlecode.com/git/icons/bug-32.png' /> <a href='#Unstable_releases.md'>Unstable releases</a></td></tr>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/gentoo-32.png' /> <a href='https://github.com/okias/ixit/tree/master/app-mobilephone/esmska'>Gentoo</a></td><td /><td /><td><img src='http://wiki.esmska.googlecode.com/git/icons/history.png' /> <a href='http://code.google.com/p/esmska/downloads/list'>Older releases</a></td></tr>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/mandriva-32.png' /> <a href='#Mandriva_/_Mageia.md'>Mandriva / Mageia</a></td><td /><td /><td><img src='http://wiki.esmska.googlecode.com/git/icons/source-32.png' /> <a href='http://code.google.com/p/esmska/wiki/Source?tm=4'>Source code</a></td></tr>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/opensuse-32.png' /> <a href='#openSUSE.md'>openSUSE</a></td><td /><td /><td /></tr>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/ubuntu-32.png' /> <a href='#Ubuntu.md'>Ubuntu</a></td><td /><td /><td /></tr>
<tr><td><img src='http://wiki.esmska.googlecode.com/git/icons/logo/tux-32.png' /> <a href='#Generic_Linux.md'>Generic Linux</a></td><td /><td /><td /></tr>
</tbody>
</table>

![http://wiki.esmska.googlecode.com/git/icons/info.png](http://wiki.esmska.googlecode.com/git/icons/info.png) Latest program version is: **1.9** (see [list of changes](Changelog.md))

![http://wiki.esmska.googlecode.com/git/icons/money-32.png](http://wiki.esmska.googlecode.com/git/icons/money-32.png) **Please consider a [donation](Support.md) for this open source project.**


---


## Installation details ##

### ![http://wiki.esmska.googlecode.com/git/icons/logo/arch-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/arch-32.png) Arch ###

Run this command in the terminal:
```
pacman -S esmska
```

Unstable releases can be found at [aur.archlinux.org](http://aur.archlinux.org/packages.php?ID=30579).

### ![http://wiki.esmska.googlecode.com/git/icons/logo/fedora-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/fedora-32.png) Fedora ###

Run these commands in the terminal:
```
su -
curl 'http://download.opensuse.org/repositories/Java:/esmska/common/Java:esmska.repo' -o /etc/yum.repos.d/esmska.repo
yum install esmska
```

### ![http://wiki.esmska.googlecode.com/git/icons/logo/tux-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/tux-32.png) Generic Linux ###

  * If you have a distribution using deb packages, try using the same approach as for [Ubuntu](#Ubuntu.md). If that doesn't work, try to download and install the single [deb file](http://download.opensuse.org/repositories/Java:/esmska/common-deb/all/).
  * If you have a distribution using RPM packages, try making your package manager to use [this repository](http://download.opensuse.org/repositories/Java:/esmska/common/). If that doesn't work, try to download and install the single [RPM file](http://download.opensuse.org/repositories/Java:/esmska/common/noarch/).
  * In other cases, you'll probably need to use the [multi-platform package](#Multi-platform_package.md).

### ![http://wiki.esmska.googlecode.com/git/icons/logo/macosx-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/macosx-32.png) Mac OS X ###

![http://wiki.esmska.googlecode.com/git/icons/download-24.png](http://wiki.esmska.googlecode.com/git/icons/download-24.png) [Download Esmska](https://www.dropbox.com/s/tkx81ynj4z6f348/Esmska-1.9.0.dmg?dl=0)

Requires Intel-based Mac running Mac OS X 10.7.3 (Lion) or later. Java is bundled to application so there is no need to download it manually. To install the application, open .dmg file and then drag and drop the application to your Applications folder.

If you are running Esmska for a first time, hold Control (Ctrl) key and then click on the Esmska icon. While still holding Control key, click on Open item from popup menu. Dialog will appear and after that, please confirm that you are willing to launch application downloaded from this page. This is because Esmska isn't digitally signed so OS X needs your explicit approval for security reasons. For more information, please see [[Java](Java.md)] page.

Package maintainer: [Marian Bouček](mailto:marianboucek_at_seznam_dot_cz?subject=Esmska%20Mac%20OS%20X%20package)

### ![http://wiki.esmska.googlecode.com/git/icons/logo/mandriva-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/mandriva-32.png) Mandriva / Mageia ###

Run these commands in the terminal:
```
su -
urpmi.addmedia --update petos-esmska http://petos.cz/rpm/esmska
urpmi esmska
```

Package maintainer: [Petr Šafařík](mailto:petos_at_mandrivalinux_dot_cz?subject=Esmska%20Mandriva%20package)

### ![http://wiki.esmska.googlecode.com/git/icons/logo/opensuse-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/opensuse-32.png) openSUSE ###

Click on this button [![](http://wiki.esmska.googlecode.com/git/icons/opensuse-1click.png)](http://software.opensuse.org/ymp/Java:esmska/common/esmska.ymp) or run these commands in the terminal:
```
su -
zypper addrepo 'http://download.opensuse.org/repositories/Java:/esmska/common/' esmska
zypper install esmska
```

### ![http://wiki.esmska.googlecode.com/git/icons/logo/ubuntu-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/ubuntu-32.png) Ubuntu ###

Run these commands in the terminal:

```
sudo -i
wget -q -O - http://download.opensuse.org/repositories/Java:/esmska/common-deb/Release.key | apt-key add -
echo 'deb http://download.opensuse.org/repositories/Java:/esmska/common-deb/ ./ #Esmska' > /etc/apt/sources.list.d/esmska.list
apt-get update
apt-get install esmska
```

### ![http://wiki.esmska.googlecode.com/git/icons/logo/windows-32.png](http://wiki.esmska.googlecode.com/git/icons/logo/windows-32.png) Windows ###

It is strongly recommended to uninstall any previous versions before installing a new one.

![http://wiki.esmska.googlecode.com/git/icons/download-24.png](http://wiki.esmska.googlecode.com/git/icons/download-24.png) [Download Esmska](http://ripper.profitux.cz/esmska/packages/Esmska-1.9-setup.exe)

### ![http://wiki.esmska.googlecode.com/git/icons/portable-32.png](http://wiki.esmska.googlecode.com/git/icons/portable-32.png) Windows Portable ###

You can put portable version on removable media (USB flash drives) and use it on any other Windows computer (at school, cafés, etc).

![http://wiki.esmska.googlecode.com/git/icons/download-24.png](http://wiki.esmska.googlecode.com/git/icons/download-24.png) [Download Esmska](http://ripper.profitux.cz/esmska/packages/Esmska-1.9-portable.7z)

Use [7-Zip](http://www.7-zip.org/) to unpack the archive.


---


## Special options ##

### ![http://wiki.esmska.googlecode.com/git/icons/package-32.png](http://wiki.esmska.googlecode.com/git/icons/package-32.png) Multi-platform package ###
You can download a package which works in any operating system, provided that you have [Java](Java.md) installed. Just unpack the archive and run the program.

![http://wiki.esmska.googlecode.com/git/icons/download-24.png](http://wiki.esmska.googlecode.com/git/icons/download-24.png) [Download Esmska](http://ripper.profitux.cz/esmska/packages/esmska-1.9.tar.gz)

Windows users: Use [7-Zip](http://www.7-zip.org/) to unpack the archive (twice).

### ![http://wiki.esmska.googlecode.com/git/icons/bug-32.png](http://wiki.esmska.googlecode.com/git/icons/bug-32.png) Unstable releases ###

We will be very happy if you [get involved](GetInvolved#Betatesting.md), start using our unstable beta releases and [report](Issues.md) bugs that you find. Also see the [changelog](Changelog.md).

Download:
  * Multi-platform package: _no unstable release at the moment_
  * Arch: See [instructions](#Arch.md).


---


![http://wiki.esmska.googlecode.com/git/icons/money-32.png](http://wiki.esmska.googlecode.com/git/icons/money-32.png) **Please consider a [donation](Support.md) for this open source project.**