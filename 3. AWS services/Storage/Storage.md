# Storage

What cloud service provider you're using they're usually broken down into these three types

## Elastic Block Storage - Block

- data is split into evenly split blocks
- directly accessed by the operating system 
- supports only a single right volume 
- Imagine you have an application over here and that application is using a virtual machine that has a specific operating system and then it has a drive mounted to it uh could be using FC or iSCSI
- You need a virtual Drive attached to your VM is when you're going to be using block 
- Persistant block storage
- Virtual hard drive in cloud, you can attach to your EC2 instances.
- Select different kinds of hard drives - SSD, IOPS SSD, Throughput HHD, Cold HHD

## AWS Elastic File Storage - File

- File is stored with data and metadata 
- multiple connections via a network share 
- supports multiple reads, writing locks the file 
- We could have an application but it doesn't necessarily have to be an application and so it's using NASA exports as the means to communicate and so the protocols here can be NFS or SMB which are very common file system protocols 
- When you need a file share where multiple users where multiple users need to access the same drive 
- This is pretty common where you might have multiple virtual machines and you just want to act as like one uh Drive 
- One example that could be like let's say you're running a Minecraft server you're only allowed to have one world on a particular single drive but you want to be able to have multiple virtual machines to maximize that compute that'd be a case for that.
- Cloud native NFS file system storage
- File storage you can mount to multiple EC2 instances at a time.
When you need to share files b/w multiple servers

## AWS S3 - Object

- object is stored with data, metadata and a unique ID 
- scales with limited no file limit or storage limit 
- Supports multiple reads and write so there are no locks 
- The protocol here we're going to be using https and API 
- When you just want to upload files and not have to worry about the underlying infrastructure 
- Not intended for high IOPs - input and outputs per seconds


[Storage](st1.png)

## Others

### Storage Gateway 

- This is a hybrid cloud storage service that extends your on premise storage to the cloud 
- we got three offerings here: 
	- File Gateway so extend your local storage to Amazon S3 volume
	- Volume Gateway caches your local drive to S3 so you have a continuous backup of the local files in the cloud 
	- Tape Gateway stores files onto virtual tapes for backing up your files on very cost effective long-term storage

### AWS Snow Family

- storage devices used to physically migrate large amounts of data to the cloud 
- snowball and snowball Edge these are briefcase size data storage devices between 50 to 80 terabytes (I think snowball is not available anymore)
- snowmobile this is a cargo container filled with racks of storage and compute that is transported a semi trailer tractor truck to transfer up to 100 petabytes of data per trailer 
- snow cone this is a very small version of snowball that can transfer 8 TB of data

### AWS backup 

- a fully managed backup service that makes it easy to centralize and automate the backup of data across multiple a services 
- Eg. EC2, EBS, RDS, DynamoDB, EFS, storage Gateway you create the backup plans 

### Cloudendure disaster recovery 

- Continuously replicates your machine in a lowcost staging area in your target AWS account and preferred region enabling fast and reliable recovery in case of IT data center failures 

### Amazon FSX 

- feature Rich and highly performant file system that can be used for windows (SMB) or Linux (luster) 
	- Amazon FSX for Windows file server uses SMB protocol and allow you to mount FSX to Windows servers 
	- Amazon FSx for luster uses uh Linux's luster file system and allows you to mount FSX Linux servers