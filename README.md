# empc
Single window, single playlist, no thrills, bare-bones mpc client for emacs taylored to _my_ use case. 

# Keybindings
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
