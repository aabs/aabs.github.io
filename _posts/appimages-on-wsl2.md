Title: AppImages on WSL2
Date: 2020-03-04 13:31
Author: aabs
Category: Semantic Web
Slug: appimages-on-wsl2
Status: published
Attachments: 2020/03/fish-logo.png

This is a reminder to self, for those times when you just gotta have `vim` and `fishdots` on a recent version of `fish` shell (and someone upstream has completely screwed up the CA certificates so you can't use `apt` or linux`brew` because they can't be configured to relax cacert security).

First, create a place for them to live

``` {.wp-block-syntaxhighlighter-code}
mkdir -p ~/bin; cd /tmp
```

Now get fish shell

``` {.wp-block-syntaxhighlighter-code}
wget --no-check-certificate https://download.opensuse.org/repositories/shells:/fish:/nightly:/master/AppImage/fish-latest-x86_64.AppImage
chmod a+x fish-latest-x86_64.AppImage
./fish-latest-x86_64.AppImage --appimage-extract
mv ./squashfs-root/ ~/bin/fish_root
abbr -a fish ~/bin/fish_root/AppRun
```

Then download neovim

``` {.wp-block-syntaxhighlighter-code}
wget --no-check-certificate 
https://github.com/neovim/neovim/releases/download/v0.4.3/nvim.appimage
chmod u+x nvim.appimage
./nvim.appimage --appimage-extract
mv ./squashfs-root/ ~/bin/nvim_root
abbr -a nvim ~/bin/nvim_root/AppRun
```

Lovely. Now you have the one true shell and the one true editor. All's well with the world.
