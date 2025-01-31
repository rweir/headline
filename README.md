# Headline ZSH Theme
<img src="https://raw.githubusercontent.com/moarram/headline/assets/images/slice.png" width="600"/>

Headline. A stylish theme with deliberate use of space. No dependencies. Easily customizable.

<br>


## Contents
* [Features](#features)
* [Installation](#installation)
* [Customization](#customization)
* [Terminal Setup](#terminal-setup)
* [Screenshots](#screenshots)
* [Credits](#credits)

<br>


## Features
### Separator Line
A line above the prompt info text with matching colors. May be disabled with `HEADLINE_LINE_MODE=off` for a more compact prompt.

### Information Line
`<user> @ <host>: <path> | <branch> [<status>]`

This line is responsive, meaning it won't overflow when it gets too long. Individually style each segment of the information line using [ANSI SGR codes](https://en.wikipedia.org/wiki/ANSI_escape_code#SGR_(Select_Graphic_Rendition)_parameters) (which are conveniently aliased in the theme file). You can customize the characters for joining segments and disable segments entirely.

### Git Status
All the Git status symbols are customizable. The defaults are below:

| Symbol | Meaning          |
|--------|------------------|
| `+`    | staged changes   |
| `!`    | unstaged changes |
| `?`    | untracked files  |
| `↓`    | commits behind   |
| `↑`    | commits ahead    |
| `↕`    | commits diverged |
| `*`    | stashed files    |
| `✘`    | conflicts        |
| (none) | clean branch     |

<br>


## Installation
Download the `headline.zsh-theme` file.
```
wget https://raw.githubusercontent.com/moarram/headline/main/headline.zsh-theme
```

In your `~/.zshrc`, source the `headline.zsh-theme` file.
```
source your/path/to/headline.zsh-theme
```

More details on the wiki page: [Installation](https://github.com/Moarram/headline/wiki/Installation)

<br>


## Customization
The `headline.zsh-theme` file describes variables ([around line 70](https://github.com/Moarram/headline/blob/main/headline.zsh-theme#L70)) for customizing prompt behavior, colors, styles, symbols, etc. Set these variables in your `~/.zshrc` *after* sourcing the theme to override the defaults. Play around with it and make it your own!

More details on the wiki page: [Customization](https://github.com/Moarram/headline/wiki/Customization)

<br>


## Terminal Setup
For the continuous line above the prompt, use a font with ligatures such as [Fira Code](https://github.com/tonsky/FiraCode).

If you want symbols, use a font that has them such as [FiraCode Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode) and assign your desired symbols to the prefix variables.

More details on the wiki page: [Terminal Setup](https://github.com/Moarram/headline/wiki/Terminal-Setup)



<br>


## Screenshots
Screenshots of theme in [iTerm2](https://iterm2.com/index.html). Using [FiraCode Nerd Font](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode) for continuous line and fancy icons.

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/zsh_theme_light.png" width="600"/>
> 
> Status showing `+` for staged changes, `!` for unstaged changes, and `?` for untracked files (configurable).

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/zsh_theme_brown.png" width="600"/>
> 
> Optional icons, special font needed.

> <img src="https://raw.githubusercontent.com/moarram/headline/assets/images/zsh_theme_dark.png" width="600"/>
> 
> Path truncated to fit in available space, user and host hidden.

<br>


## Credits
* Headline's Git status functions borrow code from `git.zsh` in [Oh-My-Zsh's core library](https://github.com/ohmyzsh/ohmyzsh/blob/master/lib).
* Thanks to u/romkatv (author of [Powerlevel10k](https://github.com/romkatv/powerlevel10k)) for the [Reddit post](https://old.reddit.com/r/zsh/comments/cgbm24/multiline_prompt_the_missing_ingredient/) describing how to calculate prompt string display length.
