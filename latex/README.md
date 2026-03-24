Building tex -> pdf

### tex engine

#### Install tex engine

Options:

1. [miktex](https://www.tug.org/texlive/windows.html)

Miktex does not include every tex package under the sun unless you ask it to, by default it downloads them on the fly with a package manager (after asking you). Its installer is reasonable.

- next download the miktex installer: https://miktex.org/download
- run the miktex installer, which defaults to `%appdata%\MiKTeX` (config) and `%localappdata%\Programs\MiKTeX` (program)
- note that the installer should update your $PATH on windows, if it doesn't, the runtime is at `%localappdata%\Programs\MiKTeX\miktex\bin\x64\`

update packages
- open "miktex console" from start menu. If it says it's already running, check your system tray applications and it will be there (right click -> restore to get it to pop up)
- go to updates tab, update now

2. [texlive](https://www.tug.org/texlive/windows.html)

The texlive installer is painfully slow (expect tens of minutes or more) since it downloads every tex package under the sun by default and there are _thousands_ (it even does this sequentially!) and they are mostly hosted on slow university servers.

- download installer `install-tl-windows.exe`
- run installer, which defaults to `C:/texlive/<year>`

3. (untested) or [tinytex](https://yihui.org/tinytex)

Tinytex is like texlive but it only contains a subset of the 4000+ packages downloaded by texlive.

#### Set up

+ add to your PATH

### texstudio

!!! LIGHT MODE ONLY ALERT !!!

Install
- install some tex engine (see above)
- download from https://texstudio.org/

build pdf instructions:
- open in texstudio
- build

### vscode extension

Install
- install some tex engine (see above)
- install vscode
- install some perl runtime (eg, [strawberry perl](https://strawberryperl.com/) on windows) for compatibility with the vscode extension
- install the [latex workshop extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) in vscode
- add your tex executable to your $PATH (note you may need to restart vscode to reload your $PATH)
- follow any additional steps: https://github.com/James-Yu/LaTeX-Workshop/wiki/Install

- open this folder in vscode (all files must be visible in the "explorer" tab)
- open the tex file
- open the tex extension sidebar (will appear after opening the tex file)
- make some minor change to the tex file and hit save, which should trigger it to download the packages you need
- note you may need to open the miktex console here and run updates if you're using miktex
- reopen the tex file, make some minor change to text, rebuild

If you run into problems, ref https://github.com/James-Yu/LaTeX-Workshop/wiki/Compile
