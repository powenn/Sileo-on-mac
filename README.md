# Sileo on Mac

### Update:For some reason, I can't provide any file,check out them on discord server 

I will show you how I install sileo on mac ,I just gather and unify these information in [Hayden's sever](https://discord.com/invite/qgqhUJsP) ,you can get more advanced tutorial on the sever .

![Screenshot of Sileo on Mac][1]
![Screenshot of Sileo on Mac][2]

## Things you need
- [Homebrew](https://brew.sh/)(optional)
- [gnu-tar from homebrew](https://formulae.brew.sh/formula/gnu-tar)(optional)
- [Sileo for Mac deb file ](https://github.com/powenn/Sileo-on-mac-/tree/main/sileo%20deb%20files) (if you using M1 mac choose arm version,intel choose amd)
- [procursus ](https://github.com/powenn/Sileo-on-mac-/tree/main/package)(support for big sur,catlina,mojave )

## Getting  Start

Now telling you the basic to install sileo on mac

### Optional

If you want to use `homebrew` and `gnu-tar` just keep going ,if not just skip to first step 

install `homebrew`
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
then install `gnu-tar`
```
brew install gnu-tar
```
### First step

First,you need install procursus on your mac 

There are two way to install,depending on have you install `homebrew` and `gnu-tar` from homebrew  

#### The way without `homebrew`

replace <strap> with the path to the bootstrap you downloaded and run the command: 
```
zstd -d <strap>.zst && sudo tar --preserve-permissions -xkf <strap> -C /
```
#### if you have `gnu-tar` from `homebrew` 

you can shorten the command 
```
sudo gtar --preserve-permissions -xkf <strap>.tar.zst -C /
```
then add  `/opt/procursus/bin` to the start of your PATH in your shell config file
```
nano ~/.zprofile
```
put `PATH="/opt/procursus/bin:$PATH"` on the top 
```
PATH="/opt/procursus/bin:$PATH"
```
Then you can install sileo through 
```
sudo dpkg -i <path to Sileo deb>
```
you will see sileo in your app folder

before you open it 
```
sudo apt update
sudo apt upgrade
```
then you can experience it

btw this is my repo [powen00hsiao repo](https://powenn.github.io/powen00hsiao/)

[1]: https://github.com/powenn/Sileo-on-mac-/blob/main/screenshot/01.png
[2]: https://github.com/powenn/Sileo-on-mac-/blob/main/screenshot/02.png
