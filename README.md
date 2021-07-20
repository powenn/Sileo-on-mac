# Sileo on Mac

I will show you how I install sileo on mac ,I just gather and unify these information in [Hayden's sever](https://discord.com/invite/qgqhUJsP) ,you can get more advanced tutorial on the sever .

## Things you need
- [Homebrew](https://brew.sh/)(optional)
- [Sileo for Mac deb file ](    ) (if you using M1 mac choose arm version,intel choose amd)
- [procursus ](      )(support for big sur,catlina,mojave )

## Getting  Start

Now telling you the basic to install sileo on mac
First,you need install procursus on your mac 
There are two way to install,depending on have you install homebrew and `gnu-tar` from homebrew  

The way without homebrew
replace <strap> with the path to the bootstrap you downloaded and run the command: 
```
zstd -d <strap>.zst && sudo tar --preserve-permissions -xkf <strap> -C /
```
if you have 'gnu-tar' from homebrew you can shorten the command to
```
sudo gtar --preserve-permissions -xkf <strap>.tar.zst -C /
```
then add  '/opt/procursus/bin' to the start of your PATH in your shell config file
```
nano ~/.zprofile
```
put `PATH="/opt/procursus/bin:$PATH"` on the top 
```
`PATH="/opt/procursus/bin:$PATH"`
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

