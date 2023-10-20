# Uninstalling Vizitest
:::info 
Any tests you have created will continue to run after removing Vizitest. 
:::

To fully remove Vizitest from your machine, please follow these steps.

- Uninstall the Vizitest IntelliJ plugin.
- Remove the vizitest folder. The exact location is OS dependent [TODO : check windows and linux paths]
  - **/Users/username/.vizitest** on Mac
  - **/D:Users/username/.vizitest** on Windows
  - **/Users/username/.vizitest** on Linux
- To fully remove Vizitest Groups and Test Configurations from your codebase, remove the ```.vizitest``` folder from the root of your project.

