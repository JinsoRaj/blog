---
title: "Kill Process Running on a Port - Linux"
description: "Kill Process Running on a Port - Linux"
date: 2023-03-24T16:25:46+05:30
draft: false

tags: ["linux", "terminal", "process"]
categories: ["Linux"]
featuredImage: "/ps-linux.webp"
featuredImagePreview: "/ps-linux.webp"

toc:
  enable: false
  auto: true
---
<br><br>


As an instance, to kill all the process running on TCP port 8000, use the below command to detect the process id:

```bash
sudo lsof -i TCP:8000
```

And now kill it with its pid:

```bash
kill -9 <pid_value>
```

Certain processes like `mysqld` and `apache2` might restart after you have killed them using the above commands. Even if you use the `killall` command, they will still appear after some time. 

In such cases, I advise you to use application specific commands to stop a service. For example, to kill the Apache process on Ubuntu, use the command:

```bash
sudo systemctl stop mysqld
```

---

## Extra

See a list of Top process that using the most memory or CPU or disk:
    
```bash
top
```
    
```bash
htop
```

Search a running process:

```bash
ps -ef | grep firefox
```

```bash
pgrep firefox
```