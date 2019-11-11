
![CLEVER DATA GIT REPO](https://github.com/congmingshuju/git-resources/blob/master/images/0-clever-data-github.png "李聪明 数据")


# 添加驱动器空间 - 扩展AWS的SQL 服务器数据中心的操作系统（跨区卷）的磁盘。
### Adding Drive Space Extending Disks From OS Spanned Volume on SQL Server Datacenter Server in AWS
**发布-日期:  2014年12月2日 (评论)**

## Contents

- [中文](#中文)
- [English](#English)
- [SQL-Logic](#Logic)
- [Build Quality](#Build-Quality)
- [Author](#Author)
- [License](#License) 


## 中文
我们在通过AWS添加空间后使用此方法。当驱动器被添加到操作系统后，我们首先初始化磁盘，而磁盘仍然是“unallocated”，选择你要扩展的驱动器，右键单击并选择“Extend Volume”。我们在AWS的SQL数据库服务器上配置AlwaysOn故障转移群集的时候执行过此操作。服务器版本: Server 2008 R2 Datacenter – Windows 6.1.7601 Service Pack 1 Build 7601。我们添加了驱动器，并在两个节点上进行了扩展（INTE-SQLA-01和INTE-SQLA-02）。这是一种安全的无风险操作，并且不会导致服务或数据库停机。以下是此过程中执行的步骤。我们要扩展的驱动器是SQL Log Drive（DriveL :)。第一，右键单击新磁盘的左侧窗格，然后选择“Initialize Drive”。以下步骤显示了此过程。转到“Start”→“Run”，然后键入“diskmgmt.msc”。添加新磁盘后，只需右键单击并选择“Initialize”即可。


## English
We used this method after the space was added via AWS. Once a drive was added to the OS, we first Initialized the Disk, and while the disk was still ‘unallocated’; go to the drive you want to expand, and right-click and select ‘Extend Volume’. We did this on the SQL Server Database Server Configured with AlwaysOn Failover Cluster within AWS. Server Version: Server 2008 R2 Datacenter – Windows 6.1.7601 Service Pack 1 Build 7601. Drives were added, and expanded on both nodes (INTE-SQLA-01 & INTE-SQLA-02) This was a safe no-risk operation, and did not cause any downtime for Services, or Databases. Below are the steps performed during this process. The drive we wish to extend is the SQL Log Drive ( Drive L: ). First thing you do is right-click the left pane of the new disk and select ‘Initialize Drive’. The following steps show this process. Go to Start à Run, and type in ‘diskmgmt.msc’. Once the new disk has been added, simply right-click and select ‘Initialize’.

---

### 1
![Spanned Volume AWS](images/step-1.jpg?raw=true "步骤1")

### 2
在以下提示中保留默认设置，然后单击“OK”。
On the following prompt keep the default settings, and Click ‘OK’. 
![Spanned Volume AWS](images/step-2.jpg?raw=true "步骤2")

### 3
一旦完成，它将只显示为“Online”，并保持“Unallocated”状态。
Once it’s completed it will simply display as ‘Online’, and remain in an ‘Unallocated’ state.

![Spanned Volume AWS](images/step-3.jpg?raw=true "步骤3")

### 4
返回到你要扩展的原始驱动器（ Drive L:)，然后单击鼠标右键。选择“Extend Volume”。
Go back to the original Drive you wish to extend ( Drive L: ) and right-click. Select 'Extend'.

![Spanned Volume AWS](images/step-4.jpg?raw=true "步骤4")

### 5
在以下提示中单击“Next”。
Click ‘Next’ on the following prompt.
![Spanned Volume AWS](images/step-5.jpg?raw=true "步骤5")

### 6
选择左侧的磁盘，然后单击“Add”，然后单击“Next”。
Select the disk on the left, and click ‘Add’, then ‘Next’.
![Spanned Volume AWS](images/step-6.jpg?raw=true "步骤6")

### 7
点击“Finish”完成。
Click ‘Finish’ and you’re done.

![Spanned Volume AWS](images/step-7.jpg?raw=true "步骤7")

### 8
新磁盘现在是“跨区卷”，在磁盘管理下显示为紫色。从Windows资源管理器中查看，你会看到驱动器为250GB。
The new disks are now ‘Spanned Volumes’ and will be represented in Purple under Disk Management.  When viewed from Windows Explorer; you will see the drive as 250GB.
![Spanned Volume AWS](images/step-8.jpg?raw=true "步骤8")


[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Quality 
| [![Build status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg=true)](https://ci.appveyor.com/project/tygerbytes/resourcefitness) | [![Coveralls](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?branch=master)](https://coveralls.io/github/tygerbytes/ResourceFitness?branch=master) | [![nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](https://www.nuget.org/packages/TW.Resfit.Core/) |
|-|-|-|

>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](https://ci.appveyor.com/project/tygerbytes/resourcefitness/history)

## Author

- **李聪明 数据 Clever Data**
- **Mike的数据库宝典 Mikes Database Collection**
- **李聪明** "Lee Songming"

[![Gist](https://img.shields.io/badge/Gist-李聪明数据-<COLOR>.svg)](https://gist.github.com/congmingshuju)
[![Twitter](https://img.shields.io/badge/Twitter-mike的数据库宝典-<COLOR>.svg)](https://twitter.com/mikesdatawork?lang=en)
[![Wordpress](https://img.shields.io/badge/Wordpress-mike的数据库宝典-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)

---
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Lee Songming](https://github.com/congmingshuju/git-resources/blob/master/images/clever-data-gist-z5.png "李聪明 数据")



