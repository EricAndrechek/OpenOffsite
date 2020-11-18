# OpenOffsite

## An open-source service designed to simplify decentralized offsite data backups among the community.

### How it works

OpenOffsite acts as the gateway to an offsite raid system, where your data is split up into 5 (this is an arbitrary number, need to research what is optimal) parts and then shared across our network of users onto different servers across the globe. Your local copy of your data is used by you, and in the event that your hard drive fails or is damaged, you can recover your data from the network of servers.

This file split up and encryption utilizes an open-source project called [horcrux](https://github.com/jesseduffield/horcrux). In our service, we split your file into 5 parts in such a manner that only 3 are required to piece all of your data back together. This means that even if 2 of your 5 backups go offline or are corrupted, you can still piece together your data.

![How it works diagram](ServerDiagram.png)

### Requirements

In order to use OpenOffsite as part of our decentralized network of users, you must be willing to offer 5 times the amount of data you want backed up offsite as your own backup server for other people. This means if you want to backup 250GB offsite, you will need an additional 1TB to backup other user's data. This excess of storage ensures there is always space to backup your data offsite on command, and that there are duplicates and redundancies in place so that you need not worry about the safety of your offsite data.

Furthermore, by utilizing another open-source tool called [croc](https://github.com/schollz/croc), you do not even require opening up your server to the public internet or sharing your IP address with anyone else. The entire data transfer is routed through croc's proxy service and is more often than not capped by your internet's upload speed than anything else.
