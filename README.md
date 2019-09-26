# dsort

dsort is bash script that automatically organizes your downloads
directory or any other directory, based on simple rules supplied
in it's configurations file. For more information about where this
file should be located and how to write it, as well as dsort's
available options, see the manpage.

## Install

Running the below command will install both executable and manpage
under /usr/local/bin and /usr/local/share/man/man1/:
- sudo make install

If you wish to install under a different prefix, provided you have
the required rights, provide it as an argument, like so:
- make PREFIX="path/to/my/dir" install

## Uninstall

In complete parallel to install, run:
- sudo make uninstall
or, if you installed under a different prefix
- make PREFIX="path/to/my/dir" uninstall

## Example

If for example you have some PNG files ending with the .png extension
in $HOME/Downloads/, then putting the following in $HOME/.config/dsort.conf:

```
*.png
Pictures/
```
and running dsort from your terminal will move all files ending with
.png in $HOME/Downloads/ to $HOME/Pictures/:
