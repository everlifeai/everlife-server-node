# Setting up Everlife Server Node

This document contains instructions for setting up and running the
**Everlife** avatar on a server machine. To simply get up and running with **Everlife**, you may want to [install the community node instead](https://github.com/everlifeai/everlife-node-releases/releases).

## Install

To install the Everlife avatar, follow the instructions according to your operating system. After installing, use the `/intro` command and the avatar itself will walk you through a short guide.

| Jump to: | [Windows](#windows) | [MacOS](#macos) | [Ubuntu / DEBIAN](#ubuntudebian) | [CentOS / Red Hat](#centos) | [Docker](#docker) |
| -------- | ------------------- | --------------- | -------------------------------- | --------------------------- | ----------------- |
|          |                     |                 |                                  |                             |                   |

------

<a name=docker></a>

## Docker

One option for installation is to use [Docker](https://www.docker.com). If you are comfortable using Docker you do not need to install the other pre-requisites like NodeJS and Python as the container is already set up with everything you need.

### Docker Install Steps

There are two options for running docker. The first way is to download and use this repository to run and the other is to simply pull from [Docker Hub](https://hub.docker.com/r/everlifeai/everlife-server-node).

#### Running using the GitHub repo

This is the most flexible way to run and would be recommended if you want to edit the source code and modify the node for your particular use.

1. Install [Docker](https://www.docker.com)
2. Install [Git](https://git-scm.com/)
3. Download [this repo](https://github.com/everlifeai/everlife-server-node)
4. Run `./run-docker.sh`

#### Running from Docker Hub

This is the simplest option. Simply pull and run from [the Docker Hub](https://hub.docker.com/r/everlifeai/everlife-server-node) directly.

```sh
$> docker run -it --rm -p 8191:8191 -p 8192:8192 -v $(cwd)/everlifeai:/root/everlifeai everlifeai/everlife-server-node:latest node run.js
```

Once you are set up, you can proceed to [editing the configuration](#config), and setting up your [telegram chatbot](#telegram).

------

<a name=macos></a>

## Mac Setup

Installing on your Mac is simple. You can use a package manager like [Homebrew](https://brew.sh) to simplify the package installs.

1. Install [Git](https://git-scm.com/)
2. Download [this repo](https://github.com/everlifeai/everlife-server-node)
3. Install [NodeJS](https://nodejs.org/en/download/) LTS Version: 14.16.0 and above
4. Install [Python 2.7](https://www.python.org/)
5. Run `./run-mac.sh`

Once you are set up, you can proceed to [editing the configuration](#config), and setting up your [telegram chatbot](#telegram).

------

<a name=ubuntudebian></a>

## Ubuntu/Debian Setup

Setting up on any *-nix machine is simple as well. Use the built in package manager to install the required packages (`yum install` or `apt-get`).

1. Install [Git](https://git-scm.com/)
2. Download [this repo](https://github.com/everlifeai/everlife-server-node)
3. Install [NodeJS](https://nodejs.org/en/download/) LTS Version: 14.16.0 and above
4. Install [Python 2.7](https://www.python.org/)
5. Run `./run-linux.sh`

Once you are set up, you can proceed to [editing the configuration](#config), and setting up your [telegram chatbot](#telegram).

------

<a name=centos></a>

## CentOS / Red Hat Setup

Setting up on any *-nix machine is simple as well. Use the built in package manager to install the required packages (`yum install` or `apt-get`).

1. Install [Git](https://git-scm.com/)
2. Download [this repo](https://github.com/everlifeai/everlife-server-node)
3. Install [NodeJS](https://nodejs.org/en/download/) LTS Version: 14.16.0 and above
4. Install [Python 2.7](https://www.python.org/)
5. Run `./run-linux.sh`

Once you are set up, you can proceed to [editing the configuration](#config), and setting up your [telegram chatbot](#telegram).

------

<a name=windows></a>

## Windows Setup

Installing on windows requires a bit more setup as we need to set up some *-nix like tools. The simple way to do this is to install a [Cygwin distribution](https://www.cygwin.com).

1. Install Cygwin: [64 Bit Version](https://www.cygwin.com/setup-x86_64.exe) or
   [32 Bit Version](https://www.cygwin.com/setup-x86.exe)
2. Install [Git](https://git-scm.com/)
3. Download [this repo](https://github.com/everlifeai/everlife-server-node)
4. Install [NodeJS](https://nodejs.org/en/download/) LTS Version: 14.16.0 and above
5. Install [Python 2.7](https://www.python.org/)
6. Run `./run-win.cmd`

Once you are set up, you can proceed to [editing the configuration](#config), and setting up your [telegram chatbot](#telegram).

------

<a name=config></a>

## Configuration

Your environment, data, and configuration is created under the `$HOME/everlife` folder. Here you will find your blockchain, wallets, configuration, and so on.

The first time you run, this folder will be set up for you.



------

<a name=telegram></a>

## Talking to your new bot over Telegram

In order to talk with your avatar over [Telegram](the://telegram.org) you need to set up a communication channel with it. The steps for doing this are as follows:

1. Go to [Telegram](https://telegram.me/botfather) to create a bot by typing the
   
       `/newbot`
   
    command to create your telegram bot.
   
1. The BotFather will ask you for a name and username, then generate an authorization token for your new bot. The token is a string that looks something like `110201543:AAHdqTcvCH1vGWJxfSeofSAs0K5PALDsaw` .
   
1. Link this new telegram bot with your avatar. To do this, simply save the telegram token in the `cfg.env` file located in the `data` folder somewhere under `$HOME/everlife`.
   
   (To find the exact location of your data folder you can check the logs or pass the `--info` parameter to the run script. For example (`./run-mac.sh —info`).

----

## Next steps

1. You should now join the Everlife network through an **Avatar Hub**. Contact our support channel in discord to get your invite code to join the hub and inform your avatar that you would like to join this Avatar Hub by saying
   
        /use_invite xxxx
   
2. Install and try out various skills

    ```
    "install calculator"
    "install what-wine"
    ```
    
3. Do some work and earn EVER, or buy and NFT asset, or play some game, or develop your own skills. The sky’s the limit. Enjoy!

Feel free to provide us your feedback and issues in our [discord support
channel](https://discord.gg/TDyRSr4).

-----

