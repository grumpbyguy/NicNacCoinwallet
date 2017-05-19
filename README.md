**1. Clone wallet sources**

```
git clone https://github.com/grumpbyguy/NicNacCoinwallet.git
```


**2. Set symbolic link to coin sources at the same level as `src`. For example:**

```
ln -s ../NicNacCoin NicNacGui
```

Alternative way is to create git submodule:

```
git submodule add https://github.com/grumpbyguy/NicNacCoin.git cryptonote
```

**3. Build**

```
mkdir build
cd build
cmake -G "Visual Studio 12 Win64" ..

```
**And then do Build.**

```
In 'build' folder solution for Visual Studio will be created
Open in with Visual Studio and make build there
