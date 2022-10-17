# How to Use

## Starting up a Plugin

Set the plugin you want to activate as the boot target, and press the mode button to activate it. For details, please refer to the [camera._setPlugin](../theta-web-api-v2.1/commands/camera._set_plugin.md) in the Web API.

### Declaration of Permissions

When installing from the RICOH THETA store, based on the protection level set in the manifest file, permission is automatically granted. During development, use an application that displays the screen such as Vysor, and grant permission from the application settings or from a plugin dialog window.

### Using WebUI

The plugin can launch a web server and provide a WebUI or its own API. By using port 8888 on the web server that the plugin starts up, it becomes possible to open a home page provided by the plugin web server from a basic app on a smartphone.

The client can find out the presence or absence of the web server by using the Web API's [camera._listPlugins](../theta-web-api-v2.1/commands/camera._list_plugins.md). The information from camera._listPlugins consists of information described in the configuration file (\assets\settings.json) of each plugin. If the setting file does not exist or the setting value is incorrect, the default value is written in the camera._listPlugins information.

The information that can be described in the settings file is as follows:

* Whether the plugin provides WebUI (default value: none)

Sample configuration file:			

~~~
{
 "webServer": true
}
~~~

## Finishing a Plugin

Push and hold the Mode Button for 2 seconds to finish. When the plugin detects that the Mode Button has been pressed for 2 seconds, it must quit. When the plugin finishes, a [notification of termination for the plugin](./broadcast-intent.md#notifying-completion-of-plugin) must be made.
