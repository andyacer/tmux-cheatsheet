# Credit

I copied this from an existing Gist because I liked the format.  That author also referenced the others below.
* [Original gist by agarie](https://gist.github.com/agarie/b65728102f5a3a577243)
* [A tmux crash course](https://robots.thoughtbot.com/a-tmux-crash-course)
* [tmux cheatsheet from @henrik](https://gist.github.com/henrik/1967800)


## Session Management

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux new -s session_name`||creates a new tmux session named session_name|
|`tmux rename-session`|prefix + $|rename the current session|
|`tmux attach -t session_name`||attaches to an existing tmux session named session_name|
|`tmux switch -t session_name`||switches to an existing session named session_name|
|`tmux list-sessions`|prefix + s|lists existing tmux sessions|
|`tmux detach`|prefix + d|detach the currently attached session|

## Windows

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux new-window`|prefix + c|create a new window|
|`tmux select-window -t :0-9`|prefix + 0-9|move to the window based on index|
|`tmux rename-window`|prefix + ,|rename the current window|
|`tmux find-window`|prefix + f|find window from matching text (e.g. the window name)|
|`tmux kill-window`|prefix + &|kill the current window|

## Panes

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux split-window`|prefix + "|splits the window into two vertical panes|
|`tmux split-window -h`|(prefix + %|splits the window into two horizontal panes|
|`tmux swap-pane -[UDLR]`|prefix + { or }|swaps pane with another in the specified direction|
|`tmux select-pane -[UDLR]`||selects the next pane in the specified direction|
|`tmux select-pane -t :.+`||selects the next pane in numerical order|
||prefix + q|show pane numbers|
|`tmux kill-pane`|prefix + x|kill current pane|
|`tmux copy-mode`|prefix + [|enter copy mode|
|`tmux paste-buffer`|prefix + ]|paste the contents of the paste buffer in the current pane|

## Useful commands

* `tmux list-keys` lists out every bound key and the tmux command it runs
* `tmux list-commands` lists out every tmux command and its arguments
* `tmux info` lists out every session, window, pane, its PID, etc
* `tmux source-file ~/.tmux.conf` reloads the configuration file

