# Credit

I copied this from an existing Gist because I liked the format.  That author also referenced the others below.
* [Original gist by agarie](https://gist.github.com/agarie/b65728102f5a3a577243)
* [A tmux crash course](https://robots.thoughtbot.com/a-tmux-crash-course)
* [tmux cheatsheet from @henrik](https://gist.github.com/henrik/1967800)

I use "Oh My Tmux", the key bindings below use it as a baseline:
* [Oh My Tmux!](https://github.com/gpakosz/.tmux)

Some of these shortcuts reference aliases in my .zshrc file.

## Introspection / General

| Command | Shortcut | Description |
|---------|----------|-------------|
|`:list-commands`||List all available tmux commands|
|`:list-keys`|`keys` alias in shell|show list of all currently assigned keys|
|`:display-panes`|prefix + q|Show pane numbers|
|`tmux list-sessions`|prefix + i|Lists existing tmux sessions|
|`sublime ~/.tmux.conf.local`|prefix + e|Open up tmux config in an editor|
|`source-file ~/.tmux.conf`|prefix + r|Reload tmux configuration|
|`xclip selection c`|`echo "test" \| clip`|Pipe output of command to clipboard using xclip|
|`sublime ~/.zshrc`|`profile` alias in shell|Open up ZSH config profile in Sublime editor|

## Session Management

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux list-sessions`|prefix + i|lists existing tmux sessions|
|`tmux new -s session_name`||creates a new tmux session named session_name|
|`tmux rename-session`|prefix + $|rename the current session|
|`tmux attach -t session_name`||attaches to an existing tmux session named session_name|
|`tmux detach`|prefix + d|detach the currently attached session|
|`resurrect save`|prefix + Ctrl-s|Save the entire session, windows, panes, etc. to disk|
|`resurrect restore`|prefix + Ctrl-r|Restore session from disk. Not sure how to select among saves|


## Windows

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux next-window`|prefix + n|go to the next window|
|`tmux previous-window`|prefix + p|go to the previous window|
|`tmux new-window`|prefix + c|create a new window|
|`tmux swap-window`|Ctrl + shift + LR|Change window ordering Left / Right|
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
|`yank line`|prefix + y|Uses yank plugin to copy command line to the clipboard|
|`yank pwd`|prefix + Y|Uses yank plugin to PWD to clipboard|
|`tmux respawn-pane -k`|`repane` alias in shell|Reload a new shell in the current pane. To get new aliases loaded and stuff.|

## Copy mode

| Command | Shortcut | Description |
|---------|----------|-------------|
|`tmux copy-mode`|prefix + [|Enter copy mode|
|`tmux choose-buffer`|prefix + =]|Choose a buffer to paste from|
|`tmux list-buffers`|prefix + '+'|Faster viewing buffer list|
|`copy-pipe `|y|yank the selected text to a buffer and clipboard|
|`copy-pipe-and-cancel `|Y|copied text pasted to command prompt & buffer - NO clipboard|
|`copy-line`|Triple-Click (Mouse)|Select full line|
||/|Search from the start of the entire pane buffer.|
||?|Search backward|
||g|Go to top line|
||G|Go to last line|
||PgUp|Page Up|
||PgDown|Page Down|
||q|Quit copy-mode|
|`tmux save-buffer buf.txt`||Save buffer contents to buf.txt|
|`tmux capture-pane`||Don't do this, use the logging plugin instead (see below)|


## Logging (Plugin-based)

| Command | Shortcut | Description |
|---------|----------|-------------|
||prefix + shift + p|Start/stop logging of the current pane|
||prefix + alt + p|Screen capture the current pane (ONLY visible)|
||prefix + alt + shfit + p|Capture ENTIRE pane's history to file|




## Helpful links

* https://tmuxcheatsheet.com/
* https://github.com/tmux-plugins/
* https://github.com/gpakosz/.tmux
* https://github.com/tmux/tmux/wiki
* https://gist.github.com/Bekbolatov/6840069e51382965fdad
* https://hashcat.net/wiki/doku.php?id=example_hashes

## Helpful man page screenshots

<img src="https://github.com/andyacer/tmux-cheatsheet/raw/main/choose-buffer.png">


<!-- 

Comments / testing stuff here:


## Non-tmux shortcuts

| Command | Shortcut | Description |
|---------|----------|-------------|
|`xclip selection c`|`echo "test" \| clip`|Pipe output of command to clipboard using xclip|
|`sublime ~/.zshrc`|`profile`|Open up ZSH config profile in Sublime editor|



 -->