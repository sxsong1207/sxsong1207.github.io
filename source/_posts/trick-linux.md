---
title: Linux Tricks
date: 2018-02-09 14:46:34
tags:
categories: Trick
---

# Disk empty? Clean it

Try this package: `ncdu`

---

# Term Emulator
## Tmux
.tmux.confg

    # remap prefix to Ctrl+a
    set -g prefix C-a
    unbind C-b
    bind C-a send-prefix
    # force a reload of config file
    unbind r
    bind r source-file ~/.tmux.conf \; display "Reloaded!"
    # quick pane cycling
    unbind ^A
    bind ^A select-pane -t :.+
    # copy-mode shortkey use vi mode
    setw -g mode-keys vi  

    # enable utf-8 support for status-bar
    set -g status-utf8 on

    # set foreground color scheme
    set -g pane-border-fg green  
    set -g pane-border-bg black  
    set -g pane-active-border-fg white 
    set -g pane-active-border-bg yellow  
    set -g message-fg white  
    set -g message-bg black  
    set -g message-attr bright  
    set -g status-fg white  
    set -g status-bg black  
    setw -g window-status-fg cyan  
    setw -g window-status-bg default  
    setw -g window-status-attr dim  
    setw -g window-status-current-fg white  
    setw -g window-status-current-bg red  
    setw -g window-status-current-attr bright  

    # set status bar format
    set -g status-left-length 40  
    set -g status-left "#[fg=green]Session: #S #[fg=yellow]#I #[fg=cyan]#P"  
    set -g status-right "#[fg=cyan]%d %b %R"  
    set -g status-interval 60  
    set -g status-justify centre  

    # set notification
    setw -g monitor-activity on  
    set -g visual-activity on
    
## Terminator

## Terminology
