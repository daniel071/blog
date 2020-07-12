---
title: "Making your terminal  look like a ninja's 🚀 💻 🖱"
description: Coding is such a blissful activity.
date: 2020-04-19T11:00:00.000Z
next: coding-as-a-teen
previous: coming-soon
display: true
--- 

### Why should you use  terminal

As a programmer, a terminal is an essential tool for our every day's workflow as it helps us run commands that automates some GUI hurdles, making your terminal as useful and easy to use as possible is not only highly practical for any kind of work, but it also helps you like your work more.

### When do you need  terminal

You will surely need your terminal as a programmer for one reason or another, for example for version control or package control(npm, npm, yarn, cargo, etc...) and in many other fields that you can find here: 

In this short tutorial, we're gonna make your terminal go from this

to this

### Prerequisites

I assume that you are using a linux distribution, if not try out linux mint or install ubuntu on WSL, i also assume that you have access to an internet connection as you'll need to clone some github repositories.

### Let's Go |

First of all let's open the terminal, for classic linux users just search for the terminal in your installed programs, as for WSL users it's the program that opens when you click on the ubuntu icon in your programs

 <p class='tip'>  📓 📝 😎  tip: <br />  <br />Add the terminal  to the taskbar if it's not already there for ease of access  <p>

First let's install the required programs by typing:

```bash
sudo apt update
```



```bash
sudo apt install git zsh curl fonts-powerline
```

then hit enter.

 <p class='tip'>  📓 📝 😎 ​tip: <br />  <br /> zsh is an alternative shell to bash and git is a version control program  <p>


After the download finishes if you have been prompted to set zsh as your default shell, if not then type in your terminal 

```bash
chsh -s /usr/bin/zsh
```

Then enter your password

 <p class='tip'>  📓 📝 😎  tip: <br />  <br /> don't panic if you cannot see the output of your password, it does not display on the console  <p>


Let us then install oh-my-zsh, which we will need in order to level-up our zsh experience; 

just type:

```bash
sh -c "(curl -FsSl https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

you should have this output in your terminal:

![ohmyzsh output](install.png)

wow, now your terminal looks a bit better, but... it's not that good yet, let us use one of the best features of ohmyzsh: plugins, so let's install what is in my humble opinion the best plugin out there: powerlevel10k, powerlevel10k is a cool zsh theme.

### powerlevel10k

Let us install it  by typing:

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

After this operation, edit your ~/.zshrc with your favorite text editor and on the 11th line delete it and replace with:

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Then restart your shell by typing ` bash` then typing `zsh`

 <p class='tip'>  📓 📝 😎  tip: <br />  <br /> If you're too lazy to follow these steps, then just copy this file after typing q and paste it into ~/.p10k.zsh  <p>

you will then be prompted to enter some visual configurations like below:

![](choice1.png)

![](choice2.png)

![](choice3.png)

![](choice4.png)

![](choice4-5.png)

![](choice5.png)

![](choice6.png)



![](choice7.png)



![](choice8.png)

![](choice11.png)

![](choice12.png)

![](choice13.png)

Now the problem is that some icons are not displaying, to fix that let's install nerd-fonts by typing:

```bash
mkdir -p ~/.local/share/fonts
cd ~/.local/share/fonts && curl -fLo "Droid Sans Mono for Powerline Nerd Font Complete.otf" https://github.com/ryanoasis/nerd-fonts/raw/master/patched-fonts/DroidSansMono/complete/Droid%20Sans%20Mono%20Nerd%20Font%20Complete.otf
```
 <p class='tip'>  📓 📝 😎  tip: <br />  <br /> Don't install if everything is fine, if it's not working it just means that nerd-fonts is your default shell font <p>



![](choice14.png)



Copy one of these 2 files as your .p10k.zsh or read through the [The powerlevel10k manual](https://github.com/romkatv/powerlevel10k/blob/master/README.md) to find out how each of these components works, you should get this:

![1](term-cool-1.png)

and this: 

![2](term-cool-2.png)



or this:

![minimal](term-minimal-ex.png)

### Bonus: Syntax highlighting 🤠

Now let us install syntax highlighting so that we can see whether or not a command we are gonna enter is valid or not, for example here is the expected output:

![image-20200712162741893](image-20200712162741893.png)

to install, first type:

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```

then 

```bash
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
```

Then, enable syntax highlighting in the current interactive shell:

```bash
source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

Here's the output on my terminal:

![output](syntax-display.png)

### Bonus: Smart autosuggestion

Then, let us install a plugin for autosuggestion, so that you won't need to type whole commands as your terminal will automatically suggest you the command based on your recent commands and based on the available commands on your system.

Let's install it by typing:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Then in your ~/.zshrc search for the line where `plugins=(git)` and replace it with `plugins=(git zsh-autosuggestions)`

Then restart your shell by typing ` bash` then typing `zsh`

Let's test it out, start typing `ba` then, BANG!! you automatically get autosuggestions, to complete the command use the right key arrow

![completions](autosugg-ex.png)

This is it!!!! If you want to know more about customizing your terminal checkout:

[The powerlevel10k manual](https://github.com/romkatv/powerlevel10k/blob/master/README.md) : To know more about customizing your powerlevel10k theme

[The zsh-users github organization](https://github.com/zsh-users/) : for more awesome zsh plugins

[Oh my zsh repo](https://github.com/ohmyzsh/ohmyzsh) : to know more about oh my zsh




