-- layout: blog
-- title: How to set browser to I2P
-- filename: blog/posts/how-to-set-browser-to-i2p.html
-- Author: Bartek Jasicki
From [the official site](https://geti2p.net/en/):

> I2P is an anonymous network built on top of the internet. It allows users
> to create and access content and build online communities on a network
> that is both distributed and dynamic. It is intended to protect
> communication and resist monitoring by third parties such as ISPs.

Official guide how to configure web browser you can find in the project
[documentation](https://geti2p.net/en/about/browser-config). Here I want to
present the alternative ways for this.

### Desktop

On the most of the desktop browsers, configuration depends on plugin
[SwitchyOmega](https://github.com/FelisCatus/SwitchyOmega). It is available for
Firefox, Firefox based browser and for Chrome and Chromium based browsers.

1. Install SwitchyOmega in your browser. On the project page you can find links
   to both stores.
2. When the plugin will be installed, enter its options by clicking its icon
   and select **Options** entry from the menu. A new browser tab will open with
   the plugin options.
3. From the menu on the left, under *Profiles* select entry *proxy*.
4. The form for entering the proxy server will appear. If you have installed
   I2P on this same computer and you have the default configuration for the
   proxy, enter `127.0.0.1` in *Server* field and `4444` in *Port* field. It
   may look [that](images/guide/proxy.png)
5. Click on button *Apply changes* to save your setting.
6. From the menu on the left, under *Profiles* select entry *auto switch*.
7. Remove any existing rules and create a new: for *Condition Type* select
   option `Host wildcard`. For the field *Condition Details* enter `*.i2p`. For
   the *Profile* field select option `proxy`. Your setting now should look
   [that](images/guide/autoswitch.png).
8. Again click on button *Apply changes* to save your setting. And close the
   plugin preferences.
9. Again, click on the plugin's icon and from the menu select option **auto
   switch**.
10. Try to enter any eepsite :) Now every time when you try to reach any I2P
   address, the plugin will switch to I2P proxy. When you will browse clearnet,
   you will be using the direct connection.

### Android

It is recommended to use [F-Droid](https://f-droid.org/) repository for
download and update all needed applications. This guide is a lot shorter than
the desktop version, but depends on specific web browser.

1. Download application [I2P](https://f-droid.org/packages/net.i2p.android.router/),
   install, configure and start I2P router. It may take some time (around 4-5
   minutes) before HTTP tunnel will be available. In this time you can do
   second thing.
2. Download application [Privacy Browser](https://f-droid.org/packages/com.stoutner.privacybrowser.standard/),
   install it and configure as you prefer. *Note:* in Google Store free version
   of this browser contains advertisements. Version from the F-Droid doesn't
   have them.
3. When your HTTP tunnel in I2P router will be ready, just select option
   **I2P** from the *Proxy* menu in the menu on the right side of the program.
   If you want to disable proxy, from this same menu select option **None**.

If you want to use I2P proxy from the other machine (for example, from your
server), select option **Custom** from the *Proxy* menu and in the program
settings (the left menu of the program, entry *Settings*) enter the address
and port for your I2P proxy. For example: `http://192.168.0.12:4444`.
