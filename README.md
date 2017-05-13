1. Clone wallet sources
```

git clone https://github.com/grumpbyguy/NicNacCoinwallet.git
```

2. Set symbolic link to coin sources at the same level as src. For example:

ln -s ../NicNacCoin NicNacGui
Alternative way is to create git submodule:

git clone https://github.com/grumpbyguy/NicNacCoinwallet.git NicNacGui

git submodule add https://github.com/grumpbyguy/NicNacCoin.git NicNacCoinsGUIw
```

3. Build

mkdir build
cd build
cmake -G "Visual Studio 12 Win64" ..

And then do Build.
