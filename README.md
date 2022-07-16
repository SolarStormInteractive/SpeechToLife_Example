# Speech-To-Life plugin Example project

This is the example project for the speech-To-Life plugin which will be released on the Unreal Marketplace sometime soon.

See the [documentation wiki](https://github.com/SolarStormInteractive/SpeechToLife_Docs/wiki) for full information and documentation about the plugin itself. More specifically, the page documenting this example project [here](https://github.com/SolarStormInteractive/SpeechToLife_Docs/wiki/Example-Project-Details).

To target Oculus Quest VR, see [this wiki pages](https://github.com/SolarStormInteractive/SpeechToLife_Docs/wiki/Android-Details) section on Oculus Quest configuration. By default, this example project targets android default (untouched configuration) because targeting Oculus Quest breaks supporting basic android devices.

# The Branches
This project contains two other branches other than main:
* 'ue_4.27' - Use this for Unreal Engine 4.27. This branch looks like main.
* 'ue_5.0' - Use this for Unreal Engine 5.0

There are some important configuration differences between the two branches but that is about it. They are not mergable unfortunately because of how different configuration between the two engines is.

The 'main' branch contains the base line where I do development. I then clobber the 4.27 and 5.0 branches with new changes and replace the configuration.
