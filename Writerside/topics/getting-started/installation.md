# Installation and Updating

<warning>
<p>
Vizitest is currently available for Java only.
</p>
<p>
Currently, it requires IntelliJ Community or Ultimate, Version 2022.3 or later. We will soon be removing the Intellij dependency so Vizitest can run with any IDE.
</p>
</warning>

## Register and Install
1. First, you will need to [register for Vizitest](https://vizitest.com/trial-signup-form).
2. Next, [install the IntelliJ plugin from the Marketplace](https://plugins.jetbrains.com/plugin/22716-vizitest). 

You can also [download and install the plugin here](https://mrm.automated-software-testing.com/releases/com/ast/vizitest/plugins/intellij/Vizitest-0.1.2.zip). Then install it from Setting -> Plugins

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
Vizitest is conventionally versioned using the standard ```major.minor.patch``` system.

When IntelliJ starts, Vizitest checks for updates and automatically installs minor and patch updates for you.

Major version updates are installed upon request from the Test Manager's Settings dialog.


