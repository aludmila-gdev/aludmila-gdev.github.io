---
author_profile: true
title: "How do I set up my native Android development environment."
header:
  teaser: "assets/images/teaser-500x300.jpg"
categories:
- Android
tags: 
  - mobile development
  - android
  - kotlin
  - environment
toc: true
---

## Introduction
an introduction to the software that will be covered, explaining its features and functionality.

## Prerequisites
In this section, I share with you the configuration of my computer, and I consider the list of what are the minimum requirements necessary for you to follow the tutorial.

|        MacBook Pro (Retina, 13-inch, Mid 2014)        |
|:-----------------------------------------------------:|
|             macOS Big Sur 11.7.1 (20G918)             |
|             Processor 8 GB 1600 MHz DDR3              |
|               Memory 8 GB 1600 MHz DDR3               |
|              Graphics Intel Iris 1536 MB              |


However, it's ok if you have a different hardware configuration! **Try to follow the steps and adapt them to your context!**
{: .notice--info}


## Installation
### Install Android Studio

1. Visit the official [Android Studio Website](https://developer.android.com/studio){: .btn .btn--primary}
2. Click the "Download Android Studio" button and wait for the installer to download.
3. Once downloaded, run the installer file and follow the on-screen instructions to install Android Studio. During installation, you will be able to choose which components you want to install and which directory you want to install Android Studio in.
4. Once installation is complete, launch Android Studio and follow the onscreen instructions to complete the initial setup. This includes installing the Android SDK and setting development preferences.

After the initial setup is complete, you're ready to start developing Android apps using Android Studio!
{: .notice--success}

### Install Java
1. Visit the official [Oracle website to download Java](https://www.oracle.com/technetwork/java/javase/downloads/index.html){: .btn .btn--primary}
2. On the downloads page, look for the "Java SE" section and click on the "Download" button corresponding to the Java version you want to install. Be sure to choose the version compatible with your operating system.
3. On the next page, accept the terms and conditions and click the "Download" button. The download should start automatically.
4. When the download is complete, open the .dmg file that was downloaded. This should open a window containing the installer file.
5. Double-click the installer file to launch it. Follow the on-screen instructions to complete installing Java on your computer.

After installation is complete, you can verify that Java is working correctly by typing `java -version` in Terminal. If Java is installed correctly, you should see a message with information about the installed version.
{: .notice--success}

### Install Homebrew
1. Open the Terminal app on your Mac. You can find it in the "Utilities" folder inside the "Applications" folder.
2. Paste the following command into the Terminal window and press Enter:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. Wait while the Homebrew installation script downloads and runs.
4. When prompted, type your admin password and press Enter.
5. Wait while Homebrew is installed on your system. This may take a few minutes, depending on the speed of your internet connection.
6. When the installation is complete, Terminal will display a message that Homebrew has been successfully installed.
7. To verify that Homebrew installed correctly, run the following command in Terminal:

```
brew --version
```

8. This should display the version of Homebrew you just installed.

Now that Homebrew is installed, you can use the `brew` command to install and manage packages on your Mac. To install a package, simply type "brew install [package name]" in Terminal and press Enter. Homebrew will automatically download and install the package and any required dependencies.
{: .notice--success}


### Install iTerm2

iTerm2 offers several features and customization options that can be useful for advanced users or those who need more flexibility in using the terminal.

1. Visit the [iTerm2 official website](https://www.iterm2.com/){: .btn .btn--primary}
2. Open your web browser and visit the iTerm2 official website:
3. Click the "Download" button to download the iTerm2 installation file. 
4. When the download is complete, open the downloaded .zip file and extract the iTerm.app file. 
5. Move the iTerm.app file to your Mac's "Applications" folder. 
6. Double-click the iTerm.app file in the "Applications" folder to launch iTerm2. 
7. iTerm2 may display a security warning asking you to confirm that you want to open the application. Click "Open" to continue. 
8. iTerm2 will launch and you can start using it right away.

Ready! You now have iTerm2 installed on your Mac and can use it as an alternative terminal to the standard macOS Terminal.
{: .notice--success}


### Install zsh
1. Open the Terminal app on your Mac. You can find it in the "Utilities" folder inside the "Applications" folder. 
2. Type the following command in Terminal and press Enter to check if zsh is already installed on your Mac:

```
zsh --version
```

3. If zsh is already installed, you will see the version of zsh installed on your system. 
4. If zsh is not installed, you can install zsh using Homebrew. If you don't already have Homebrew installed, follow the steps in "[Install Homebrew](#install-homebrew)" before continuing. 
5. Type the following command in Terminal and press Enter to install zsh using Homebrew:

```
brew install zsh
```

6. Wait while Homebrew downloads and installs zsh on your system. This may take a few minutes, depending on the speed of your internet connection. 
7. Once the installation is complete, enter the following command in Terminal to change your default shell to zsh:

```
chsh -s /bin/zsh
```

8. When prompted, type your admin password and press Enter. 
9. Close Terminal and open a new Terminal. zsh will now be the default shell you use in Terminal.

Ready! Now zsh is installed on your Mac and you can use it as your default shell in Terminal. zsh offers a number of customization options and features that can make your Terminal experience more efficient and enjoyable.
{: .notice--success}

### Install oh-my-zsh
1. Open the terminal
2. Paste the following command and [ENTER]

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Configure your .zshrc file
1. Open the terminal
2. Copy the commands below respectively and [ENTER] after each of them

```sh
cd
```

```sh
open .
```
3. Now download this [.zshrc file] and copy it to the open folder.

### Install NVM
1. Open the iterm
2. Copy the commands below respectively and [ENTER] after each of them:

```sh
brew update
```

```sh
 brew install nvm 
```

```sh
 mkdir $HOME/.nvm
```
### Configure GitHub credentials

Now that your [Iterm] is configured, we can start using it instead of the standard terminal.

1. Open the iterm
2. Copy the commands below respectively and [ENTER] after each of them:

  ```sh
   git config --global user.name "Your Name"
  ```
  
  ```sh
   git config --global user.email "your_email@example.com"
  ```

Now you will need to follow the documentation available on github for [Generating a new SSH key and adding it to the ssh-agent] and [Adding a new SSH key to your GitHub account].
   {: .notice--success}

## Testing the environment

### Clone a test project

After setting up your ssh keys, you should be able to clone a test repository to build an Android project. To do this, run the following command in your iterm:
```sh
 git clone git@github.com:aludmila-gdev/DiceRoller.git
```
If there is an error at this stage, you can search for an answer on Google, or contact me by sending the error message, and I can try to help you in some way!

### Open and run the test project

Now that the initial configurations are done, let's test them by building a pre-existing project, which was downloaded from git in the previous step.

1. Open Android Studio, and you should see a screen like this:
   {% include figure image_path="assets/images/home-android-studio.png" alt="" caption="" %}

2. Open the project you downloaded earlier:

   {% include figure image_path="assets/images/open-project.png" alt="" caption="" %}

3. [Create a virtual device] following the guideline;

4. Once you have a device created, use the play icon to build and view the app in the emulator:

   {% include figure image_path="assets/images/play-app.png" alt="" caption="" %}

5. Wait for the app to build, this may take a few minutes. At the end you should see a screen similar to this:

   {% include figure image_path="assets/images/environment-working.png" alt="" caption="" %}

6. Congratulations!! you have a completely configured android environment, and now you can start building your apps!🥳
   {: .notice--success}


## Referral Links


- [Download android studio](https://developer.android.com/studio)
- [.zshrc file](https://github.com/aludmila-gdev/android-environment-setup/blob/master/.zshrc)
- [Previous Java releases](https://www.oracle.com/java/technologies/downloads/archive/)
- [Create a virtual device](https://developer.android.com/studio/run/managing-avds)
- [Java SE Development Kit 11.0.2](https://download.oracle.com/otn/java/jdk/11.0.2+9/f51449fcd52f4d52b93a989c5c56ed3c/jdk-11.0.2_osx-x64_bin.dmg)
- [Java SE Development Kit 8u251](https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html#license-lightbox)
- [Iterm](https://iterm2.com/)
- [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)


[download android studio]: <https://developer.android.com/studio>
[.zshrc file]: <https://github.com/knludi/android-environment-setup/blob/master/.zshrc>
[Previous Java releases]: <https://www.oracle.com/java/technologies/downloads/archive/>
[Create a virtual device]: <https://developer.android.com/studio/run/managing-avds>
[Java SE Development Kit 11.0.2]: <https://download.oracle.com/otn/java/jdk/11.0.2+9/f51449fcd52f4d52b93a989c5c56ed3c/jdk-11.0.2_osx-x64_bin.dmg>
[Java SE Development Kit 8u251]: <https://www.oracle.com/java/technologies/javase/javase8u211-later-archive-downloads.html#license-lightbox>
[Iterm]: <https://iterm2.com/>
[Generating a new SSH key and adding it to the ssh-agent]: <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent>
[Adding a new SSH key to your GitHub account]: <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account>
 
