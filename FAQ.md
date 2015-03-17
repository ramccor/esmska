# Questions #



![http://wiki.esmska.googlecode.com/git/icons/info.png](http://wiki.esmska.googlecode.com/git/icons/info.png) If your question is not answered here, ask us. Just visit [Esmska Answers](https://answers.launchpad.net/esmska).

![http://wiki.esmska.googlecode.com/git/icons/info.png](http://wiki.esmska.googlecode.com/git/icons/info.png) Do you have a problem? See [Problems](Problems.md).

## Where are the program configuration files stored? ##

  * Linux (and similar): `~/.config/esmska` (configuration files) and `~/.local/share/esmska` (data files)
  * Mac OS: `~/Library/Application Support/Esmska`
  * Windows XP: `C:\Documents and Settings\<user>\Application Data\esmska`
  * Windows Vista/7: `C:\Users\<user>\AppData\Roaming\esmska`
  * Esmska portable: The files are stored in the `config` folder in the program directory.

> Note: Character `~` denotes user home directory, as usual.<br />
> Note: The configuration directories are often hidden by default in file managers.

## Where is the program log stored? ##
> You can find the log:
    * Mac OS: `~/Library/Logs/Esmska.log`
    * Other systems: `console.log` in your [configuration directory](#Where_are_the_program_configuration_files_stored?.md)

> The log is mainly useful when solving problems. When reporting issues the developers will probably ask you for it.

## How to send a message to multiple people? ##
> Just hold _Control_ or _Shift_ and select more people in your contact list. The displayed number of written messages is computed according to the "worst" gateway from the group of people.

> Note: Mac OS users will use the _⌘ Cmd_ key instead of _Control_.

## When will it be possible to send messages to MY favorite gateway? ##
> It is not possible that we support every thinkable world gateway. But we created a [pluggable gateway system](GatewayHowto.md) which allows _anyone_ (even you) with a little skill to create the support for that gateway. It consists only from a simple file which describes how to send a message through that gateway. It should be easy for any average programmer. Send us this file (or find someone who can do it) and we will include it in a subsequent release.

## How to import contacts from my favorite application? ##
> The application must support exporting contacts to vCard format (vcf file) or it must natively supported by Esmska (see _Import contacts_ dialog). Here is some more info for popular applications:
    * Gmail - supports exporting contacts to vCard
    * Mozilla Thunderbird - install [MoreFunctionsForAddressBook](http://nic-nac-project.de/~kaosmos/morecols-en.html) extension, open address book, right click on _Personal Contacts_ folder and choose _Export as vcf_.

## How can I create a launcher on desktop/panel? ##
> The easiest way is usually to install the program from installable package created for your operating system or use [Java WebStart](JavaWebStart.md).

> If you want to use the system-independent package, you have these possibilities:
    * Linux users may add a [launcher](https://help.ubuntu.com/community/HowToAddaLauncher) anywhere. Use `esmska.sh` file as a _Command_ and `icons/esmska.svg` as an _Icon_.
    * Windows users can create a shortcut to `esmska.exe`.

> There are some icons placed in the program folder so you can attach an icon to your new launcher. I recommend using the SVG icon which you can scale to any size without losing any quality. (Unfortunately Windows users can use only the ICO icon because the system does not allow them any better format.)

## Is it possible to run the program from removable drive (e.g. usb flashdrive)? ##
> There is a portable version of the program available for MS Windows, see [Download](Download.md) page.

> Second option is to run the program from a terminal with option `--portable`, i.e.
```
./esmska.sh --portable
```
> or on Windows:
```
java -jar esmska.jar --portable
```

> The program will let you choose the location of the configuration files. Therefore you can easily carry them (even with the program) on a removable drive.

## Does the program have some advanced settings? ##
> Run the program from terminal with the option `--help`, i.e.
```
./esmska.sh --help
```
> or on Windows:
```
java -jar esmska.jar --help
```
> or on Windows without [Java](Java.md) installed (using the bundled one):
```
jre\bin\java.exe -jar esmska.jar --help
```

> Note for Windows users: If you have a non-english locale, you will see just a mess in the terminal instead of national characters. This is not a program fault, it's a Windows problem. You can use `java -Dfile.encoding=CpXXX -jar ...` to see it correctly (replace `CpXXX` with windows terminal codepage for your locale, eg. `Cp852` for Czech locale), but after that the output redirection will mess the characters again. Say Wow.

> Note for Mac users: If you installed Esmska from dmg file, it's kind of hard to run it from the terminal - you have to traverse inside to the app bundle, where program files are located. Second option is to download common platform-independent package and use that one.

## How to use Esmska easily on multiple computers? ##
> You'd probably like to have all your contacts/settings/history synchronized on all your computers. Esmska doesn't have native support for that. But you can use some third-party tool like [Dropbox](https://www.dropbox.com/) and synchronize your [configuration directory](#Where_are_the_program_configuration_files_stored?.md).

> Read more at [SyncOtherFolders](http://wiki.dropbox.com/TipsAndTricks/SyncOtherFolders) and [Symlink Semantics and Workarounds](http://wiki.dropbox.com/Symlink%20Semantics%20and%20Workarounds).

> **Note:** Never have Esmska running on multiple computers simultaneously, the program doesn't support that and you could lose some data.

> Example setup for Linux:
  1. Stop Dropbox on both computers. Quit Esmska.
  1. Back up your data.
```
mv ~/.config/esmska ~/.config/esmska_backup
```
  1. Create symbolic links from the Dropbox folder to your configuration folder on both computers.
```
mkdir ~/.config/esmska
ln -s ~/.config/esmska ~/Dropbox/esmska
```
  1. Start Dropbox on both computers.
  1. Copy all your data from backup back to your configuration directory.
```
cp -r ~/.config/esmska_backup/* ~/.config/esmska
```

> Second solution: Place the portable version of Esmska to the Dropbox folder. That will make the whole program cloned on all your computers.

## I want to disable the splashscreen ##
  * Linux: Edit the `esmska.sh` startup script and replace `java -jar esmska.jar` with `java -splash: -jar esmska.jar`.
  * Mac: Right mouse on application → Show package contents → enter Contents → edit [Info.plist](http://skitch.com/algi/bjtt7/emska-info) → expand Java → remove SplashFile key → save.
  * Windows: In the program directory create `esmska.bat` file containing:
```
@start javaw -splash: -jar esmska.jar %*
```
> and always run the program by this file.

## I want to run the program in a different language ##
> Esmska respects the language of your system. If you change your system language setting, Esmska will run in that language (provided that it is [translated](https://translations.launchpad.net/esmska) into that one).

> You can also run the program in a custom language by this command:
```
java -Duser.language=en -jar esmska.jar
```
> where you can replace `en` (English) with your language code (as defined in [ISO 639-1](http://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)).

## When a new program version will be out? ##
> A new version is released after some substantial changes. Usually this is in a range of few months.

## Is some other possibility how to send SMS apart from this program? ##
> There is many of similar programs, even non-commercial, but most of them only for MS Windows. There is another good possibility working for all systems, which is sending SMS right from your IM client by using Jabber SMS transport. For example the [jabbim.com](http://www.jabbim.com/) Jabber server offers free messages to Czech GSM gateways. This way sending a SMS looks like sending of a standard IM message and has a great advantage that you have all your contacts always with you, wherever you are (in café, in work) - just run a standard/web [Jabber](http://en.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol) client and you can happily send messages.

## Will there be Esmska for Android/iPhone/Windows Mobile? ##

> Definitely not, it would require to re-write Esmska from scratch. But there are some good alternatives already available for mobile phones, just search around. For example:
  * https://market.android.com/details?id=cz.vojtisek.freesmssender
  * http://wiki.androidforum.cz/index.php/SMS_zadarmo

## How can I support the project? ##
> By many ways, from donations to blogging about this project and telling all your friends. You can read more details on the [Support](Support.md) page. Thank you!