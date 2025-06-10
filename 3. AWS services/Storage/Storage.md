# Storage

What cloud service provider you're using they're usually broken down into these three types

## Elastic Block Storage - Block

- data is split into evenly split blocks
- directly accessed by the operating system 
- supports only a single right volume 
- Imagine you have an application over here and that application is using a virtual machine that has a specific operating system and then it has a drive mounted to it uh could be using FC or iSCSI
- You need a virtual Drive attached to your VM is when you're going to be using block 

## AWS Elastic File Storage - File

- File is stored with data and metadata 
- multiple connections via a network share 
- supports multiple reads, writing locks the file 
- We could have an application but it doesn't necessarily have to be an application and so it's using NASA exports as the means to communicate and so the protocols here can be NFS or SMB which are very common file system protocols 
- When you need a file share where multiple users where multiple users need to access the same drive 
- This is pretty common where you might have multiple virtual machines and you just want to act as like one uh Drive 
- One example that could be like let's say you're running a Minecraft server you're only allowed to have one world on a particular single drive but you want to be able to have multiple virtual machines to maximize that compute that'd be a case for that.

## AWS S3 - Object

- object is stored with data, metadata and a unique ID 
- scales with limited no file limit or storage limit 
- Supports multiple reads and write so there are no locks 
- The protocol here we're going to be using https and API 
- When you just want to upload files and not have to worry about the underlying infrastructure 
- Not intended for high IOPs - input and outputs per seconds

[Storage](st1.png)