# git is-it-in #

Find whether a commit has been merged into a branch.

Usage: `git is-it-in ref1 ref2`

This will tell you whether ref1 is an ancestor of ref2 or vice versa.        

Examples:

    $ git is-it-in 963102 HEAD
    963102 is an ancestor of HEAD

    $ git is-it-in 963102   # If no second argument, we assume HEAD
    963102 is an ancestor of HEAD

    $ git is-it-in 8f8e49997e HEAD
    8f8e49997e is NOT an ancestor of HEAD
    HEAD is NOT an ancestor of 8f8e49997e

    $ git is-it-in 8f8e49997e 963102
    963102 is an ancestor of 8f8e49997e
           



# How to install #

Just download the `git-is-it-in` file from this repo and put it someplace on your path, like `~/bin/`

# Tips #

For quick access, add the following snippet to your `~/.gitconfig` file:

    [alias]
        i = is-it-in
        
Now you can use `git i` instead of `git is-it-in`.