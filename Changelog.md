# Changelog #

### In development ###
  * _there is no further development of Esmska_

### 1.9 ###
  * added new gateways `[CZ]GoSMSGo` and `[CZ]Poslat.cz` (thanks Franta Mizera, [issue #468](https://code.google.com/p/esmska/issues/detail?id=#468), [issue #469](https://code.google.com/p/esmska/issues/detail?id=#469))
  * announced the end of Esmska development and maintenance

### 1.8 ###
  * _released 2nd July 2014_
  * don't crash with gateways with unknown message length ([issue #463](https://code.google.com/p/esmska/issues/detail?id=#463))
  * always set problem detail when sending is unsuccessful ([issue #464](https://code.google.com/p/esmska/issues/detail?id=#464))
  * improve user signature handling

### 1.7 ###
  * _released 23rd June 2014_
  * gateway updates
  * moved signature to message start (thanks Petr Matas, https://github.com/kparal/esmska/pull/8)
  * added a way to easily add new contacts from unknown numbers (thanks tomas kozak, https://github.com/kparal/esmska/pull/12, [issue #255](https://code.google.com/p/esmska/issues/detail?id=#255))
  * When a message is split into several fragments (to be sent separately), they are no longer visible as separate pieces in the history (which makes it hard to forward the message), but they are instead visible as the original single message. (thanks Lenka Saidlova, https://github.com/kparal/esmska/pull/10, [issue #185](https://code.google.com/p/esmska/issues/detail?id=#185))
  * gateway script API changed: removed `SENDER_NAME`, `getExtraSignatureLength()` and `getMaxParts()`
  * show the user signature inside the message text
  * split message text by word boundaries (thanks Pavel Zak, https://github.com/kparal/esmska/pull/13, [issue #110](https://code.google.com/p/esmska/issues/detail?id=#110))

### 1.6 ###
  * _released 20th December 2013_
  * reverted back the change from version 1.5, because if caused problems with recent Java versions. As a result. `[CZ]t-zones` gateway stays broken, because of their certificate issues. ([issue #454](https://code.google.com/p/esmska/issues/detail?id=#454))

### 1.5 ###
  * _released 5th December 2013_
  * trust self-signed SSL certificates ([issue #454](https://code.google.com/p/esmska/issues/detail?id=#454))

### 1.4 ###
  * _released 3rd June 2013_
  * fixed gateway `[CZ]T-mobile` ([issue #438](https://code.google.com/p/esmska/issues/detail?id=#438))
  * be faster when sending successive messages for `[CZ]T-mobile`
  * `[CZ]t-zones`: fix gateway for users of Mych5 tariff ([issue #440](https://code.google.com/p/esmska/issues/detail?id=#440), thanks Martin Pavlásek)
  * `[CZ]O2_(registrace)`: fix detection of invalid credentials ([issue #437](https://code.google.com/p/esmska/issues/detail?id=#437))
  * `[LT]dos.lt`: add sender number support ([issue 445](https://code.google.com/p/esmska/issues/detail?id=445))
  * `[CZ]T-mobile`, `[CZ]t-zones`: fix certificate problems ([issue #443](https://code.google.com/p/esmska/issues/detail?id=#443))
  * `[CZ]PoslatSMS.cz`: removed gateway due to frequent complaints ([issue #390](https://code.google.com/p/esmska/issues/detail?id=#390))
  * compose a whole message from its parts when editing queue ([issue #152](https://code.google.com/p/esmska/issues/detail?id=#152), thanks Tomáš Jiříček)
  * `[CZ]O2_(registrace)`: remove captcha, not needed anymore ([issue #433](https://code.google.com/p/esmska/issues/detail?id=#433))

### 1.3 ###
  * _released 1st December 2012_
  * notify when paid SMS is sent for `[CZ]t-zones` and `[CZ]Vodafone park` ([question 202235](https://answers.launchpad.net/esmska/+question/202235))
  * fixed gateway `[CZ]O2 SMSender`
  * fixed gateways `[CZ]O2` and `[CZ]O2 (registrace)` (thanks Filip Oščádal, [issue #423](https://code.google.com/p/esmska/issues/detail?id=#423))
  * fixed gateways `[CZ]Vodafone` and `[CZ]Vodafone park` (thanks Filip Oščádal, [issue #426](https://code.google.com/p/esmska/issues/detail?id=#426))
  * fixed gateways `[CZ]T-mobile` and `[CZ]t-zones` ([issue #431](https://code.google.com/p/esmska/issues/detail?id=#431), [issue #432](https://code.google.com/p/esmska/issues/detail?id=#432))
  * fixed gateway `[CZ]Vodafone` ([issue #435](https://code.google.com/p/esmska/issues/detail?id=#435))
  * don't update gateways that require more recent program version ([issue #425](https://code.google.com/p/esmska/issues/detail?id=#425))
  * fixed gateways `[CZ]O2` and `[CZ]O2 (registrace)` ([issue #436](https://code.google.com/p/esmska/issues/detail?id=#436))

### 1.2 ###
  * _released 22nd January 2012_
  * send usage info less frequently to avoid high server load
  * fix compilation errors on Java 7
  * fixed gateway `[CZ]O2 (registrace)` ([issue #416](https://code.google.com/p/esmska/issues/detail?id=#416))
  * fix mysterious crashes when configuring gateways ([issue #415](https://code.google.com/p/esmska/issues/detail?id=#415))
  * add Mac OS packaging scripts

### 1.1 ###
  * _released 3rd December 2011_
  * ignore diacritical marks when searching in contact list
  * disable notification icon in Gnome 3 ([issue #404](https://code.google.com/p/esmska/issues/detail?id=#404))
  * `[CZ]O2 (registrace)`: fix problems when sending messages too quickly ([issue #412](https://code.google.com/p/esmska/issues/detail?id=#412))
  * `[CZ]O2` and `[CZ]O2 (registrace)`: fix gateway changes ([issue #413](https://code.google.com/p/esmska/issues/detail?id=#413))
  * add new gateway `[INT]Odorik.cz` ([issue #309](https://code.google.com/p/esmska/issues/detail?id=#309))
  * fix gateway `[CZ]KlikniAVolej` ([issue #414](https://code.google.com/p/esmska/issues/detail?id=#414))

### 1 ###
  * _released 28th August 2011_
  * `[CZ]t-zones`: fix sending long messages when using english interface ([issue #397](https://code.google.com/p/esmska/issues/detail?id=#397))
  * new program icon (thanks Vítězslav Válka)
  * don't crash when no gateway credentials are filled in but the gateway requires it
  * added new gateway `[CZ]SMS Manager` (thanks Lukáš Pulda)

### 0.22.2 ###
  * _released 28th July 2011_
  * fix occasional warning about incorrect number format when pasting a number into the recipient field
  * `[CZ]t-zones`: work correctly for english web localization ([issue #395](https://code.google.com/p/esmska/issues/detail?id=#395))
  * don't erase gateway properties (signatures, etc) on gateway update

### 0.22.1 ###
  * _released 2nd July 2011_
  * `[CZ]Vodafone`: fix gateway and decrese message delay to 0 sec ([issue #383](https://code.google.com/p/esmska/issues/detail?id=#383), [question 161831](https://answers.launchpad.net/esmska/+question/161831))
  * fix crash when no problem description is provided in the gateway script ([issue #386](https://code.google.com/p/esmska/issues/detail?id=#386))

### 0.22 ###
  * _released 16th June 2011_
  * `[CZ]t-zones`: fix frequent gateway-overloaded messages ([issue #340](https://code.google.com/p/esmska/issues/detail?id=#340))
  * fix focus problems on Win 7 in sending progress dialog ([issue #341](https://code.google.com/p/esmska/issues/detail?id=#341))
  * fix single instance mode problems in Windows ([issue #345](https://code.google.com/p/esmska/issues/detail?id=#345))
  * show confirm dialog when deleting messages from queue ([issue #347](https://code.google.com/p/esmska/issues/detail?id=#347))
  * enable automatic gateway updates, remove old manual update dialog ([issue #315](https://code.google.com/p/esmska/issues/detail?id=#315))
  * `[CZ]Vodafone`: fix gateway changes ([issue #351](https://code.google.com/p/esmska/issues/detail?id=#351), [issue #366](https://code.google.com/p/esmska/issues/detail?id=#366))
  * add new gateway `[CZ]KlikniAVolej` gateway ([issue #339](https://code.google.com/p/esmska/issues/detail?id=#339))
  * add signature profiles, allow per-gateway signature profiles ([issue #87](https://code.google.com/p/esmska/issues/detail?id=#87), [issue #306](https://code.google.com/p/esmska/issues/detail?id=#306))
  * only enable signature options for those gateways that support it ([issue #354](https://code.google.com/p/esmska/issues/detail?id=#354))
  * don't crash program when settings.xml file is invalid ([issue #357](https://code.google.com/p/esmska/issues/detail?id=#357))
  * disallow running Esmska with using OpenJDK + WebStart (IcedTea) because of many present bugs in IcedTea ([issue #335](https://code.google.com/p/esmska/issues/detail?id=#335), [issue #357](https://code.google.com/p/esmska/issues/detail?id=#357), [issue #358](https://code.google.com/p/esmska/issues/detail?id=#358))
  * delete invalid local gateways on program start ([issue #359](https://code.google.com/p/esmska/issues/detail?id=#359))
  * allow only one program instance to be running
  * add sender name signature into SMS text manually if it is not supported by the gateway ([issue #355](https://code.google.com/p/esmska/issues/detail?id=#355))
  * delete `[INT]sms4you` gateway, provide `[INT]SMSpoint` gateway instead ([issue #363](https://code.google.com/p/esmska/issues/detail?id=#363))
  * fix `[CZ]PoslatSMS.cz` gateway ([issue #370](https://code.google.com/p/esmska/issues/detail?id=#370), [issue #377](https://code.google.com/p/esmska/issues/detail?id=#377))
  * remove `[CZ]SMSmánia (O2)` gateway ([issue #371](https://code.google.com/p/esmska/issues/detail?id=#371))
  * implement sending program usage info ([issue #267](https://code.google.com/p/esmska/issues/detail?id=#267))
  * improve error descriptions for sms failures, add "resend" button ([issue #251](https://code.google.com/p/esmska/issues/detail?id=#251))
  * slightly improve startup performance ([issue #378](https://code.google.com/p/esmska/issues/detail?id=#378))
  * moderately improve startup performance by loading gateways asynchronously after showing main window ([issue #380](https://code.google.com/p/esmska/issues/detail?id=#380))

### 0.21 ###
  * _released 6th March 2011_
  * fixed gateway `[CZ]Vodafone` ([issue #294](https://code.google.com/p/esmska/issues/detail?id=#294), [issue #329](https://code.google.com/p/esmska/issues/detail?id=#329), [issue #333](https://code.google.com/p/esmska/issues/detail?id=#333))
  * fixed dialog focus issue on Mac OS ([issue #301](https://code.google.com/p/esmska/issues/detail?id=#301))
  * new icon for `[INT]SMSdiscount` ([issue #303](https://code.google.com/p/esmska/issues/detail?id=#303), thanks Tomáš Kováčik)
  * updated Substance themes to version 6.1
  * improved user interface - important buttons have text description now
  * `[CZ]Vodafone` gateway now silently ignores invalid sender number (see [issue #306](https://code.google.com/p/esmska/issues/detail?id=#306))
  * show info label when queue is paused ([issue #296](https://code.google.com/p/esmska/issues/detail?id=#296))
  * allow to edit or delete sms from queue only when it is not currently being sent (it's not yet supported anyway)
  * hide gateway name for multisend mode ([issue #310](https://code.google.com/p/esmska/issues/detail?id=#310))
  * fixed `[CZ]Vodafone` gateway not reporting errors correctly
  * fixed `[CZ]O2` and `[CZ]O2 (registrace)` gateways ([issue #319](https://code.google.com/p/esmska/issues/detail?id=#319))
  * fix insufficient credit message for `[INT]SMSdiscount` gateway ([issue #323](https://code.google.com/p/esmska/issues/detail?id=#323), thanks Tomáš Kováčik)
  * bundle Java into the Windows installer
  * Windows uninstaller will automatically delete any leftover files in Esmska directory
  * added new gateway `[CZ]PoslatSMS.cz` ([issue #325](https://code.google.com/p/esmska/issues/detail?id=#325), thanks Filip Oščádal)
  * remove gateway `[CZ]Vodafone samoobsluha` (operator ended supporting it)
  * add back `[SK]Orange` and `[SK]Orange (platený)` gateways ([issue #183](https://code.google.com/p/esmska/issues/detail?id=#183), thanks Tomáš Kováčik)
  * change the algorithm for suggesting preferred gateway ([issue #326](https://code.google.com/p/esmska/issues/detail?id=#326))
  * completely rework configuration tabs with gateway preferences, allow to mark gateways as hidden and favorite ([issue #237](https://code.google.com/p/esmska/issues/detail?id=#237))
  * change dialog to display error messages and security code requests to non-modal, all-in-once dialog ([issue #251](https://code.google.com/p/esmska/issues/detail?id=#251))
  * don't throw exception in About frame when Desktop API is not supported ([issue #337](https://code.google.com/p/esmska/issues/detail?id=#337))
  * add new gateway `[CZ]smska.cz` ([issue #290](https://code.google.com/p/esmska/issues/detail?id=#290))

### 0.20.0 ###
  * _released 24th July 2010_
  * fixed changes in `[CZ]T-mobile` and `[CZ]t-zones` gateways ([issue #274](https://code.google.com/p/esmska/issues/detail?id=#274))
  * allow compressing of just selected text ([issue #250](https://code.google.com/p/esmska/issues/detail?id=#250))
  * ensure that correct message from history is deleted when the history is updated in the meantime ([issue #272](https://code.google.com/p/esmska/issues/detail?id=#272))
  * altered algorithm for suggesting recommended gateway, should work better now and also should not report false errors in information boxes ([issue #273](https://code.google.com/p/esmska/issues/detail?id=#273))
  * renamed all references of "operators" to "gateways", both in source code and in filesystem structure
  * correctly show warning message about invalid credentials for `[CZ]Vodafone samoobsluha` gateway, inform about supported Java versions ([issue #271](https://code.google.com/p/esmska/issues/detail?id=#271))
  * enable parallel sms queues again ([issue #279](https://code.google.com/p/esmska/issues/detail?id=#279))
  * fix problem where moving messages up and down the queue would mark other than first message as being ready ([issue #248](https://code.google.com/p/esmska/issues/detail?id=#248))
  * fix broken gateway `[CZ]O2` ([issue #284](https://code.google.com/p/esmska/issues/detail?id=#284))
  * added new gateway `[CZ]O2 (registrace)` ([issue #286](https://code.google.com/p/esmska/issues/detail?id=#286))
  * added new gateway `[CZ]Vodafone park` ([issue #246](https://code.google.com/p/esmska/issues/detail?id=#246), thanks Csaba Botoš)

### 0.19.0 ###
  * _released 23rd May 2010_
  * show gateway info when hovering mouse over gateway combobox ([issue #243](https://code.google.com/p/esmska/issues/detail?id=#243))
  * added `[INT]sms4you` gateway, removed `[LT]sms4you` gateway ([issue #245](https://code.google.com/p/esmska/issues/detail?id=#245))
  * clean log files created by multiple program instances ([issue #195](https://code.google.com/p/esmska/issues/detail?id=#195))
  * added new gateway `[CZ]O2 SMSender` ([issue #73](https://code.google.com/p/esmska/issues/detail?id=#73))
  * disable IPv6 support in Java on Linux, because it breaks networking on Ubuntu and Debian ([issue #252](https://code.google.com/p/esmska/issues/detail?id=#252))
  * fixed exception when editing gateway for multiple contacts ([issue #254](https://code.google.com/p/esmska/issues/detail?id=#254))
  * notify user about uncaught program exceptions in modal dialogs ([issue #256](https://code.google.com/p/esmska/issues/detail?id=#256))
  * added new gateway `[INT]SMS Global` ([issue #261](https://code.google.com/p/esmska/issues/detail?id=#261), thanks Peng Duan)
  * display infinity sign in message progress bar tooltip when there is no limit on characters ([issue #259](https://code.google.com/p/esmska/issues/detail?id=#259))
  * updated Substance library to version 6.0 ([issue #253](https://code.google.com/p/esmska/issues/detail?id=#253))
  * documented CSV fields in config files ([issue #266](https://code.google.com/p/esmska/issues/detail?id=#266))
  * fix `[CZ]Vodafone` gateway problem when user signature was not filled in - added workaround when Vodafone sends an invalid URL ([issue #269](https://code.google.com/p/esmska/issues/detail?id=#269))
  * inform a user that `[CZ]Vodafone samoobsluha` is no longer usable on Java 6 Update 19 and higher due to insecure server certificate ([issue #271](https://code.google.com/p/esmska/issues/detail?id=#271))

### 0.18.0 ###
  * _released 12th February 2010_
  * handle gateway delays correctly even if user messed up system time in the meantime ([issue #198](https://code.google.com/p/esmska/issues/detail?id=#198))
  * allow several redirects to the same URL ([issue #201](https://code.google.com/p/esmska/issues/detail?id=#201))
  * fix gateway `[CZ]t-zones` ([issue #207](https://code.google.com/p/esmska/issues/detail?id=#207), thanks radomir.orkac)
  * updated vCard manipulation library
  * add new gateway `[INT]GoSMS` ([issue #210](https://code.google.com/p/esmska/issues/detail?id=#210), thanks tomas.kovacik)
  * added possibility to enable or disable advanced controls visibility
  * don't inform about updates of hidden gateways ([issue #192](https://code.google.com/p/esmska/issues/detail?id=#192))
  * user is warned if he selects probably inappropriate gateway ([issue #199](https://code.google.com/p/esmska/issues/detail?id=#199))
  * on first program run user is asked for default country prefix ([issue #199](https://code.google.com/p/esmska/issues/detail?id=#199))
  * allow gateway to provide additional hint when asking for security image ([issue #211](https://code.google.com/p/esmska/issues/detail?id=#211))
  * updated Substance library to 5.3
  * don't notify about updates when running from Java Webstart ([issue #221](https://code.google.com/p/esmska/issues/detail?id=#221))
  * allow gateways to become deprecated
  * removed `[SK]Orange` and `[SK]Orange (platený)` gateways ([issue #183](https://code.google.com/p/esmska/issues/detail?id=#183))
  * improved failure checks for `[INT]SMSdiscount` ([issue #214](https://code.google.com/p/esmska/issues/detail?id=#214))
  * 'message too long' error message now mentions charsets ([issue #214](https://code.google.com/p/esmska/issues/detail?id=#214))
  * fix downloading updates with Java 6u18 ([issue #236](https://code.google.com/p/esmska/issues/detail?id=#236))
  * handle duplicated gateway scripts loading correctly ([issue #235](https://code.google.com/p/esmska/issues/detail?id=#235))

### 0.17.0 ###
  * _released 13th October 2009_
  * when composing new message and trying to edit existing message from the queue, ask the user whether to replace the text
  * fix program freeze with redo function ([issue #160](https://code.google.com/p/esmska/issues/detail?id=#160))
  * add new gateway `[SK]Orange (platený)`, fix paid accounts problem with `[SK]Orange` gateway ([issue #158](https://code.google.com/p/esmska/issues/detail?id=#158), thanks Tomáš Kováčik and Ladislav Matěj)
  * fix problems with downloading gateways containing non-ascii characters in their names, mainly on Windows ([issue #164](https://code.google.com/p/esmska/issues/detail?id=#164))
  * fix swapping of sms sender name and sms sender number when reloading esmska ([issue #176](https://code.google.com/p/esmska/issues/detail?id=#176))
  * fix problems with charset in messages for some gateways
  * fixed `[CZ]t-zones` gateway ([issue #177](https://code.google.com/p/esmska/issues/detail?id=#177))
  * semantics of debug modes changed a little
  * program output is saved to file `console.log` into user configuration directory (easier bug reporting!)
  * display an error dialog if there is some uncaught program exception caused by Esmska (easier bug reporting!)
  * create checkbox in settings to enable debug mode (even easier bug reporting!)
  * all gateway script files must now contain only ascii characters in filenames, which solves problems on some platforms (guess which) and in some tools ([issue #159](https://code.google.com/p/esmska/issues/detail?id=#159))
  * changed type of encryption of gateway passwords → program startup is faster! (about 600ms less on my 2GHz CPU)
  * improved appearance on Mac OS X (unified toolbar support)
  * removed many icons from main menu to improve readability
  * exit button is displayed in toolbar only when program notification icon is visible (then window close does not quit the program and therefore the button makes sense)
  * older user-local gateway scripts are deleted when newer version is present system-wide (should improve startup speed)
  * fix alternate text color in sms pane was not readable on dark substance skins ([issue #181](https://code.google.com/p/esmska/issues/detail?id=#181))
  * display main window properly when iconified and started again in Windows ([issue #182](https://code.google.com/p/esmska/issues/detail?id=#182))
  * warn if current program version is older than user config files ([issue #186](https://code.google.com/p/esmska/issues/detail?id=#186))
  * fixed gateway `[INT]SMSdiscount` ([issue #187](https://code.google.com/p/esmska/issues/detail?id=#187), [issue #188](https://code.google.com/p/esmska/issues/detail?id=#188))
  * fixed gateway `[CZ]T-mobile` ([issue #189](https://code.google.com/p/esmska/issues/detail?id=#189))

### 0.16.0 ###
  * _released 5th July 2009_
  * fixed problems with charset in vCard files
  * added different notification icons for states when program is idle and when it has some message in the queue ([issue #57](https://code.google.com/p/esmska/issues/detail?id=#57))
  * text area in history frame now can be expanded
  * provide a manager for entering security codes instead of many dialogs ([issue #141](https://code.google.com/p/esmska/issues/detail?id=#141))
  * added `[LT]sms4you` gateway ([issue #144](https://code.google.com/p/esmska/issues/detail?id=#144))
  * fixed non-working link in czech localization ([issue #145](https://code.google.com/p/esmska/issues/detail?id=#145))
  * added `[DK]CoolSMS (FriSMS)` gateway ([issue #146](https://code.google.com/p/esmska/issues/detail?id=#146), thanks Julius Bartkus)
  * enabled Ctrl+F and Delete shortcut in history frame
  * updated Substance library to version 5.2
  * added `[DK]CoolSMS (GratisSMS)` gateway ([issue #150](https://code.google.com/p/esmska/issues/detail?id=#150), thanks Julius Bartkus)
  * enabled automatic regular backups of user configuration files
  * shortened delay interval for `[CZ]T-mobile` gateway
  * fixed `[CZ]O2` gateway ([issue #151](https://code.google.com/p/esmska/issues/detail?id=#151), thanks hrubis)
  * when updating gateway in program directory set read permissions for everyone ([issue #155](https://code.google.com/p/esmska/issues/detail?id=#155))
  * added new gateway `[LT]dos.lt` ([issue #154](https://code.google.com/p/esmska/issues/detail?id=#154))

### 0.15.0 ###
  * _released 17th April 2009_
  * in contact list doubleclick now edits contact, middleclick writes new message
  * added update manager - from now on, you can download gateway updates without needing to update the whole program! ([issue #80](https://code.google.com/p/esmska/issues/detail?id=#80), [issue #81](https://code.google.com/p/esmska/issues/detail?id=#81))
  * added options to choose whether you want to check just program updates, just gateway updates, both or none; also for unstable versions
  * added system-wide configuration file - very useful for Linux package maintainers ([issue #121](https://code.google.com/p/esmska/issues/detail?id=#121))
  * created portable program version for MS Windows ([issue #12](https://code.google.com/p/esmska/issues/detail?id=#12))
  * improved manipulation with vCard files - parsing should be more stable now and should support different character encondings (quoted-printable, etc) ([issue #70](https://code.google.com/p/esmska/issues/detail?id=#70), [issue #71](https://code.google.com/p/esmska/issues/detail?id=#71))
  * fixed problem with `[CZ]O2` gateway - seems they have declared war on us ([issue #131](https://code.google.com/p/esmska/issues/detail?id=#131))
  * added gateway `[CZ]SMSmánia (O2)` to help with persistent problems with `[CZ]O2` gateway. Not much of a better solution unfortunately.
  * a vCard file can be dropped on contact list or an application icon (on Mac) to import contacts (thanks Marian Bouček)
  * a text containing name or phone number can be dropped on contact list to add new contact
  * accept organizations as contact names in vCard files ([issue #135](https://code.google.com/p/esmska/issues/detail?id=#135))

### 0.14.1 ###
  * _released 19th March 2009_
  * prevent data loss when saving configuration on modern filesystems like ext4 ([LP #317781](https://bugs.launchpad.net/ubuntu/+source/linux/+bug/317781))
  * fixed operator `[CZ]T-mobile` ([issue #119](https://code.google.com/p/esmska/issues/detail?id=#119))
  * fixed operator `[CZ]t-zones` ([issue #118](https://code.google.com/p/esmska/issues/detail?id=#118))
  * improved setting proxy in GUI ([issue #101](https://code.google.com/p/esmska/issues/detail?id=#101))

### 0.14.0 ###
  * _released 16th March 2009_
  * removed option to set border decorations (let's simplify things)
  * improved some icons ([issue #103](https://code.google.com/p/esmska/issues/detail?id=#103))
  * fixed displaying of 'š' character on OpenJDK ([issue #105](https://code.google.com/p/esmska/issues/detail?id=#105))
  * updated Substance library to 5.1 (fixes [issue #108](https://code.google.com/p/esmska/issues/detail?id=#108))
  * when user has no contacts defined show a little hint how to add one
  * fixed not showing Hebrew translation in program
  * rewritten basic classes allowing easier development in the future. This is a huge change and will require thorough testing.
  * user is better informed if import finds no new contacts
  * when program update is available clicking on the statusbar will open a download page in user's browser
  * added package for FreeBSD (thanks martinko)
  * improved intelligence when suggesting operator in contact editing
  * fixed typing operator passwords with special keyboard layouts (like Czech), added "show password" checkbox ([issue #115](https://code.google.com/p/esmska/issues/detail?id=#115))
  * added clickable links to operator website to error messages
  * fix `[CZ]Vodafone samoobsluha` gateway not to throw unknown error when something bad happens ([issue #115](https://code.google.com/p/esmska/issues/detail?id=#115))
  * added tooltip to each of the available gateway in the combobox with summary information
  * changed debug commandline option syntax
  * default Substance skin is now Business Black Steel
  * fix problem when removing old history records on program exit ([issue #117](https://code.google.com/p/esmska/issues/detail?id=#117))
  * fix problem when editing gateway for multiple contacts at once
  * contact list operations are recorded in the program log
  * http and https proxies should be finally working ([issue #101](https://code.google.com/p/esmska/issues/detail?id=#101), thanks Marek Palatinus)

### 0.13.0 ###
  * _released 26th January 2009_
  * added `--version` command line option to show program version
  * toolbar is visible by default now
  * program licensing is more carefully described
  * changed a few icons
  * added `--debug` command line option to show debugging output (also useful for debugging operator scripts)
  * added the new [Nimbus](http://java.sun.com/developer/technicalArticles/javase/java6u10/#nimbus) look-and-feel instead of the old Metal on platforms that support it (Java 6 Update 10 and higher). In program preferences available under "Crossplatform" option.
  * fixed button order in dialogs under KDE
  * in preferences dialog only really relevant look-and-feels should be shown now. No more duplicates.
  * fixed non-working mnemonics on some buttons
  * added README file to the program sources (useful for package maintainers)
  * added option to build sources without Mac OS proprietary library (useful for package maintainers)
  * updated Substance library to 5.1dev, small fonts on KDE3 should be finally solved ([issue #89](https://code.google.com/p/esmska/issues/detail?id=#89))
  * user data are now continuously saved during program execution, not only on program exit. No more lost data when system crashes. ([issue #56](https://code.google.com/p/esmska/issues/detail?id=#56))
  * user data are now saved when program ended by control signals (SIGHUP, SIGINT, SIGKILL). Unfortunatelly Gnome does not use these signals when logging out. ([issue #67](https://code.google.com/p/esmska/issues/detail?id=#67))
  * queue list and contact list tooltips are now prettier
  * added combobox to preferences to select country prefix easily according to country
  * allowed editing of multiple contacts at once
  * fix country prefixes of countries starting with +1 (except US and Canada)
  * replaced bat launcher with exe launcher for those still using the wrong operating system
  * improved ICO image, windows users will now have nicer shortcuts
  * provided new Linux distribution packages (openSUSE, Fedora, Mandriva) (thanks Michal Vyskočil)
  * provided MS Windows installer ([issue #100](https://code.google.com/p/esmska/issues/detail?id=#100))

### 0.12.2 ###
  * _released 18th November 2008_
  * updated `[CZ]O2` gateway because operator has changed the website ([issue #93](https://code.google.com/p/esmska/issues/detail?id=#93))
  * removed extraneous `&` characters from notification icon menu items ([issue #92](https://code.google.com/p/esmska/issues/detail?id=#92))
  * fixed having program hidden in system tray and unchecking "show notification icon" in preferences

### 0.12.1 ###
  * _released 9th November 2008_
  * reverted Substance library back to 4.2 because it caused many problems (showing security code window, rendering queue panel) ([issue #89](https://code.google.com/p/esmska/issues/detail?id=#89), [issue #91](https://code.google.com/p/esmska/issues/detail?id=#91))

### 0.12.0 ###
  * _released 8th November 2008_
  * fixed problem in `[CZ]t-zones` script when sending multiple messages ([issue #75](https://code.google.com/p/esmska/issues/detail?id=#75), thanks David Watzke)
  * program internationalized and translated to English (and some other community-provided languages)
  * added new gateway `[SK]Orange` ([issue #84](https://code.google.com/p/esmska/issues/detail?id=#84), thanks Tomáš Kováčik)
  * added new menu items to easily ask question, translate program or report error
  * enhanced program preferences with possibility of showing simple/advanced options
  * added new gateway `[INT]SMSdiscount` ([issue #85](https://code.google.com/p/esmska/issues/detail?id=#85), [issue #90](https://code.google.com/p/esmska/issues/detail?id=#90), thanks Tomáš Kováčik)
  * fixed problem in `[CZ]T-mobile` script when using english locale ([issue #83](https://code.google.com/p/esmska/issues/detail?id=#83))
  * added new `--debug-network` and `--debug-network-full` command line options to easily debug network communication
  * added new gateway `[CZ]SMS.cz` ([issue #88](https://code.google.com/p/esmska/issues/detail?id=#88), thanks Igor Štefanko)
  * updated Substance library - one more skin, faster redrawing, fixes extremely small fonts on KDE 3 ([issue #89](https://code.google.com/p/esmska/issues/detail?id=#89))

_The older changelog records are available only in the ![http://wiki.esmska.googlecode.com/git/icons/lang/cs.png](http://wiki.esmska.googlecode.com/git/icons/lang/cs.png) Czech language._

### 0.11.1 ###
  * _vydáno 4. září 2008_
  * aktualizován skript pro O2 kvůli úpravě brány na straně operátora (zásluha Zdeněk Burian)
  * aktualizován skript pro t-zones kvůli úpravě brány na straně operátora ([issue #69](https://code.google.com/p/esmska/issues/detail?id=#69))
  * přidána podpora pro volně přístupnou bránu pro T-Mobile ([issue #68](https://code.google.com/p/esmska/issues/detail?id=#68))

### 0.11.0 ###
  * _vydáno 9. srpna 2008_
  * opraveno schovávání splashscreenu při minimalizovaném startu ([issue #55](https://code.google.com/p/esmska/issues/detail?id=#55))
  * Cmd+W na hlavním okně na Mac OS již neukončuje program, pouze schovává
  * při exportu kontaktů se program dotazuje na přepsání existujícího souboru ([issue #63](https://code.google.com/p/esmska/issues/detail?id=#63))
  * přidána brána pro Vodafone Samoobsluhu ([issue #11](https://code.google.com/p/esmska/issues/detail?id=#11), vytvořil Martin Jansa)
  * políčko pro výběr příjemce je inteligentnější, umožňuje zadat číslo i jméno
  * aktualizován skript pro Vodafone, aby korektně zobrazoval chybové hlášky operátora
  * aktualizován skript pro t-zones, aby správně nahlásil neúspěšné přihlášení
  * přidána možnost požadovat doručenku zprávy (aktuálně podporuje pouze t-zones)

### 0.10.0 ###
  * _vydáno 21. června 2008_
  * program je možné spustit na Mac OS X Leopard (s Javou od Applu) nebo na OpenJDK
  * přidáno kontextové menu do seznamu kontaktů
  * opravena brána t-zones, která hlásila chybu, když se odesílala sms delší než 1 zpráva
  * z nastavení odebrána volba "neukládat frontu" v rámci zpřehlednění a malé používanosti uživateli
  * opraven problém při importu vCard kontaktu bez telefonního čísla
  * při importu z vCard nyní program inteligentněji vybírá výchozí číslo u kontaktů s více čísly
  * při importu kontaktů je nyní výsledný seznam seřazen dle abecedy
  * posílání zpráv nyní respektuje prodlevu definovanou operátorem, prodleva se zobrazuje u každé zprávy ve frontě
  * zprovozněno současné posílání zpráv na různé operátory
  * přidána možnost nastavit maximální počet dní, po kterou uchovávat historii odeslaných zpráv
  * přidána možnost spouštět program minimalizovaně s ikonou v oznamovací oblasti ([issue #55](https://code.google.com/p/esmska/issues/detail?id=#55))
  * opraveno počitadlo celkového počtu zpráv, pokud má uživatel zapnutý podpis ([issue #54](https://code.google.com/p/esmska/issues/detail?id=#54))
  * nová ikona programu ([issue #53](https://code.google.com/p/esmska/issues/detail?id=#53))
  * odstraněna z nastavení položka "pamatovat rozvržení formuláře", to by měla být automatická vlastnost každého programu
  * vyřešen problém s ořezáváním chybových dialogů pod systémovým vzhledem ve Windows
  * vylepšena interakce s myší v seznamu kontaktů (při zobrazení kontextové nabídky je označen příslušný kontakt, v seznamu se dá posunovat pomocí kolečka)
  * přidán další ukazatel průběhu při psaní zprávy, zobrazující naplnění jednotlivých aktuálních zpráv textem ([issue #58](https://code.google.com/p/esmska/issues/detail?id=#58))
  * přidána kontextová nabídka do fronty zpráv ([issue #59](https://code.google.com/p/esmska/issues/detail?id=#59))
  * opraveno pořadí tlačítek u dialogů u GTK, Mac a Windows vzhledu

### 0.9.0 ###
  * _vydáno 10. května 2008_
  * program vás varuje (do konzole), pokud se jej pokusíte spustit na nepodporované verzi Javy (GCJ, OpenJDK, atd)
  * program již nespadne, pokud není požadovaný typ vzhledu dostupný - zejména šlo o GTK na Windows ([issue #48](https://code.google.com/p/esmska/issues/detail?id=#48))
  * program je nyní možno spouštět přímo z webového prohlížeče pomocí [Java WebStart](JavaWebStart.md)
  * byla přidána kontextová nabídka pro práci se schránkou u nejdůležitějších textových polí i pro jiné vzhledy, než je jen Substance ([issue #39](https://code.google.com/p/esmska/issues/detail?id=#39))
  * dialogy s velmi dlouhými zprávami od operátora se již nezobrazují širší než obrazovka ([issue #38](https://code.google.com/p/esmska/issues/detail?id=#38))
  * reference na knihovny projektu jsou nyní v relativních cestách, takže je možné pomocí antu projekt sestavit ihned po stažení, netřeba spouštět NetBeans a nastavovat knihovny
  * po spuštění programu se ve stavovém řádku zobrazuje "tip dne"
  * při vkládání příliš dlouhého textu do zprávy (např. ze schránky) se nyní text patřičně ořízne a je zobrazeno upozornění ve stavovém řádku ([issue #47](https://code.google.com/p/esmska/issues/detail?id=#47))
  * skripty operátorů nyní mají možnost zobrazit ve stavovém řádku programu nějakou dodatečnou zprávu od operátora (například počet volných sms)
  * t-zones nyní zobrazuje počet zbývajících volných sms
  * již by neměly v seznamu dělat problémy kontakty se stejným číslem a operátorem, případně odlišným operátorem ([issue #36](https://code.google.com/p/esmska/issues/detail?id=#36))
  * při změně brány u rozepsané zprávy se zachová jméno kontaktu. To pomáhá zejména při prohlížení historie.
  * přidána možnost zobrazení ikony programu v oznamovací oblasti. Program se dá do této ikony schovat a v kontextové nabídce jsou dostupné základní operace s programem. Bohužel ikona není dostupná pod moderními kompozitními správci oken (Compiz, Beryl, ...), bude až od Java 6 Update 10. Taktéž je vzhled nabídky velice škaredý, nelze ani přidat ikonky. Samotná hlavní ikona je neprůhledná. V tomto pro Javu mnoho bodů dolů.
  * přidána možnost importovat kontakty z vCard souborů (`*`.vcard, `*`.vcf), například z gammu/wammu ([issue #45](https://code.google.com/p/esmska/issues/detail?id=#45), [issue #23](https://code.google.com/p/esmska/issues/detail?id=#23))
  * přidána možnost exportovat kontakty do vCard souboru
  * licence programu byla změněna na [GNU Affero General Public License v3](http://www.gnu.org/licenses/agpl.html)

### 0.8.0 ###
  * _vydáno 8. dubna 2008_
  * při spuštění programu se automaticky označí naposledy použitý kontakt
  * vytvořena podpora pro operátory fungující jako zásuvné moduly. Nyní je možné, aby si uživatel sám napsal vlastní skript pro zvoleného operátora a přidal si ho do programu nahráním do příslušného adresáře. Účel je samozřejmě ten, aby uživatel poté zaslal ten skript tvůrci programu, který ho poté zařadí mezi oficiální skripty do následujícího vydání programu. ([issue #20](https://code.google.com/p/esmska/issues/detail?id=#20))
  * veškerá čísla se nyní zpracovávají v plně mezinárodním formátu
  * ukládání konfiguračních souborů je nyní bezpečnější. Data by se již neměly ztratit, pokud dojde k problému při ukládání - zachová se předchozí verze souboru.
  * při importu je nyní možnost zvolit, zda importovat kontakty s neznámým operátorem
  * uživatel si může zvolit výchozí prefix země, čímž se mu zjednoduší spousta formulářových polí. Tento prefix se program pokusí automaticky nastavit podle uživatelova národního prostředí při prvním startu.
  * uživatel si může zvolit filtr pro zobrazené operátory
  * možnost zkopírovat protokol do systémové schránky
  * program varuje, pokud je již jednou spuštěn
  * přidána podpora pro uživatelská jména/hesla u jednotlivých operátorů. Nyní lze tedy vytvářet podporu i pro operátory požadující přihlášení.
  * přidána podpora pro t-zones ([issue #5](https://code.google.com/p/esmska/issues/detail?id=#5))
  * přidána možnost nastavení proxy

### 0.7.0 ###
  * _vydáno 2. února 2008_
  * možnost spouštění programu uprostřed obrazovky
  * přidána možnost zobrazit si nástrojovou lištu s některými často používanými akcemi ([issue #34](https://code.google.com/p/esmska/issues/detail?id=#34))
  * jednotlivé motivy vzhledu lze nyní přepínat bez restartu programu
  * přidán dialog pro zobrazení protokolu (logu) aplikace
  * navigační nabídka je nyní snad přehledněji rozčleněná
  * při úpravě kontaktů jsou nesprávně vyplněná pole barevně odlišena
  * přidán grafický ukazatel volného místa při psaní smsky
  * zkrácena prodleva kontroly napsaného textu ve zprávě (obarvování apod) z 500ms na 100ms, máme rychlé procesory
  * okno s historií zpráv se již automaticky aktualizuje po odeslání nové zprávy ([issue #35](https://code.google.com/p/esmska/issues/detail?id=#35))
  * opraven problém, kdy na Windows nešlo pomocí příkazové řádky zvolit jiný adresář s konfiguračními soubory
  * přidáno hledání v historii odeslaných zpráv
  * přidáno hledání v seznamu kontaktů ([issue #19](https://code.google.com/p/esmska/issues/detail?id=#19))

### 0.6.0 ###
  * _vydáno 5. ledna 2008_
  * esmska.sh může být spuštěno i z jiného adresáře nebo pomocí symbolických odkazů, postará se o korektní nastavení aktuálního adresáře
  * do nastavení přidána volba, zda odstraňovat diakritická znaménka ze zpráv
  * do nástrojové lišty přidána akce pro kompresi aktuálně psané zprávy
  * do seznamu vzhledů přidán GTK look and feel - použitelné v prostředí KDE, XFCE, apod., kde Java standardně zobrazuje Metal vzhled, ačkoli v některých distribucích se GTK vzhled umí přizpůsobit i jiným prostředím než GNOME a tudíž se tam dá použít ([issue #22](https://code.google.com/p/esmska/issues/detail?id=#22))
  * .bat spouštěč pro Windows již nenechává otevřené terminálové okno
  * program po startu kontroluje, zda nevyšla novější verze programu. Lze vypnout v nastavení. ([issue #10](https://code.google.com/p/esmska/issues/detail?id=#10))
  * ve stavovém řádku se u hlášek vypisuje čas
  * konfigurační soubory jsou nyní ukládány dle [doporučení](http://www.freedesktop.org/wiki/Specifications/basedir-spec) [freedesktop.org](http://www.freedesktop.org), tzn. standardně do `~/.config`. Windows se freedesktop specifikacemi neřídí, takže tam se to ukládá do `%APPDATA%`. Při aktualizaci ze staré verze je nutno využít export a import kontaktů. ([issue #30](https://code.google.com/p/esmska/issues/detail?id=#30))
  * přidány globální zkratky pro vybrané položky v hlavní nabídce
  * konečně přidána dlouho slibovaná možnost zobrazit si historii odeslaných zpráv
  * tlačítko pro pozastavení fronty je nyní "zamačkávací"
  * v seznamu kontaktů se nyní dá pohybovat šipkami. Po Enteru nebo dvojkliku se kurzor přesouvá do okna zprávy.
  * ve stavovém řádku se nyní zobrazují ikony ([issue #32](https://code.google.com/p/esmska/issues/detail?id=#32))
  * v rámci snad blížící se internacionalizace přejmenovány konfigurační soubory na anglické názvy. Při aktualizaci ze staré verze je nutno využít export a import kontaktů.

### 0.5.1 ###
  * _vydáno 15. listopadu 2007_
  * možnost zadávat argumenty příkazové řádky i .bat nebo .sh souboru
  * aktualizován skript pro Vodafone kvůli změně jejich stránek ([issue #28](https://code.google.com/p/esmska/issues/detail?id=#28))

### 0.5.0 ###
  * _vydáno 12. listopadu 2007_
  * přidána možnost zadávat argumenty příkazové řádky
  * přidána možnost specifikovat umístění konfiguračních souborů přes volbu příkazové řádky ([issue #13](https://code.google.com/p/esmska/issues/detail?id=#13))
  * přidána možnost přepnout se do "portable" módu přes volbu příkazové řádky - využitelné při spouštění z externího (flash) disku ([issue #13](https://code.google.com/p/esmska/issues/detail?id=#13))
  * aktualizace vzhledů Substance na verzi 4.1
  * Substance "Sahara" jako výchozí vzhled
  * kontakty a fronta sms jsou místo xml ukládány jako csv soubory
  * opraveno vyhlazování fontů pod vzhledy Substance ([issue #17](https://code.google.com/p/esmska/issues/detail?id=#17))
  * přidána kontextová nabídka pro práci se schránkou do všech textových polí - jen při použití vzhledů Substance
  * aktualizovány ikony
  * úprava skriptu pro posílání na O2, kvůli jejich úpravě stránek ([issue #26](https://code.google.com/p/esmska/issues/detail?id=#26))

### 0.4.0 ###
  * _vydáno 25. srpna 2007_
  * k projektu přidána ikonka programu (png i svg), pro vytváření spouštěčů
    * zjistil jsem, že jisté prehistorické systémy (aka Windows) neumí k zástupci přiřadit dokonce ani png ikonu, natož svg; upřímnou soustrast...
  * přechod na licenci GNU GPL 3
  * české řazení v seznamu kontaktů
  * podpora dlouhých zpráv na O2, které se před odesláním správně rozdělí
  * přidána možnost importu kontaktů z programu Kubík SMS DreamCom ([issue #3](https://code.google.com/p/esmska/issues/detail?id=#3))
  * přidána možnost importu kontaktů z programu DreamCom SE ([issue #3](https://code.google.com/p/esmska/issues/detail?id=#3))
  * přidána možnost exportu/importu kontaktů do/z CSV formátu ([issue #14](https://code.google.com/p/esmska/issues/detail?id=#14))
  * přidána možnost měnit Look&Feel
  * přidán JGoodies Look&Feel
  * přidán Substance Look&Feel
  * přidán splash screen

### 0.3.0 ###
  * _vydáno 27. července 2007_
  * změna pořadí sms ve frontě
  * přidání ikon operátorů
  * přehlednější fronta (text sms v místní nápovědě)
  * možnost používat neomezené zpět a vpřed (undo a redo) v textu zprávy
  * vylepšené používání a správa adresáře
  * kontrola správnosti údajů při tvorbě kontaktu
  * klávesové zkratky
  * změna vzhledu uživatelského rozhraní
  * posuvníky mezi jednotlivými částmi formuláře
  * pamatování velikosti a rozvržení formuláře
  * hromadné odesílání zpráv

### 0.2.0 ###
  * _vydáno 22. července 2007_
  * změna vzhledu uživatelského rozhraní
  * přidán adresář kontaktů
  * pamatování posledních nastavení (položky formuláře, fronta sms)
  * přidán konfigurační dialog

### 0.1.0 ###
  * _vydáno 12. července 2007_
  * úvodní vydání
