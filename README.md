# tmux-launch
Just a small bash script to launch tmux with a defined layout

Call it like

    tmux-launcher path-to-layout-file
    
You first of course should do a 

    chmod u+x tmux-launcher
    
### Where to put
I have a bin folder in my home dir. And that's the location, I put the tmux-launch file. The layout files are there too, but this should become a matter of change.

### The layout file
These files should have the expression "layout" in their names. But that's up to you. The script searches for files with "layout" in its own dir to make suggestions, if nothing is being found.

The layout file is line based, values are seperated by a tab char. Every line consists of:

0. name - Just a marker for human issues. Like a description.
0. id - Index to be referenced later.
0. parent id - The pane to select and split. References `id`.
0. percent - Amount of size to steal from parent pane.
0. direction - Split the parent pane horizontal or vertical.
0. directory - The directory to change to .
0. command - The initial command for this pane.
