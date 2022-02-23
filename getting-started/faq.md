---
description: Frequently asked questions
---

# FAQ

On this page you'll find a collection of frequently asked questions about NexusForever.\
It is recommended that you have a read through this page before asking any questions on the project.

### General

* **What Is NexusForever?**\
  NexusForever is a server emulator for the defunct MMORPG (massively multiplayer online role playing game) WildStar which was developed by Carbine and published by NCSoft.
* **Does the NexusForever project accept donations?**\
  ****We will never ask for donations, period. We give our time and knowledge to the project out of our love for WildStar and not monetary gain.
* **When will NexusForever be finished?**\
  ****There is no set finish date for the project yet.\
  It's a large task, and it will take some time to recreate WildStar as it existed at shutdown. However, a great deal of the game has already been implemented, with more being added every day.
* **Is NexusForever the same as Arctium?**\
  ****No, the Arctium WildStar sandbox and server is a separate, closed source project.\
  It is not associated with Nexus Forever, and is being developed independently.\
  However, the two projects do share resources and discoveries.
* **What version of WildStar does NexusForever support?**\
  ****NexusForever supports WildStar version 16042, this was the final patch for WildStar. There are no plans to support other versions at this time.

### Developer

* **What language is NexusForever written in?**\
  ****NexusForever is written in C# utilising the latest version of .NET.
* **Can NexusForever be run on other operating systems such as Linux?**\
  ****NexusForever can be run on any operating system that the .NET runtime supports including many distributions of Linux and OSX.
* **Does NexusForever support Docker?**\
  ****NexusForever does not support Docker, there are no plans to support Docker either officially or via pull request at this time.
* **Can NexusForever be run as a service?**\
  ****NexusForever can be installed as a Window's service or a systemd service on Linux.
* **Can NexusForever be used with other database providers such as SQL Server?**\
  ****Currently no, we only support MySQL and by extension MariaDB.\
  NexusForever used Entity Framework so it would be possible to add support for other database providers further down the line.
* **What's the difference between the master and develop branch?**\
  Master is the latest stable build of NexusForever, features have been around for a while and have some form of testing, this branch is recommended for those wanting to host a NexusForever server or have a local installation.\
  Develop is the latest build of NexusForever with the latest features but may be unstable with little to no testing, this branch is recommended for developers.
