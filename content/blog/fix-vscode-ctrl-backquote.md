+++
title = "Fixing Ctrl+` in VSCode"
date = 2023-06-25
taxonomies.tags = ["utilities"]
+++

Yesterday, I encountered this [issue][issu] while coding with Visual Studio Code. The default terminal shortcut `` Ctrl+` `` is not working on my new laptop. It seems some CJK Keyboards/IMEs reserve it for internal use. After some research, I figured out global hotkeys are not affected. So I wrote a [fixer][proj] to register it as a global hotkey and forward its keypress messages. Fortunately, it worked.

<!-- more -->

###### Update (March 29, 2024):

While it would be ideal to implement the fixer as a VSCode extension, I'm not familiar with front-end development. Currently, the fixer runs continuously in the background whenever the system is running, leading to some unnecessary troubles:

- The forwarded keypress messages are not perfect. Sometimes it causes unexpected behaviors in other programs.
- Users may play games, it would be catastrophic if some anti-cheat engines mistakenly classify the fixer as a cheating program.

To tackle these issues, the fixer implements a naive detection. It operates only if the title of the active window ends with `- Visual Studio Code` or `- VSCode`.

###### Update (April 29, 2024):

Recently, I struggled to learn the basics of VSCode extensions, and finally wrapped the fixer into an [extension][ext]. If you've encountered similar issues, consider giving it a try.

###### Update (May 1, 2024):

Today I just discovered that my IME has a configurable option: "Press `` Ctrl+` `` to switch to this IME". Disabling it resolved the issue, so my previous work has been pointless all along. What a dramatic turn of events...

[issu]: https://github.com/Microsoft/vscode/issues/63659
[proj]: https://github.com/lanlytt/vscode-cjk-toggle-terminal-fixer
[ext]: https://github.com/lanlytt/ctrl-oem3
