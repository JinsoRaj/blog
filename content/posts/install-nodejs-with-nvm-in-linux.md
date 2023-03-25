---
title: "Install Nodejs With Nvm in Linux"
description: "Install Nodejs With Nvm in Linux"
date: 2023-03-24T16:23:22+05:30
draft: false

tags: ["nodejs", "linux", "installation", "nvm"]
categories: ["Linux","Programming", "Tech"]
featuredImage: "/node-nvm.webp"
featuredImagePreview: "/node-nvm.webp"

toc:
  enable: true
  auto: true
---
<br>
--- 

## Installation 

A way of installing Node.js that is particularly flexible is to use nvm, the **Node Version Manager**. This piece of software allows you to install and maintain many different independent versions of Node.js, and their associated Node packages, at the same time.

Audit the script to make sure it isn’t doing anything you don’t agree with.

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh
```

Review the script and make sure you are comfortable with the changes it is making.

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

This will install the nvm script to your user account. To use it, you must first source your .bashrc file:

```bash
source ~/.bashrc
```

---

Now, you can ask NVM which versions of Node are available:

```bash
nvm list-remote
```

You can install a version of Node by writing in any of the release versions listed. 

```bash
nvm install v18.13.0
```

You can view the different versions you have installed by listing them:

```bash
nvm list
```

You can switch between installed versions with nvm use:

```bash
nvm use v14.10.0
```

---

## Uninstall

To uninstall a version of Node.js that you installed using nvm, first determine whether it is the current active version:

```bash
nvm current
```

If the version you are targeting is not the current active version, you can run:

```bash
nvm uninstall v18.13.0 
```
---

If the version you would like to remove is the current active version, you first need to deactivate nvm to enable your changes:

```bash
nvm deactivate
```

Then you can uninstall the current version using:

```bash
nvm uninstall <your-version>
```
---

## Errors

Build Error:

```text
npm ERR! code 1
npm ERR! path /home/ubuntu/mine/myfolder/node_modules/deasync
npm ERR! command failed
npm ERR! command sh -c node ./build.js
npm ERR! gyp info it worked if it ends with ok
npm ERR! gyp info using node-gyp@7.1.2
npm ERR! gyp info using node@16.10.0 | linux | arm64
npm ERR! gyp ERR! build error 
npm ERR! gyp ERR! 
stack Error: not found: make npm/node_modules/node-gyp/bin/node-gyp.js" "rebuild"
npm ERR! gyp ERR! cwd /home/ubuntu/mine/myfolder/node_modules/deasync
npm ERR! gyp ERR! node -v v16.10.0
npm ERR! gyp ERR! node-gyp -v v7.1.2
npm ERR! gyp ERR! not ok 
npm ERR! Build failed
```

Solution:

```bash
sudo apt-get install build-essential
```

