---
title: 'VSCode: Manual'
date: 2019-04-06 14:09:58
tags:
---

## Visual Studio Code on macOS
### Launching from the command line

You can also run VS Code from the terminal by typing 'code' after adding it to the path:

- Launch VS Code.
- Open the **Command Palette** (`kb(workbench.action.showCommands)`) and type 'shell command' to find the **Shell Command: Install 'code' command in PATH** command.

![macOS shell commands](/blog/images/shell-command.png)

- Restart the terminal for the new `$PATH` value to take effect. You'll be able to type 'code .' in any folder to start editing files in that folder.

>**Note:** If you still have the old `code` alias in your `.bash_profile` (or equivalent) from an early VS Code version, remove it and replace it by executing the **Shell Command: Install 'code' command in PATH** command.

To manually add VS Code to your path, you can run the following commands:

```bash
cat << EOF >> ~/.bash_profile
# Add Visual Studio Code (code)
export PATH="\$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
EOF
```

Start a new terminal to pick up your `.bash_profile` changes.

**Note**: The leading slash `\` is required to prevent `$PATH` from expanding during the concatenation. Remove the leading slash if you want to run the export command directly in a terminal.

## Workbench

### Easier Display Language configuration ([March 2019 version 1.33](https://code.visualstudio.com/updates/v1_33))

Running the `Configure Display Language` command will now open a Quick Pick listing the available locales based on the Language Packs you have installed, instead of only opening the locale.json file. When you make a selection, the locale will be automatically updated and you'll be prompted to restart VS Code for the change to take effect.

![](/blog/images/display-language-picker.png)


## 其他

### Configuration Shell

MacOS
修改集成终端
```json
{
    "terminal.integrated.shell.osx": "/bin/zsh"
}