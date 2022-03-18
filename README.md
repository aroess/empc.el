# empc.el
Empc is a single window, single playlist, no thrills, bare-bones mpd client for EMACS. It requires [mpd and mpc](https://musicpd.org/) to be installed.

![image](https://github.com/aroess/empc/blob/main/screenshot.png?raw=true)

## Installation
Save `empc.el` somewhere in your `.emacs.d` folder and put this in your init.el:

```elisp
(load-file "~/.emacs.d/path_to/empc.el")`
```

Or add it to your [load path](https://www.emacswiki.org/emacs/LoadPath).

## Configuration
To change the [default keybindings](https://github.com/aroess/empc.el/blob/234a630e743f3d62c58ee67dd3dc2a105f5d91b2/empc.el#L105) simply redefine the empc-mode-map keys in your `init.el`:
``` elisp
(define-key empc-mode-map "0" (empc-generic-command "volume +5" nil nil))
(define-key empc-mode-map "9" (empc-generic-command "volume -5" nil nil))
```

There is not much else to configure. I personally don't use any fancy EMACS packages for candidate selection so I like to set the wildcard character `*` as initial input for the search/jump-box.

```elisp
(setq empc-search-initial-input "*")
```

## Keybindings
| Key | command | 
| --- | --- |
| RET | `mpc play` (song under cursor) |
| p | `mpc toggle` |
| j | jump to song
| n | `mpc next` | 
| b | `mpc prev` | 
| c | `mpc seek +5` |
| x | `mpc seek -5` |
| r | `mpc random` |     
| R | `mpc repeat` |      
| s | `mpc single` |
| + | `mpc volume +5` |
| - | `mpc volume -5` |
| . | `mpc status` |
| f | follow = move cursor to current song |
| g | revert playlist buffer |
| U | `mpc clear && mpc update --wait  && mpc add /` |
| q | quit window |
