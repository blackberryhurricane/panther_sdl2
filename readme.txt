Panther_SDL2 is a fork of SDL2 (version 2.0.3) which is compatibile with Mac OS X 10.3.9 
and Mac OS X 10.4.

Panther_SDL2 takes Thomas Bernard's excellent Mac OS X 10.4 SDK Tiger patches to the next level, 
making it work at the MACOSX_DEPLOYMENT_TARGET of version 10.3, which enables Mac OS X 10.3.9 
compatibility (10.3.8 and below will not work with this method). Xcode 2.5 has been tested.

== 

If you are building for a Panther target:

export MACOSX_DEPLOYMENT_TARGET=10.3
./configure --exec-prefix=$app --prefix=$app --disable-x --disable-joystick --disable-haptic
make
sudo make install

(X11 probably works but was not test)

If you are building for Tiger:
export MACOSX_DEPLOYMENT_TARGET=10.4
./configure --exec-prefix=$app --prefix=$app --disable-joystick --disable-haptic
make
sudo make install

==

Thomas BERNARD Tiger Patch:
https://gist.github.com/miniupnp/26d6e967570e5729a757

Found from this post:
https://forums.libsdl.org/viewtopic.php?p=41191