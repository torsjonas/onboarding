# onboarding
List of the most used apps &amp; tools @ Woorank

## IDE

- [SublimeText 3](http://www.sublimetext.com)

OR

- [Atom](https://atom.io/)

### SublimeText Packages

- Aligment
- BracketHightlighter
- DashDoc
- DocBlockr
- Emmet
- Git
- GitGutter
- INI
- LESS
- **Package Control**
- Pretty JSON
- Sass
- SideBarEnhancements
- SublimeLinter
- SublimeLinter-contrib-semistandard (needs to `npm i -g semistandard`)
- SublimeLinter-json
- SublimeLinter-php

### SublimeText User Settings

```json
{
	"auto_indent": true,
	"auto_match_enabled": true,
	"ensure_newline_at_eof_on_save": true,
	"indent_subsequent_lines": true,
	"indent_to_bracket": true,
	"rulers":
	[
		80,
		120
	],
	"tab_size": 2,
	"translate_tabs_to_spaces": true,
	"trim_automatic_white_space": true,
	"trim_trailing_white_space_on_save": true
}
```

## Db clients

- pgCommander (AppStore)
- [SequelPro](http://www.sequelpro.com/)
- [Redis Desktop Manager](http://redisdesktop.com/)
- [Robomongo](http://robomongo.org/)

## Terminal & shell

- [Homebrew](http://brew.sh/)
- [iTerm2](https://www.iterm2.com/)
- [fish](http://fishshell.com/)

### Fish config (~/.config/fish/config.fish)

````
# Aliases
alias clr='clear'                         # Clear your terminal screen
alias dmac='docker-machine'               # docker-machine
alias dcp='docker-compose'                # Docker-Compose
alias flush='killall -HUP mDNSResponder'  # Flush DNS (Yosemite)
alias ip='curl icanhazip.com'             # Your public IP address
alias ll='ls -al'                         # List all files in current directory in long list format
alias ldir='ls -al | grep ^d'             # List all directories in current directory in long list format
alias ut='uptime'                         # Computer uptime

# Sublime Text command
function subl
    /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl $argv
end


# docker-machine setup
eval (docker-machine env dev)

# Rebuild docker image
function dcpRebuild
  docker-compose stop $argv; and docker-compose rm -v $argv; and docker-compose build $argv;
end

# Clean docker containers
alias dckContClean='docker rm -v (docker ps -a -q)'

# Clean docker images
alias dckImgClean='docker rmi -f (docker images | grep "<none>" | awk "{print \$3}")'

# Node Env
set -x NODE_ENV development
```

## Virtualization

- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Docker-toolbox](https://www.docker.com/docker-toolbox)

## Password & Security

- [1Password](https://agilebits.com/onepassword)
- Meldium (Chrome extension)
- CryptoCat (AppStore)
- Authy (PlayStore + Chrome extension)

## Utility apps

- Alfred (AppStore)
- Flycut (AppStore)
- [Dash](https://kapeli.com/dash)
- [Divvy](http://mizage.com/divvy)
- [Dropbox](https://www.dropbox.com/)
- Paw (AppStore)
- Slack (AppStore)

