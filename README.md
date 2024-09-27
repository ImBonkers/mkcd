# mkcd
I am tired of having to write mkdir and cd in two steps...

Add the contents of the main file into ~/.bashrc or whatever file is run at the start of every new terminal session

Example:

in ~/.bashrc add:
```
--- bashrc stuff ---

mkcd() {
    if [ ! -d "$1" ]; then
        mkdir -p "$1"
    fi
    cd "$1" || { echo "Failed to change to directory: $1"; return 1; }
}

--- more bashrc stuff ---
```
