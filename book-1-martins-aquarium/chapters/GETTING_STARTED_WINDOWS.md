# Installations

## Visual Studio Code

Visit the [Visual Studio Code](https://code.visualstudio.com/) website to download and install the code editor. This is the code editor you will be using for the next 3 months.

## Enable the Windows Subsystem for Linux

You'll need to install and enable the Windows Subsystem for Linux. You can follow the instructions below, or you can watch the [Enabling WSL in Powershell](https://youtu.be/Mzv6Pxppwoo) video to see how to enable the Linux subsystem.

1. Go to the `Start` menu (windows key) and search for `PowerShell`.
1. Run PowerShell as an Administrator. To do this, find the PowerShell application, then right-click on it and choose "Open as administrator".
1. Copy and paste this command into your PowerShell:

```sh
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. Restart your computer when prompted to.

## Ubuntu

Once you've completed the above steps **and** restarted your computer, you will [install Ubuntu from the Microsoft Store](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab).

This is needed ***before*** you install the Windows Terminal Preview below.

## Windows Terminal

Later in the instructions, we will ask you to type a command into your terminal. For Windows, this is the **Windows Terminal** application using **Ubuntu**.

Visit the [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) download page and open it in the Microsoft Store App. This will be your default terminal (using Ubuntu) which you will use to navigate your file system, and run development tools throughout the course.

Once Windows Terminal Preview is installed:

1. Go to the `Start` menu (windows key)
1. search for `Windows Terminal`
1. Open `Windows Terminal`
1. By default, this will open a new PowerShell terminal window. _Do **not** use the PowerShell terminal window._
1. Click the down arrow <kbd>﹀</kbd> located at the top of the terminal window.
1. Select **Ubuntu** to open a new **Ubuntu Tab**.

    > _Ubuntu will begin to install and you'll be asked to wait for a minute or two for the installation to complete._
    >
    > **IMPORTANT:** It is very important that you remember both the username and password that you create in the next step. If you need to write them down to remember them, that's a great strategy.

1. Once Ubuntu is done installing, you'll be prompted to create a new user (and its password).


## Ubuntu Starting Directory

By default, when you start the Ubuntu shell in Windows Terminal, your starting directory is your Windows user directory. You need to change it so that it starts in your Linux user directory.

1. In the terminal type `cd` and press enter.
1. Type `pwd` and press enter. The path that outputs is called the **home directory** for Ubuntu.

Watch the [WSL Ubuntu Starting Directory](https://www.youtube.com/watch?v=n1YSFT5VK-Y) video to ensure that when you run Ubuntu, you start in the correct directory.

## Node

You will install Node.js using the Windows Terminal. Open Windows Terminal, and in a **new Ubuntu Tab**, copy and paste the following lines one at a time:

```sh
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
```

```sh
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt-get install -y nodejs
```

After a while, you will be prompted with a message asking for permissions. Using the arrow keys on your keyboard, select **Yes** and hit the enter key to continue installing Node.js.

## Node Packages - Web and API Servers

Now that you have Node installed, you can install some open source software that you will need in the course.

Open Windows Terminal, start a **new Ubuntu Tab**, and type in the following command to install `serve` and `json-server`.

```sh
sudo npm i -g serve json-server
```

## Git

Git is how you and your teammates will work on a shard codebase during your time at NSS. Type in the following command to install. You can install the required software using the following command from your **Ubuntu terminal**.

```sh
sudo apt-get install git tig
```

### Configuring Git

> ##### _NOTE: This step requires your GitHub username and email. If you have not yet registered for a [GitHub](#github) account, do that first._

Once Git is done being installed, watch the video on how to [set up global Git configuration](https://youtu.be/66EB9oxGMzQ) so that you can successfully back up your code to GitHub in a few days... once we show you how to do it.

### Handling Permission Issues After Setup

Sometimes, a student has permission issues after installing and configuring Git. To ensure that this doesn't happen to you, watch the [Owning Your Git Config Directory](https://youtu.be/exva3J_jojc) video and follow the steps.

## Z-shell

Z-shell, or _"zsh"_, is a powerful replacement for the standard Bash terminal.

1. Open your Ubuntu terminal.
1. Type in `sudo apt install -y zsh` and then type in your Ubuntu password when it prompts you.

## Oh My Zsh

[Oh My Zsh](http://ohmyz.sh/) is a framework for Z-shell which makes the terminal a pleasure to work in.

Run the following command in your terminal to install `oh-my-zsh`

```sh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### SSH key

SSH is a technology that allows you to create a very secure connection between your computer and a computer located somewhere else in the world. It's an acronym for Secure SHell. When you create an SSH key on your computer, it actually creates two files:

1. A public key file that you share with other people and computers. It is usually named `id_rsa.pub`.
1. A private key file that you never, ever, ever, ever, ever share with anyone. It is usually named `id_rsa`.

### Creating Your SSH Key

Watch a short video for [creating an SSH key in the terminal](https://youtu.be/znRMcNG9_qQ) so that you can work with Github.

### Add SSH Key to Github Account

Now watch the video for [adding your SSH key to your Github account](https://youtu.be/8hlmIObpMd4).

