# Installation and Updating
Vizitest is currently available for Java only. 

Currently, it requires IntelliJ Community or Ultimate, Version 2022.3 or later. We will soon be removing the Intellij dependency so Vizitest can run with any IDE.

## Register and Install
1. [Register your Vizitest Trial](https://vizitest.com/trial-signup-form). Please do this first.
2. Install the [IntelliJ plugin from the Marketplace](https://plugins.jetbrains.com/plugin/22716-vizitest).

## Plugin Startup
Once the plugin has been installed, each time you start IntelliJ, the plugin will automatically start. You will see some notifications as Vizitest starts in the background.

<img src="intellij-startup.png" alt="connecting groups" width="300"/>

The first time the plugin starts...

- it downloads a Java version that is compatible with Vizitest. This will not conflict with your main Java version. It can take a while to download and install, so please be patient.
- It then downloads the latest version of the Vizitest service.
- And finally, it starts the Vizitest service.

Starting IntelliJ subsequently will...

- check whether the minor and patch version is up to date. If not, an update will be automatically downloaded and installed. 
- Major versions need to be explicitly installed from the Test Manager Settings. Not yet available.


## Updating Vizitest
Vizitest is conventionally versioned using major.minor.patch (1.4.6).

When IntelliJ starts, Vizitest checks for updates and automatically installs minor and patch updates for you.

Major version updates are installed upon request from the Test Manager's Settings dialog.


