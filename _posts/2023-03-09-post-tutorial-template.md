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


However, it's ok if you have a different hardware configuration! Try to follow the steps and adapt them to your context!
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

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

3. Wait while the Homebrew installation script downloads and runs.
4. When prompted, type your admin password and press Enter.
5. Wait while Homebrew is installed on your system. This may take a few minutes, depending on the speed of your internet connection.
6. When the installation is complete, Terminal will display a message that Homebrew has been successfully installed.
7. To verify that Homebrew installed correctly, run the following command in Terminal:

`brew --version`

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

`zsh --version`

3. If zsh is already installed, you will see the version of zsh installed on your system. 
4. If zsh is not installed, you can install zsh using Homebrew. If you don't already have Homebrew installed, follow the steps in "[Install Homebrew](#install-homebrew)" before continuing. 
5. Type the following command in Terminal and press Enter to install zsh using Homebrew:
`brew install zsh`
6. Wait while Homebrew downloads and installs zsh on your system. This may take a few minutes, depending on the speed of your internet connection. 
7. Once the installation is complete, enter the following command in Terminal to change your default shell to zsh:

`chsh -s /bin/zsh`
8. When prompted, type your admin password and press Enter. 
9. Close Terminal and open a new Terminal. zsh will now be the default shell you use in Terminal.

Ready! Now zsh is installed on your Mac and you can use it as your default shell in Terminal. zsh offers a number of customization options and features that can make your Terminal experience more efficient and enjoyable.
{: .notice--success}















## Configuration
A section that explains how to configure the software to run properly. This might include configuring options, registering accounts, or connecting to external services.

## Basic Usage
A section that describes the basic functionality of the software and how to use it. This may include examples and screenshots to illustrate the use of the software.

## Advanced Features
A section that describes advanced features of the software and how to use them. This can include more complex and comprehensive examples.

## Tips & Tricks
A section that features helpful tips and tricks to get the most out of the software. This may include keyboard shortcuts, hidden features, or advanced techniques.

## Troubleshooting
A section that describes common problems that may occur when using the software and how to resolve them. This may include common error messages and their solutions.

## Conclusion
A conclusion that summarizes the tutorial and highlights its main points. It may include suggestions for next steps or additional learning resources.

## References
A section that lists any additional sources of information used in the tutorial, such as official documentation, tutorials, or other references.



### Header three

#### Header four

##### Header five

###### Header six

## Blockquotes

Single line blockquote:

> Stay hungry. Stay foolish.

Multi line blockquote with a cite reference:

> People think focus means saying yes to the thing you've got to focus on. But that's not what it means at all. It means saying no to the hundred other good ideas that there are. You have to pick carefully. I'm actually as proud of the things we haven't done as the things I have done. Innovation is saying no to 1,000 things.

<cite>Steve Jobs</cite> --- Apple Worldwide Developers' Conference, 1997
{: .small}

## Tables

| Employee         | Salary |                                                              |
| --------         | ------ | ------------------------------------------------------------ |
| [John Doe](#)    | $1     | Because that's all Steve Jobs needed for a salary.           |
| [Jane Doe](#)    | $100K  | For all the blogging she does.                               |
| [Fred Bloggs](#) | $100M  | Pictures are worth a thousand words, right? So Jane × 1,000. |
| [Jane Bloggs](#) | $100B  | With hair like that?! Enough said.                           |

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|-----------------------------|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=============================|
| Foot1   | Foot2   | Foot3   |

## Definition Lists

Definition List Title
:   Definition list division.

Startup
:   A startup company or startup is a company or temporary organization designed to search for a repeatable and scalable business model.

#dowork
:   Coined by Rob Dyrdek and his personal body guard Christopher "Big Black" Boykins, "Do Work" works as a self motivator, to motivating your friends.

Do It Live
:   I'll let Bill O'Reilly [explain](https://www.youtube.com/watch?v=O_HyZ5aW76c "We'll Do It Live") this one.

## Unordered Lists (Nested)

* List item one
  * List item one
    * List item one
    * List item two
    * List item three
    * List item four
  * List item two
  * List item three
  * List item four
* List item two
* List item three
* List item four

## Ordered List (Nested)

1. List item one
  1. List item one
    1. List item one
    2. List item two
    3. List item three
    4. List item four
  2. List item two
  3. List item three
  4. List item four
2. List item two
3. List item three
4. List item four

## Forms

<form>
  <fieldset>
    <legend>Personalia:</legend>
    Name: <input type="text" size="30"><br>
    Email: <input type="text" size="30"><br>
    Date of birth: <input type="text" size="10">
  </fieldset>
</form>

## Buttons

Make any link standout more when applying the `.btn` class.

```html
<a href="#" class="btn--success">Success Button</a>
```

[Default Button](#){: .btn}
[Primary Button](#){: .btn .btn--primary}
[Success Button](#){: .btn .btn--success}
[Warning Button](#){: .btn .btn--warning}
[Danger Button](#){: .btn .btn--danger}
[Info Button](#){: .btn .btn--info}
[Inverse Button](#){: .btn .btn--inverse}
[Light Outline Button](#){: .btn .btn--light-outline}

```markdown
[Default Button Text](#link){: .btn}
[Primary Button Text](#link){: .btn .btn--primary}
[Success Button Text](#link){: .btn .btn--success}
[Warning Button Text](#link){: .btn .btn--warning}
[Danger Button Text](#link){: .btn .btn--danger}
[Info Button Text](#link){: .btn .btn--info}
[Inverse Button](#link){: .btn .btn--inverse}
[Light Outline Button](#link){: .btn .btn--light-outline}
```

[X-Large Button](#){: .btn .btn--primary .btn--x-large}
[Large Button](#){: .btn .btn--primary .btn--large}
[Default Button](#){: .btn .btn--primary }
[Small Button](#){: .btn .btn--primary .btn--small}

```markdown
[X-Large Button](#link){: .btn .btn--primary .btn--x-large}
[Large Button](#link){: .btn .btn--primary .btn--large}
[Default Button](#link){: .btn .btn--primary }
[Small Button](#link){: .btn .btn--primary .btn--small}
```

## Notices

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice}` class.
{: .notice}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--primary}` class.
{: .notice--primary}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--info}` class.
{: .notice--info}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--warning}` class.
{: .notice--warning}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--success}` class.
{: .notice--success}

**Watch out!** This paragraph of text has been [emphasized](#) with the `{: .notice--danger}` class.
{: .notice--danger}

## HTML Tags

### Address Tag

<address>
  1 Infinite Loop<br /> Cupertino, CA 95014<br /> United States
</address>

### Anchor Tag (aka. Link)

This is an example of a [link](http://apple.com "Apple").

### Abbreviation Tag

The abbreviation CSS stands for "Cascading Style Sheets".

*[CSS]: Cascading Style Sheets

### Cite Tag

"Code is poetry." ---<cite>Automattic</cite>

### Code Tag

You will learn later on in these tests that `word-wrap: break-word;` will be your best friend.

### Strike Tag

This tag will let you <strike>strikeout text</strike>.

### Emphasize Tag

The emphasize tag should _italicize_ text.

### Insert Tag

This tag should denote <ins>inserted</ins> text.

### Keyboard Tag

This scarcely known tag emulates <kbd>keyboard text</kbd>, which is usually styled like the `<code>` tag.

### Preformatted Tag

This tag styles large blocks of code.

<pre>
.post-title {
	margin: 0 0 5px;
	font-weight: bold;
	font-size: 38px;
	line-height: 1.2;
	and here's a line of some really, really, really, really long text, just to see how the PRE tag handles it and to find out how it overflows;
}
</pre>

### Quote Tag

<q>Developers, developers, developers&#8230;</q> &#8211;Steve Ballmer

### Strong Tag

This tag shows **bold text**.

### Subscript Tag

Getting our science styling on with H<sub>2</sub>O, which should push the "2" down.

### Superscript Tag

Still sticking with science and Albert Einstein's E = MC<sup>2</sup>, which should lift the 2 up.

### Variable Tag

This allows you to denote <var>variables</var>.