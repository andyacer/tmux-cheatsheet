# Credit

I copied this from an existing Gist because I liked the format.  That author also referenced the others below.
* [Original gist by agarie](https://gist.github.com/agarie/b65728102f5a3a577243)
* [A tmux crash course](https://robots.thoughtbot.com/a-tmux-crash-course)
* [tmux cheatsheet from @henrik](https://gist.github.com/henrik/1967800)

I use "Oh My Tmux", my configs are also in this repo
* [Oh My Tmux!](https://github.com/gpakosz/.tmux)


## Introspection

| Command | Shortcut | Description |
|---------|----------|-------------|
|`:list-commands`||List all available tmux commands|
|`:list-keys`||show list of all currently assigned keys|
|`:display-panes`|prefix + q|show pane numbers|
|`tmux list-sessions`|prefix + i|lists existing tmux sessions|

## Session Management

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux list-sessions`|prefix + i|lists existing tmux sessions|
|`tmux new -s session_name`||creates a new tmux session named session_name|
|`tmux rename-session`|prefix + $|rename the current session|
|`tmux attach -t session_name`||attaches to an existing tmux session named session_name|
|`tmux detach`|prefix + d|detach the currently attached session|


## Windows

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux next-window`|prefix + n|go to the next window|
|`tmux previous-window`|prefix + p|go to the previous window|
|`tmux new-window`|prefix + c|create a new window|
|`tmux select-window -t :0-9`|prefix + 0-9|move to the window based on index|
|`tmux rename-window`|prefix + ,|rename the current window|
|`tmux find-window`|prefix + f|find window from matching text (e.g. the window name)|
|`tmux last-window`|prefix + tab|jump to the last used window|
|`tmux kill-window`|prefix + &|kill the current window|


## Panes

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux split-window`|prefix + " or \| or ' |splits the window into two vertical panes|
|`tmux split-window -h`|(prefix + % or -|splits the window into two horizontal panes|
|`tmux swap-pane -[UDLR]`|prefix + { or } \| < or > |swaps pane with another in the specified direction|
|`tmux select-pane -[UDLR]`|prefix + arrow-key|selects the next pane in the specified direction|
|`tmux select-pane -t :.+`|prefix + o|selects the next pane in numerical order|
|`tmux display-panes`|prefix + q|show pane numbers|
|`tmux display-panes`|prefix + q [0-9]|select pane by number - you gotta be quick though =)|
|`tmux kill-pane`|prefix + x|kill current pane|
|`tmux break-pane`|prefix + !|breakout the pane into its own new window|
|`tmux join-pane`|prefix + s|send pane TO window number|
|`tmux join-pane`|prefix + j|join pane FROM window number|

## Copy mode

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux copy-mode`|prefix + [|enter copy mode|
|`tmux paste-buffer`|prefix + ]|paste the contents of the paste buffer in the current pane|

## Useful commands

* `tmux list-keys` lists out every bound key and the tmux command it runs


