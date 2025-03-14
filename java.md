# Java Tools (Under Construction)

You will need

- [Java LTS version](https://adoptium.net/en-GB/)
- [Kotlin](https://kotlinlang.org/docs/command-line.html)
- [Gradle](https://gradle.org/install/)
- [Maven](https://maven.apache.org/download.cgi)

The preferred way of installing all of the tools is [SDKMAN!](https://sdkman.io). But this tool works only **on unix-based machines like macOS and Linux.** By using SDKMAN you can install and configure all of these using command line. You can also install multiple versions of these in the same computer.

Windows options are

- [Cygwin](https://www.cygwin.com)
- Windows Subsystem for Linux (install instructions below)
  - GUI exercises can be complicated in WSL2! 😞

## macOS installation for sdkman

Open terminal and give command:

    curl -s "https://get.sdkman.io" | bash

Reboot your terminal. Now install

- Java LTS (Temurin)
- Kotlin
- Gradle
- Maven

See commands how to install below ⬇️

## Windows 10+: Subsystem for Linux and sdkman

You can install [Windows subsystem for linux](https://www.windowscentral.com/install-windows-subsystem-linux-windows-10) and [Ubuntu from the Store](https://www.microsoft.com/en-us/p/ubuntu-2004/9n6svws3rx71?activetab=pivot:overviewtab). You can also install [new terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) for windows.

Then you can open the new terminal and ubuntu:

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645172659368_2022-02-18+10.23.58.gif)

Install zip and unzip apps:

    sudo apt-get install unzip zip

Then install sdkman by giving following command

    curl -s "https://get.sdkman.io" | bash

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645172983047_2022-02-18+10.28.05.gif)

Reboot you terminal, so basically start ubuntu again.

# Java Installation

Type

    sdk list java

in terminal.

It should display:

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645173074838_Screenshot+2022-02-18+at+10.31.10.png)

Install Java Temurin 21.x.

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645173117641_Screenshot+2022-02-18+at+10.31.54.png)

To do this, give command:

    sdk install java 21...  // or similar!

Where 21… is the identifier (Version may vary)

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645173200172_Screenshot+2022-02-18+at+10.33.17.png)

Java should be installed now:

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645173278116_Screenshot+2022-02-18+at+10.34.15.png)

Just write

    java -version
    javac -version

To see that it works. You may need to reboot your terminal.

# Kotlin Installation

Now install the latest version of kotlin. Use

    sdk list kotlin

and

    sdk install kotlin

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645173430865_2022-02-18+10.35.36.gif)

# Gradle Installation

Now install the latest version of gradle. Use

    sdk list gradle

and install most recent gradle

    sdk install gradle

![](https://paper-attachments.dropboxusercontent.com/s_FD93635640D0A182BFE5C4E8CB3CC57B524B6F5FB5561D6C8E644FEACBE659D3_1645173548702_2022-02-18+10.37.49.gif)

# Maven Installation

Now install the latest version of gradle. Use

    sdk list maven

and install most recent maven

    sdk install maven

# Git?

If you cannot get git working in WSL2, follow these steps for [authentication](https://paper.dropbox.com/doc/GitHub-and-keys--CHZYK~zpG0fSqoFTLryyR4sSAg-ckErqW0Hu3PGe4x4J0lL9).
