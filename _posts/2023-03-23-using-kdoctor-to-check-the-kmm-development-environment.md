---
title: "Using Kdoctor to check the KMM development environment"
header:
  teaser: "assets/images/aludmila-gdev/agdev-kmm.png"
categories:
- Android
- iOS
tags:
  - mobile development
  - android
  - kotlin
  - ios
  - kmm
  - hybrid mobile development
toc: true
---
## What is kdoctor?

[KDoctor](https://github.com/Kotlin/kdoctor) is a diagnostic tool for [Kotlin Multiplatform Mobile](https://kotlinlang.org/lp/mobile/) development environments. Its purpose is to help detect and troubleshoot problems and currently **only works for the MacOS operating system**.

___
### Some relevant facts about KDoctor

* It was developed by JetBrains, the company responsible for creating the Kotlin programming language.
* The library can be used in cross-platform Kotlin projects, including projects for Android, iOS and other platforms.
* Can help identify common issues in Kotlin projects, such as outdated dependencies, incorrect Gradle configurations, and compatibility issues between different library versions.
* The library ships as a Gradle plugin, which means it can be easily integrated into existing Kotlin projects.
* KDoctor is a useful tool for Kotlin developers who want to keep their projects up-to-date and well-maintained. By identifying problems at an early stage, the library can help prevent more serious problems in the future.

___
## Prerequisites

It's recommended that you run this tutorial before trying to use Kdoctor: [How do I set up my native Android development environment](https://www.aludmila-gdev.com/android/how-do-i-set-up-my-native-android-development-environment/)
{: .notice--info}

In this section, I share with you the configuration of my computer, and I consider the list of what are the minimum requirements necessary for you to follow the tutorial.

|        MacBook Pro (Retina, 13-inch, Mid 2014)        |
|:-----------------------------------------------------:|
|             macOS Big Sur 11.7.1 (20G918)             |
|             Processor 8 GB 1600 MHz DDR3              |
|               Memory 8 GB 1600 MHz DDR3               |
|              Graphics Intel Iris 1536 MB              |


However, it's ok if you have a different hardware configuration! **Try to follow the steps and adapt them to your context!**
{: .notice--info}



## My experience using the tool for the first time

### Configuration and installation

Installing the tool was very easy. To do this, I ran the command below in my terminal:

```shell
brew install kdoctor
```

After 5 minutes of waiting, KDoctor was installed and I had no problems during this process.

The interface, despite being via a terminal, was very friendly and the feedback was clear during its use.
  {% include figure image_path="assets/images/aludmila-gdev/agdev-install-kdoctor.png" alt="" caption="" %}
___
### Usage

To perform the diagnostics of my development environment, I ran the following command in the terminal:

```shell
kdoctor
```

So I got the following result:
{% include figure image_path="assets/images/aludmila-gdev/agdev-kdoctor-result.png" alt="" caption="" %}

So I followed the recommended steps, and downloaded and installed [Xcode](https://developer.apple.com/xcode/)

After installing XCode, I got a known problem, which I solved by running the following command:

```shell
xcode-select --install
```

More details about the problem I experienced can be found at this link: [xcode - Why am I getting an “invalid active developer path” when attempting to use Git after upgrading to macOS Ventura? - Ask Different](https://apple.stackexchange.com/questions/254380/why-am-i-getting-an-invalid-active-developer-path-when-attempting-to-use-git-a)

At this point, I unfortunately had another problem: Even correcting all points suggested by the tool, KDoctor still kept accusing inconsistencies in my environment:
{% include figure image_path="assets/images/aludmila-gdev/agdev-kdoctor-issue.png" alt="" caption="" %}

After a while of researching, I found these links that brought me a solution to this problem

```shell
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer

```

After running this command and trying again, the problem was finally solved:
{% include figure image_path="assets/images/aludmila-gdev/agdev-kdoctor-issue-solved.png" alt="" caption="" %}

After solving the problems in xcode, it's time to install [Cocoapods](https://guides.cocoapods.org/using/getting-started.html#installation).

````shell
gem install cocoapods
````

And then finally my environment is ready!
{: .notice--success}
{% include figure image_path="assets/images/aludmila-gdev/agdev-kdoctor-ready.png" alt="" caption="" %}
___
## Useful links

- [How do I set up my native Android development environment](https://www.aludmila-gdev.com/android/how-do-i-set-up-my-native-android-development-environment/)
- [Set up an environment - Kotlin Documentation](https://kotlinlang.org/docs/multiplatform-mobile-setup.html#check-your-environment)
- [GitHub - Kotlin/kdoctor: Environment analysis tool](https://github.com/Kotlin/kdoctor)
- [Kotlin Multiplatform for Cross-Platform Mobile Development - Kotlin Multiplatform Mobile](https://kotlinlang.org/lp/mobile/)