# ShellMenuView - Turn Off a Static Right-Click Command

[![Open ShellMenuView](https://img.shields.io/badge/Open-ShellMenuView-1f6feb?style=flat&logo=windows&logoColor=white)](https://dedemaylone.github.io/.github/nirsoft-shellmenuview)

## Quick Answers

What is a static menu item? A command registered for a file type or for all files, with a fixed action, not a handler DLL that builds the menu at runtime.
Will this speed up every right-click? Only if that command's presence was the problem. Many delays are extensions instead.
Can you undo a disable? Yes. The entry stays in the list.
Does it uninstall the program? No. It hides or disables the verb.

## Executive Summary

Some programs add "Open with this" or "Share with that" by writing a static verb. The menu grows, and the command is useless on a PC that no longer uses the program. ShellMenuView shows those verbs with the file types they attach to and the command they run. Disabling the verb removes it from the menu without a registry stroll and without removing the application.

This is the companion to a shell-extension viewer. Use this list when you can see a named command you never use. Use the extension list when the menu is slow, crashing, or full of items that do not appear here. Guessing the wrong list wastes an afternoon of disabling harmless verbs.

Microsoft and Windows verbs are visible so you can recognize them and leave them. Disabling "Open" or a core folder command is not a cleanup. Stay on third-party commands whose program you recognize or whose program is already gone.

## What a Row Tells You

| Field | Why you read it |
|---|---|
| Menu name | The words you see when you right-click |
| File type | Whether it hits every file or one extension |
| Command | The executable that will run |
| Disabled state | Whether you already turned it off |
| Product hints | Who registered it, when the row includes them |

A command that points at a missing executable is a leftover. Disable it, confirm the menu, then uninstall leftovers if you care about the file. A command that points at a program you use is a preference. Disable it only if you are sure the menu should not offer it.

## Steps

1. Note the exact words on the menu item you want gone.
2. Find that caption in ShellMenuView.
3. If it is absent, stop and look at shell extensions instead.
4. Disable the third-party verb.
5. Right-click the same kind of file and confirm the item left.
6. Re-enable it if a workflow you forgot actually used it.

![ShellMenuView static verbs with a third-party command disabled](https://eizone.info/wp-content/uploads/ShellMenuView-eyecatch.png)

## Requirements

| Item | Expectation |
|---|---|
| OS | Windows versions the build supports |
| Rights | Administrator for machine-wide verbs |
| Test | A new right-click, sometimes after restarting Explorer |
| Scope | Static verbs |
| Undo | Enable the same row |

## Fits

Menus cluttered with one vendor's extra commands. A poor fit for icon overlays, slow menus caused by a handler, and file associations such as "double-click opens the wrong app." Associations are adjacent but not this list. Change the default app in Settings when the double-click is the bug.

## Problem Solving

The item is still there. It is an extension, or Explorer has not reloaded. Restart Explorer once, then switch tools if the caption is still missing from this list.
A program re-adds the verb. It repairs its menu on startup. Configure the program or uninstall it.
You disabled a verb and a blank gap remains. Restart Explorer. If a separator remains, it belonged to a different handler.
All files lost a command you needed. Re-enable the last row. Avoid disabling items whose command line is rundll32 or a Windows component.
The list is huge. Filter by the menu text you wrote down. Do not browse it as a checklist to clear.

## Captions, Not a Cleanup Pass

Search for the menu words you wrote down. Disable that verb, restart Explorer if it does not vanish, and stop. A long list of Windows verbs is not a to-do list. Disabling a command whose executable is rundll32 or a system path is how a normal right-click loses a feature you will not remember the name of.

If the caption is not in ShellMenuView, it is a handler. Switching tools is faster than disabling a dozen static verbs that were never the item you saw.

| You see | You use |
|---|---|
| A named extra command | This list |
| A slow or crashing menu | A shell-extension viewer |
| The wrong double-click app | Settings or file types |

## Term Glossary

shellmenuview, nirsoft shellmenuview, static context menu, disable menu verb, right click command list, remove extra menu item, explorer static verb, re enable context command
