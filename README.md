# Bjazz

This is a small bwrap script for a very specific use-case. In case that's your use-case, here you go, otherwise you probably shouldn't use this. This shouldn't cause any damage if things go wrong, but is not really tested outside of my own setup.

This script provides two main functionalities, username/home changing, and top-level directories.

The username is changed through mounting /etc/group and /etc/passwd. A custom /home directory gets mounted, so all of the files in the sandbox user's home will be available outside in ~/.bjazz/$USER/ (Where $USER is the user in the sandbox)

The ability to create new top level directories is done by simply mounting all of the host's top level directories seperately. This allows for adding new top level directories, such as /nix.

# Usage
Clone the repo and run the "enter" script with a username.

Nix can be installed by doing mkdir /nix inside of the sandbox, then proceeding with the single-user Nix install script.