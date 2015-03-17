

# Introduction #

Esmska features a **pluggable gateway system**, which allows to create support for new gateways as simple script files and add them to the program without the need of any program modification. With this plugin system, users can create their own gateway plugins, and if it works well, they can send it to us so we can integrate it into official release.

If you have some basic IT knowledge and you can create plugin for some local country or even international gateway, you are very welcome.

# Creating your own script #

The gateway script is relatively simple to write. There are some rules, which you must abide, but they are quite easy to understand. The rest of the work lies in determining which data you must send to the gateway website in order to have the message accepted.

## Recommended tools ##
  * Tool for easy visualization of HTML forms, such as [Web Developer](https://addons.mozilla.org/firefox/addon/60) extension to [Firefox](http://www.mozilla-europe.org/products/firefox/) browser. It allows you to graphically introspect HTML forms, enable/disable cookies, set HTTP Referer, disable javascript and lots of other stuff. This helps you to find out, which features and necessary to send the message.
  * Network packet sniffer and analyzer, such as [Wireshark](http://www.wireshark.org/), [HttpFox](https://addons.mozilla.org/en-US/firefox/addon/6647) or [TamperData](https://addons.mozilla.org/en-US/firefox/addon/966). By observing legitimate request and responses packets when sending messages with your browser, you can easily find out, where is the problem when using your gateway script.
  * [cURL](http://curl.haxx.se/), which is a very powerful command-line tool for sending various HTTP requests. If you have problems with sending messages through your gateway scripts, you should first of all try to send it with cURL. Because it is specializes tool just for this, it can help you solve many of your problems by comparing was web browser send, what cURL sends and what your script sends. All modern Linux distributions should have cURL in their packaging system.
  * If you still use Windows, you will also need some reasonable text editor capable of saving text file in standardized UTF-8 encoding with LF line-endings, which is the required format for the gateway files.

## Gateway script specifics ##

The gateway script file must be located in the `gateways` directory inside the program installation folder. The filename of the script must contain only ASCII characters (space excluded) and be as similar to the true gateway name (see below the format description) as possible. It must end with the `.gateway` suffix, e.g. `[XX]Foo.gateway`.

The script file must be encoded in the **UTF-8 encoding** with standard **LF newlines** (standard UNIX format).

It is recommended that you also supply and icon for your gateway, which should be a 16x16 px PNG image with (preferably) transparent background. The filename of the image must be the same as the gateway file, but ending with `.png`, e.g. `[XX]Foo.png`. The image file must also be in the `gateways` directory. Supplying of the image file is not mandatory though, just recommended.

_Have a look into the `gateways` folder for some examples._

## Internal format description ##

The whole file is just a simple **JavaScript file**. Therefore you can use there everything which is possible to use in [JavaScript](http://en.wikipedia.org/wiki/Javascript). The JavaScript support is based on the [Mozilla Rhino](http://www.mozilla.org/rhino/) project. If you don't know JavaScript, it's a very simple language, just google up some JavaScript reference and you can work with it almost instantly.

The script file must implement the [GatewayInfo](http://ripper.profitux.cz/esmska/javadoc/esmska/data/GatewayInfo.html) interface, which serves as an list of necessary information about the gateway. Content of all the methods are described in their documentation. Additionally, the script must implement the **send()** method, which is used to actually send the message (see below).

In the script you can use some variables, which are predefined and contain some important information. You can find list of these variables in the [GatewayVariable](http://ripper.profitux.cz/esmska/javadoc/esmska/transfer/GatewayVariable.html) enumeration. Be sure not to overwrite this variables with some your temporary ones! And don't forget that JavaScript (as most languages) is case sensitive.

There is also one special variable called **EXEC**. With this variable, you can invoke the public methods listed in [GatewayExecutor](http://ripper.profitux.cz/esmska/javadoc/esmska/transfer/GatewayExecutor.html) documentation. All these methods are executed by the program itself and some of them return you some result (e.g. content of the requested web page). Again, behaviour and return values are described in the methods descriptions. On the **EXEC** variable there are also some constant strings, which you can use to inform the user about particular problem in a localized message.

_Have a look at some existing gateway files to see an examples of working plugins._

### The send() method ###

It's just up to you, how you will use the provided methods and send the message. It's only required that you always **end this method returning boolean**, whether the message was sent successfully or not. There are also some recommendations you should know about:
  1. First of all, check for variables correctness and modify them, if needed. For examples, you get the phone number in the international format, but your gateway wants it in country local format. Therefore, you have check the **number** and convert it to preferred format, if needed. As another example, if your gateway requires user to log in, you should check that variables for **login** and **password** are not empty and inform the user otherwise.
  1. Very probably you will have to download and parse some web pages for variables, image identifiers, etc. You can use classic string searches, but _regular expressions_ are far more powerful. You can use them for extracting parts of strings, so you can even forward some gateway error message directly to the user. If you don't know regular expressions, you should really learn it (even though it takes some time), search up for some [reference](http://www.regular-expressions.info/) and tutorials.
  1. You can stop executing the script at any time by calling the **return** keyword. But be sure to use the **EXEC** variable to set **success** to true or false and provide some **error message** in case of the latter. This way a user can find out why the sending failed and will not blame the program itself.
  1. You can use the **EXEC** variable to set **gateway message**, which will be shown to user after sending is finished. For example you can inform the user about number of free SMS remaining this way. Be careful where to set the message, your script can end prematurely.
  1. Be sure to test your script thoroughly and consider every possibility when looking for error messages. The recipient number can be non-existent/malformed, the same holds for the sender number or signature, the login or password can be incorrect, message text can be too long, and so on. Try all these settings and inform the user about each of this problems properly.
  1. Use the predefined error messages preferentially. They can be localized which means more users will be able to use your scripts. There may be many cases in which a foreigner may want to use your country-local gateway.

# Solving problems #

Please be aware of the fact that not all websites which you can use in your browser can also be used in Esmska. There are some extremely poorly-written websites, which this program simply can't handle. It includes only a basic HTTP library, which does not have all the powers and workarounds of full-featured web browser. Therefore websites complying with web standards should pose no problems, but some of the ugly websites may not work.

  * Very often you will search for some string in text content return from GET or POST method. If you are not sure that you really got what you should have got, print the web content to standard output, e.g. like this:
```
content = EXEC.getURL("http://somepage.com", [])
print(content)
```
> This way you can easily see what you actually got. Of course this means that you must run the program from the terminal/command line.

  * You don't have to restart Esmska when you do some change in the send() method. Just send a new SMS, program executes the send() method every time from scratch.

  * If you need more powerful tool to see your network activity, you can enable network logging. Just run the application with the `--debug network` option:
```
$ java -jar esmska.jar --debug network
```
> After running this command, you will see in the standard error output in your terminal lots of messages. During message sending you will see all HTTP headers of your requests and responses. If need also content of HTTP responses, you can get it with `--debug full`. But be warned, there will be hundreds of lines on the output.

# Having your script in the official release #

It's a complete nonsense to use your script only by yourself. All the users should benefit from your work, that's the reason we have a pluggable gateway system - so the users can contribute. If you want to share your work, just create a new issue in the [issue tracker](http://code.google.com/p/esmska/issues/list) and attach your gateway script (and the icon) to it. We will include it in the next official release and all the users will be able to benefit from your work.

The same procedure also applies when you have found some bugs or you have some improvements to currently available plugins. Just modify them and send them over, we will appreciate it.

Just a small legal notice: By sending us some of your work you agree to publish it under GPL-compatible free software license (meaning we can integrate it into our program).