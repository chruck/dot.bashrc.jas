This is just my `.bashrc` .  I name it `.bashrc.jas` so it doesn't
immediately clobber whatever `.bashrc` is on whatever new system I am
on.  I usually rename an existing `.bashrc` to `.bashrc.orig`, then create
a symlink for `.bashrc` to this file.

Sourcing this file loads all environment variables in this file and
creates the files it creates.

This file increments the `${JAS_ROX}` variable in itself by:

        $ ./.bashrc.jas incr

...then `${JAS_ROX}` will be changed to today's date.  I use this to let
me know what version of this file is currently on the current system.

A list of files that `.bashrc.jas` creates:

        $ grep '^## ' .bashrc.jas |sort
        ## /root/bin/build32
        ## /root/bin/build32on64
        ## /root/bin/mntmountall
        ## ~/.Xresources (for rxvt{,-unicode}):
        ## ~/.bash_profile
        ## ~/.gdbinit
        ## ~/.gitconfig
        ## ~/.gitignore
        ## ~/.inputrc
        ## ~/.irssi/config
        ## ~/.screenrc
        ## ~/.ssh/config
        ## ~/.vim/systags
        ## ~/.vim/templates/src.c
        ## ~/.vim/templates/src.h
        ## ~/.vim/templates/src.sh
        ## ~/.vimrc.jas
        ## ~/bin/gfilt
        ## ~/bin/git_diff_wrapper
        ## ~/bin/gvim.sh
        ## ~/bin/gvimdiff.sh
        ## ~/bin/jasindent
        ## ~/bin/jasonize
        ## ~/bin/lesspipe.sh
        ## ~/bin/myscreensessionname
        ## ~/bin/snapshots.btrfs
