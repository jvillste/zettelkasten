When ever there is a content creation tool, usually the content can be shared either in the source form or as the end result. A Photoshop file is the source and a JPG file is the end result. Programs are developed as text files and the end result is an executable file encoded in the machine code.

The challenge is how to be able to commercialise source format content but still be able to share the source of projects that use such content. This would be useful for example in a [[market place based on a game engine]].
# Goals
- to be able to share content in the source format so that others can modify it and mix with other content
- to be able to sell content that can be used to make other content. An example would be software libraries and game engine assets.
- to be able to sell content creation tools and tool plugins. For example DAW:s and DAW plugins.
- to be able to use source files with the future versions of the authoring tool
- to be able to use the same source files in multiple different authoring tools
# Approaches
Software libraries can be shared in the compiled machine code format so that they can be used to build other software but the source code is not made available to the library users.

DAW plugins can be shared as machine code like software libraries. Those are tools that will not be part of the resulting audio file unlike software libraries that are compiled into the resulting executable program. But if the source file of the DAW project would be shared, the plugins must be shared also, which hinders the ability to sell plugins commercially and to share DAW project files at the same time.

Standard source formats can be developed, but the features of such formats restrict the features that content creation tools can have.
# Examples
## Programming languages
A programming language is a source format, but code editors a.k.a. "integrated development environments" (IDE:s) have their own file format for storing the settings for their features that are not expressed in the programming language that is being edited.

## Quake maps
Quake maps have a simple plaintext format and there are many map editors that use it. The editors can have diverse set of editing tools but the project is always stored in the original map file format and stays interchangeable between the different editors. This restricts the editors so that the geometry can only be expressed as so called "BSB brushes" and not higher abstraction level parameterised entities such as stairs that can have the stair count as a parameter. Stairs can be generated with a tool bot after the generation there are only BSB brushes and the parameters of the generation can not be changed. If the editors would use their own file format, the stair entity could be kept in a source format so that the parameters could be changed later on.

## Music tracker module files
I the nineties there was a [music tracker](https://en.wikipedia.org/wiki/Music_tracker) scene in which music was shared in the source form as "[module files](https://en.wikipedia.org/wiki/Module_file)". Those files contained all of the notes and samples that could then be remixed by other people to create their own music. Nowadays commercial digital audio workstations a.k.a "DAW":s have replaced music trackers and music is created using commercial software synthesizers and audio effects called "plugins" which can not be shared. Plugins need to be installed on the users machine separately to be able to open a project file that uses them. They are not stored in the project files. 

## DAW plugins
Digital audio workstation (DAW) plugins adhere to a standard API such as VST or AU. That allows different DAW:s to utilise the same plugins. The standard specifies how the plugin draws on the screen and gets user input and how it generates and processes audio. If the plugins would be shared in the project source files, the project files could be shared between users more easily.