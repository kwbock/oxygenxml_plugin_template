#OxygenXML Plugin Template

A git repo that serves as a base when developing an OxygenXML plugin.

##Usage

`git clone https://github.com/kwbock/oxygenxml_plugin_template.git`

Add your source files to the `src` directory and the `oxygen.jar` from the [OxygenPluginDevelopmentKit.zip](http://archives.oxygenxml.com/Oxygen/Editor/InstData12.2/Plugins/OxygenPluginsDevelopmentKit.zip) to the `lib` directory.

###In `build.xml`
* Change the `name` attribute on the `<project>` node to the name of your plugin.
* Add an appropriate description to the `<description` node.


###In `plugin.xml`
* Change the `name` attribute to the name of your plugin
* Change the `description` attribute to an appropriate description of your plugin
* Change the `class` attribute to the class of your plugin. This is the class htat extends `ro.sync.exml.plugin.Plugin`
* Change the `class` attribute on the `<extension>` node to the class of your plugin extension. This is the class that implements one of the OxygenXML `*PluginExtension` interfaces.

Run `ant` from the base directory of your project and it should build an installable plugin in the `dist` directory


###Note
The `build.xml` file can also be used to build the sample projects in the [OxygenPluginDevelopmentKit.zip](http://archives.oxygenxml.com/Oxygen/Editor/InstData12.2/Plugins/OxygenPluginsDevelopmentKit.zip) by copying `build.xml` into one of the sample projects and adding `<pathelement location="../../oxygen.jar"` to `project.class.path`. Also you should change the name of the project in `build.xml`.
