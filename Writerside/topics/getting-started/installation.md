# Installation
Vizitest is currently available under Java only. 

In the near term it requires IntelliJ Community or Ultimate, Version 2022.3 or later. We will soon be removing the need for Intellij and Vizitest will then run with any IDE.

- You will first need to [register with Vizitest](nutshell.md) so we can create your account. [TODO : trial page link]
- Install the [IntelliJ](https://plugins.jetbrains.com/plugin/22716-vizitest) plugin.

## Plugin Startup
Once the plugin has been installed, each time you start IntelliJ, the plugin will automatically start. You will see some notification messages as Vizitest starts in the background.

The first time the plugin starts...

- it downloads a Java version that is compatible with Vizitest. This will not conflict with your main Java version. It can take a while to download and install, so please be patient.
- It then downloads the latest version of the Vizitest service.
- And finally, it starts the Vizitest service.

Starting IntelliJ subsequently will...

- check whether the minor and patch version is up to date. If not, an update will be automatically downloaded and installed. 
- Major versions can be [installed upon request](updating.md) from the Test Manager.

## Starting Vizitest
There are two ways to start Vizitest once the Vizitest service is installed and started.

- From the main IntelliJ menu (Select "{} Open in Browser" to start the [Vizitest Test Manager](test-manager-intro.md).)
- From the **Open in Browser** link in Notification.

![](intellij-startup.png)

## Learning Vizitest
You are now ready to use Vizitest. This documentation covers key reference topics such as

- [The Test Manager](test-manager-intro.md) for organizing test.
- [The Test Editor](test-editor.md) for configuring tests.
- [Training](training.md) - a set of tutorial modules accompanied by sample code.

