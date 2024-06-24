### installation
- for key repeatin
> To enable key-repeating, execute the following in your Terminal, log out and back in, and then restart VS Code:
```
$ defaults write com.microsoft.VSCode ApplePressAndHoldEnabled -bool false              # For VS Code
$ defaults write com.microsoft.VSCodeInsiders ApplePressAndHoldEnabled -bool false      # For VS Code Insider
$ defaults write com.vscodium ApplePressAndHoldEnabled -bool false                      # For VS Codium
$ defaults write com.microsoft.VSCodeExploration ApplePressAndHoldEnabled -bool false   # For VS Codium Exploration users
$ defaults delete -g ApplePressAndHoldEnabled                                           # If necessary, reset global default
```
- bind caps as esc
  >setxkbmap -option caps:escape
### commands 
#### navigation
h / l - left / right
k / j - up / down
#### inserting
i / a - before/after cursor
I - at the start of the line
A - at the end of the line

#### making changes in command mode
x - delete char
r - replace char

#### copy/paste
yy - copy line
Yp - copy and insert next line

### Question zone?
u - delete char // dd -delete line
:set number - show line number

+p - past from system clipboard

