# Basic Idea

The intended use is that a `what.toml` with all of the file and dir metadata (for now just strings describing the contents) will be placed in the root dir of the project. Then, when `what` is called on a file it will look in the current directory for a `what.toml`, then keep going up until it (either runs out of files to looks at, or hits `home\`?). If it finds a `what.toml` it will check to see if it has the relevant information inside. If it does, it will give the user the relevant information. 

## MVP Features

`what` a single file or dir. `what` everything in the current dir. Generate .md doc of everything in the current dir.

# More Features

## what --recursive (-r)

This could be called so that one could get information about a dir, every file and dir in that dir, all dirs in those dirs... etc.

## what global

A .toml that is hit after the initial search fails, can contain info about files in `\` like `dev`, `lib32` etc.