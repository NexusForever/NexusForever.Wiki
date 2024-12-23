# Server Install Guide (Windows)

{% hint style="info" %}
This guide is intended for advanced users and it makes assumptions that you have knowledge on the technologies mentioned.
{% endhint %}

This guide will help you setup and install the NexusForever server on Windows.

### Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/downloads/) with [.NET 6](https://dotnet.microsoft.com/download/dotnet/6.0) and C# 9.0
- [MySQL](https://www.mysql.com) or [MariaDB](https://mariadb.org) server
- WildStar 16042 client

{% hint style="info" %}
NexusForever does not distribute a client. You will need to find your own clean WildStar 16042 client on the internet.
{% endhint %}

### Branches

| Branch                                                                       | Description        | Recommended       |
| ---------------------------------------------------------------------------- | ------------------ | ----------------- |
| [Master](https://github.com/NexusForever/NexusForever/tree/master)           | Stable             | For newer players |
| [Game Rework](https://github.com/NexusForever/NexusForever/tree/game_rework) | Active development | For contributors  |
| [Develop](https://github.com/NexusForever/NexusForever/tree/develop)         | Currently Inactive |

{% hint style="info" %}
For more detailed information about the branches visit the GitHub repository. By clicking any of the branches names above. Default and recommend for such is Game Rework.
{% endhint %}

### Building your Server and Tools

{% hint style="info" %}
Precompiled releases and binaries can also be found on the GitHub repository.
{% endhint %}

Switch to the [Game Rework](https://github.com/NexusForever/NexusForever/tree/game_rework) branch for all the newest features.\
The build process for NexusForever is straightforward, with the solution loaded in Visual Studio you only need to restore the NuGet packages and build the solution.

---

For more explicted instructions follow below:

1. You can download the shown branched above (we recommend Game Rework) from our [GitHub repository](https://github.com/NexusForever/NexusForever/tree/game_rework) from the releases on the right or you can clone this if you have any Git Client. Like Github Desktop or Git Bash.

If you use a Git Client, this will allow you to update your Branch without needing to manually download it everytime.

2. Inside of your download `NexusForever` you will have a folder called `Source`, look around and open `NexusForever.sln`.

If you don't have windows `Show file name extensions` than the file only will show as `NexusForever` but your folder columns should tell you the type `Visual Studio Solution`.

3. You will have 2 folders on the left side one called `Client` and another called `Server`, right click each one of them and click `Build`.

The `Client` content will be use to extract the needed information refering to the world and content of it, explained below, and the `Server` has to do with the Authentication and everything you see in-game (NPCs, Quests, etc...)

### Base Map Files

Base maps are generated files used by NexusForever that contain various bits of information about the maps in Wildstar including grid, zone and terrain height information.

The base maps can be generated using the MapGenerator which is included as part of the Visual Studio solution.\
The MapGenerator can take many parameters but the key ones are the path to your WildStar clients patch folder and the mode, using the generation mode will generate the base maps.

```
NexusForever.MapGenerator --i "C:\Program Files (x86)\NCSOFT\WildStar\Patch" --g
```

Once the process completes you'll find a folder called map in the same folder as the MapGenerator executable containing many .nfmap files, copy this folder to your NexusForever world server build folder.

---

For more explicted instructions follow below:

1. Upon finishing building our `Client` tools. Inside of `source` folder where we opened the Visual Studio file, there should be a folder called `NexusForever.MapGenerator` and follow the path down. `NexusForever.MapGenerator\bin\Debug\net8.0`. At this point you will open `CMD` (Command Prompt).

The easiest way to do this is looking at the path of the current folder (like is a browser's link bar) and clicking it once, you will have all the text selected, just type `CMD` and press ENTER, `CMD` will open on that folder!.

2. You will type the following `NexusForever.MapGenerator --i "WhereEverIsYourClientInstalledPath" --g` than press ENTER. **DO NOT CLOSE THE WINDOW WHEN IS DONE**

Example: `NexusForever.MapGenerator --i "C:\Program Files (x86)\NCSOFT\WildStar\Patch" --g`, upon pressing ENTER, it will start extracting the map information from the client to your current folder under `map` folder. This may take a while depending on your hardware.

### Game Table Files

WildStar uses client side game tables (similar to dbc or db2 files from World of Warcraft) to supply the client with various bits of information about items, quest, spells, etc..., NexusForever utilises this information as well.

We can use the MapGenerator from the previous step to extract the game tables from the client, the only difference is the mode, using the extraction mode will extract the game tables.

```
NexusForever.MapGenerator --i "C:\Program Files (x86)\NCSOFT\WildStar\Patch" --e
```

Once the process completes you'll find a folder called tbl in the same folder as the MapGenerator executable containing many .tbl files and one or more .bin localisation files depending on the amount of client languages you have installed, copy this folder to your NexusForever world server build folder.

---

For more explicted instructions follow below:

1. While still having the window still open, we will run same command with a different parametre. You will type the following `NexusForever.MapGenerator --i "WhereEverIsYourClientInstalledPath" --e` than press ENTER.

Example: `NexusForever.MapGenerator --i "C:\Program Files (x86)\NCSOFT\WildStar\Patch" --e`, upon pressing ENTER, it will start extracting the table information from the client to your current folder under `tbl` folder. This shouldn't take as long as the previous one did.

2. Upon completion, make sure you copy the folders `map` and `tbl`.

3. Go back to `source` and find the folder `NexusForever.WorldServer` and go down the path `NexusForever.WorldServer\bin\Debug\net8.0` and paste the folders `map` and `tbl` in there.

### Configuration Files

In the build folders for the 3 separate servers you'll find a configuration JSON file:

- StsServer.example.json
- AuthServer.example.json
- WorldServer.example.json

Copy or rename these files by removing the .example extension.\
Update the MySQL information in both these configuration files to match the 3 databases created earlier.

---

For more explicted instructions follow below:

1. `NexusForever` uses `dotnet` as their way to start the services. So while we are here (`NexusForever.WorldServer\bin\Debug\net8.0`) we will create a .bat (batch) file example: `WorldRun.bat`. And you will open that file with you prefered text editor (Notepad, Notepad++, Visual Studio Code, etc...) and you will add the following:

```
@ECHO OFF
dotnet NexusForever.WorldServer.dll
```

If you don't have windows `Show file name extensions`, I would recommend it enabling because you just type the name of the file . type (extension) of the file. Do a quick google search.

2. Right Click the new .bat (batch) file you've created (example: `WorldRun.bat`) and `Send to` choose `Desktop`, this will allow you to have all the server shortcuts in one place.

3. In the same folder you will have a file called `WorldServer.example.json` just copy and paste it in the same place you're, you will have now a `WorldServer.example.json - Copy` just rename that `-copy` file into the following: `WorldServer.json`.

4. Go back to `Source` and repeat steps above for `NexusForever.StsServer` and `NexusForever.AuthServer`.

If you followed the example above for the .bat (batch) file name. `STSRun.bat` and `AuthRun.bat` should have the following text in their respective batch file:

- `STSRun.bat` should have: `dotnet NexusForever.StsServer.dll`
- `AuthRun.bat` should have: `dotnet NexusForever.AuthServer.dll`

Don't forget to make those shortcuts and send them to your desktop!

Same applies for the `.json` file:

- `StsServer.example.json` copy and renamed to: `StsServer.json`
- `AuthServer.example.json` copy and renamed to: `AuthServer.json`

### Database Creation

1. Assuming you don't have a Database service running or installed, install and note down the user and password you used on the instalation of MySQL. Tends be Username: `root` and Password: `WhateverYouWantDoNotUseRoot`.

Don't change the name of the service and don't change the port number, if you're not-experienced with this.

2. Upon completing the instalation and setup, you may or not be required to restart your computer or machine, check your Windows' `Services`, and search down the list for `MySQL` or the name you gave it when installing.

You can check your `Services` by pressing the `Windows` button (on the bottom left of your screen or on your keyboard) and you can type `Services` and it will appear with 2 cog-wheels, click on it.

3. If it's says `MySQL` (or the name you called it) is `Running` the Database Service is running. Proceed to acquire a database client of your choice.

- MySQL CLI (comes with MySQL) but it's like the CMD, not easy for beginners.
- [HeidiSQL](https://www.heidisql.com/download.php), has a User Interface, it's good for beginners.
- [MySQL Workbench](https://www.mysql.com/downloads/), has a User Interface, not easy for beginners.

4. Open the Database client you choose and login to your MySQL or MariaDB. with the following:

- Hostname / IP: `127.0.0.1`
- User: `WhateverYourUsernameYouChoose`
- Pass: `WhateverPasswordYouChoose`
- Port: `3306`

Example above is from HeidiSQL

5. Upon connecting to your database do a quick google `(My Client) how to create users` and see how you create a user.

6. Create a user with the following username as `nexusforever` and password as `nexusforever`.

### Database Population

NexusForever uses Entity Framework migrations which are automatically managed during world server startup.\
Running the world server for the first time will create the databases and tables.

---

For more explicted instructions follow below:

1. Go to your desktop where you have those 3 shortcuts we made before `STS, Auth and World` and run them.

2. In your `NexusForever: World Server (DEBUG)` window. the following:

```
account create TheNameOfYourAccount ThePasswordYouWant PermissionLevel
```

PermissionLevel refers to the `role` value.

Example:

```
account create NexusAdmin MyPasswordVeryGood 3
```

From `role` table:
| id | name |
| --- | --- |
|1 | Player |
|2 | GameMaster |
|3 | Administrator |
|4 | Console |
|5 | WebSocket |

### And we are all done.
