# Speech To Life plugin Example project

This is the example project for the Speech To Life plugin which will be released on the Unreal Marketplace sometime soon.

See the [documentation wiki](https://github.com/SolarStormInteractive/SpeechToLife_Docs/wiki) for full information and documentation about the plugin itself.

Pre-built demo versions of this project can be found here:
* [Windows 64bit](https://drive.google.com/file/d/1MHZvabS2nBEDL2ztkFuHlHPNWW_LfD6g/view?usp=sharing)
* [Android](https://drive.google.com/file/d/13LS9zfDIyamoAaAp50iQV_2QCHYG5CGX/view?usp=sharing)
* [Quest](https://drive.google.com/file/d/1GqRT9NQKZEEM1NSN3DjtEp2rA6Setzqx/view?usp=sharing)

## How to use / setup this project
* Choose the engine you want to target. Use the ue_5.0 branch for Unreal Engine 5, and ue_4.27 branch for Unreal Engine 4
* Pull this example project (branch you need) into a folder (grab a release package if you like and unzip into a folder)
* Download the ['en-us'](https://alphacephei.com/vosk/models/vosk-model-small-en-us-0.15.zip) and ['es'](https://alphacephei.com/vosk/models/vosk-model-small-es-0.22.zip) recognition models. Unzip them to Content\SpeechToLife\vosk so that there are two new folders called 'en-us' and 'es'. See the screenshot below for a visual example.
* Open the project with the engine you are using, the plugin is already active with this project.
* Run the level. If your microphone is ready you will be able to use voice commands. You can also package the example for windows and android. For Quest / Quest 2 see next section.

<img src="/Screenshots/ContentFolder.png">

## Quest / Quest 2
By default, this example project targets android default (untouched configuration) because targeting Oculus Quest as well breaks supporting basic android devices. If you want to support Oculus Quest however it is as easy as in the android project settings:
* Enable 'Support Vulkan'
* Under 'Package for Oculus Mobile devices' add 'Oculus Quest 1/2'

## Example design
In the example scene 'ExampleLevel' there is an in-level pawn called BP_SpeechToUnrealPawn in the world view. Click on it to open the details there is a property called "Speech Options". Here the different recognized lines are setup for each language. You should use the engines built in localization instead of this approach, but for the sake of simplicity and visibility I defined localization manually using a mapping. Each Speech Option entry contains a mapping of language to choices. Choices start at 0 and switch to 1 and so on as you are saying the choice line. The 'object' property is the UObject which implements the SpeechObjectInterface. The implementation is simple, a function called "DoSomething" with an input parameter of 'index', index being the index of the speech choice. This is merely an example of how to use speech recognition to make the world change and you can implement speech recognition how you see fit.

For a bare bones example see the level included called 'BareBonesExample'. In this levels Level Blueprint it sets up recognition for english and feeds the recognition result sentence to the Text Render component in the world.

## The Branches
This project contains two other branches other than main:
* 'ue_4.27' - Use this for Unreal Engine 4.27.
* 'ue_5.0' - Use this for Unreal Engine 5.0. This branch looks like main.

There are some important configuration differences between the two branches but that is about it. They are not mergable unfortunately because of how different configuration between the two engines is.

## Screenshots

Android:
<img src="/Screenshots/android_screenshot.jpg">
