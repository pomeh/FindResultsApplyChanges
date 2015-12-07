**[Sublime Text 3+](http://www.sublimetext.com/) Package**. Install via an updated version of  [Package Control 2+](https://sublime.wbond.net/installation). Just **DON'T** install manually.

# Find Results Apply Changes

## Description

Apply any change you made to a "Find Results" buffer back to the files. ie:
- Search for "foo" in a folder.
- This will open a "Find Results" buffer listing all the files with "foo" in it.
- Change the instances of "foo" for "bar" or something else...
- Go to the -> Main menubar -> "Find" -> "Find Results - Apply Changes" or just press CTRL/CMD+S
- This will write all the changes made back to the files.
- Will be enabled only if the focused view is the "Find Results" tab.

## Bugs

- Uses regions to allow you do multiline changes, but when inserting new newlines, if you already applied some change, will corrupt files **if you commit more than once**, this because the new newlines will shift the line numbers. Will also 'corrupt' files if you add/remove newlines in other instances of the modified files. eg in another tab. To prevent corruption this packages will alert you and prevent most of these.
- "double-click = open file" in Find Results doesn't work with this package. This is an intented behavior. To restore the double-click behavior, you need to add `"disable_double_click": false` config line into your preferences file (to open this file, use Command Palette and search for "Preferences: Settings - User" item).

## WONTFIX

- Will write/read UTF8 files. If you have a file in another encoding, considering jumping to the U8 world. :)
- It converts line ending of files to Unix style

## Source-code

https://github.com/titoBouzout/FindResultsApplyChanges

## Forum Thread

http://www.sublimetext.com/forum/viewtopic.php?f=6&t=14118
