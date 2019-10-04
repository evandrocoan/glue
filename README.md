No longer under active development.
===================================

Glue
====

[Glue](https://github.com/chrissimpkins/glue) is a cross-platform, [extensible](http://gluedocs.readthedocs.org/en/latest/extend-glue.html) plug-in for [Sublime Text 2 and 3](http://www.sublimetext.com/) that connects your favorite editor to your shell.

Detailed documentation is available on [http://gluedocs.readthedocs.org](http://gluedocs.readthedocs.org).

## Confirm Your PATH

Before you get started, please confirm your system PATH string in the Glue settings. [Here are the instructions](http://gluedocs.readthedocs.org/en/latest/install.html#confirm-your-path).


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Now,
   Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   find the following setting on your **`Package Control.sublime-settings`** file:
   ```js
       "channels":
       [
           "https://packagecontrol.io/channel_v3.json",
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
       ],
   ```
1. And,
   change it to the following, i.e.,
   put the **`https://raw.githubusercontent...`** line as first:
   ```js
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
   ```
   * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
     you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`Glue`** and press <kbd>Enter</kbd>

See also:
1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


## Launch

#### Open with Right Click Menu

![Right Click Menu](http://gluedocs.readthedocs.org/en/latest/_images/popup-open-glue.png "Open Glue with the Right Click Menu")

#### Open with the Command Palette

![Command Palette](http://gluedocs.readthedocs.org/en/latest/_images/command-palette-open.png "Open Glue with Command Palette")

#### Open with Keybinding

```
Ctrl - Alt - G
```

## Enter Commands

Use the command input box at the bottom of the screen to enter system commands just like you would in your terminal:

![Enter Commands in Glue](http://gluedocs.readthedocs.org/en/latest/_images/command-entry-example.png "Command Entry with Glue")

and the standard output is displayed in an editor view.

## System Utilities

It works with system utilities:

#### grep

![Grep Example](http://gluedocs.readthedocs.org/en/latest/_images/grep-example.png "Grep Example")

#### cURL

![cURL Example](http://gluedocs.readthedocs.org/en/latest/_images/curl-example.png "cURL Example")

## Scripting Languages

It works with scripting languages:

![Scripting Languages Examples](http://gluedocs.readthedocs.org/en/latest/_images/scripting-language-example.png "Scripting Languages Examples")

## Inter-Process Communication

Pipelining data between processes works.  You get the standard output from the final executable in the sequence:

![Pipelining Example](http://gluedocs.readthedocs.org/en/latest/_images/pipelining-examples.png "Pipelining Example")

## Version Control

Version control tasks are accessible inside the editor:

![Version Control Example](http://gluedocs.readthedocs.org/en/latest/_images/git-example.png "Version Control Example")

## Compile, Unit Test, Profile, Minify, Compress...

You get the picture.

## Navigation & Working Directory State

Glue includes its own version of the `cd` command that allows you to navigate around your directory structure while maintaining your current working directory state between calls to the shell.

## File Management

Open files in the Sublime Text editor by file path:

```
█ glue open <filepath> [filepath2] [...]
```

or by wildcard pattern:

```
█ glue wco <wildcard>
```

and create new files with:

```
█ glue new
```

## Available Glue Commands

Glue includes its own set of commands to perform common tasks.  You can extend these with aliases (see [information below](https://github.com/chrissimpkins/glue#extend-sublime-text-with-glue-extensions)).

Usage examples with available command arguments are in [the documentation](http://gluedocs.readthedocs.org/en/latest/commands.html).

<table>
	<tr><th>Command</th><th>Description</th></tr>
	<tr>
		<td>cd</td><td>change directory</td>
	</tr>
	<tr>
		<td>exit</td>
		<td>exit the Glue terminal</td>
	</tr>
	<tr>
		<td>glue browse</td>
		<td>open URL or local project file in default browser</td>
	</tr>
	<tr>
		<td>glue clear</td>
		<td>clear text in the Glue view</td>
	</tr>
	<tr>
		<td>glue finder</td>
		<td>reveal current directory (default) or optional path in finder</td>
	</tr>
	<tr>
		<td>glue goto</td>
		<td>Sublime Text GoTo Anything search</td>
	</tr>
	<tr>
		<td>glue help</td>
		<td>view help documentation in Glue view</td>
	</tr>
	<tr>
		<td>glue localhost</td>
		<td>open default web browser to local server</td>
	</tr>
	<tr>
		<td>glue new</td>
		<td>open a new Sublime Text buffer</td>
	</tr>
	<tr>
		<td>glue open</td>
		<td>open one or more project files by filepath</td>
	</tr>
	<tr>
		<td>glue path</td>
		<td>display the system PATH setting that is used by Glue</td>
	</tr>
	<tr>
		<td>glue user</td>
		<td>display alphabetized list of your Glue user extensions</td>
	</tr>
	<tr>
		<td>glue wco</td>
		<td>open one or more files by wildcard pattern</td>
	</tr>
</table>

## Extend Sublime Text With Glue Extensions

You can build Sublime Text extensions **with your favorite language** or extend Sublime Text **with any system utility** using Glue command extensions.  These are aliases for system commands that can be called from the Glue command line using the syntax:

```
█ glue <your-command> [optional arguments]
```

You have the option to pass additional command line arguments, clipboard data, or the current working directory path to the mapped system command with [template tags](http://gluedocs.readthedocs.org/en/latest/extend-glue.html#define-your-command-extensions).

### The Glue-Commands Directory

Create a directory in your Sublime Text `Packages` directory (`Preferences > Browse Packages`) that is named `Glue-Commands`.

### The glue.json File

Create a new file in this directory with the following path `Glue-Commands/glue.json`.

Use the `glue.json` file to create Glue extensions with `key = command name` to `value = command string` mapping.

### Example

You could make a command that executes a local image compression shell script on the path `/Users/me/scripts/cruncher.sh` with the following syntax:

``` json

{
  "crunch": "/Users/me/scripts/cruncher.sh {{args}}"
}
```

Then use it in Glue like this:

```
█ glue crunch image.png
```

The mapped system command is executed as:

```
/Users/me/scripts/cruncher.sh image.png
```

in your current working directory and is accessible in any Sublime Text project.

Make as many as you'd like.  You can use the following command to reference an alphabetized list of your extensions:

```
█ glue user
```

More detailed extension documentation (including additional examples) is [available here](http://gluedocs.readthedocs.org/en/latest/extend-glue.html).

## Changelog

The changelog is available [here](https://github.com/chrissimpkins/glue/releases).

## License

[MIT License](https://github.com/chrissimpkins/glue/blob/master/LICENSE)



