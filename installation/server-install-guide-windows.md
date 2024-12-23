# Server Install Guide (Windows)

{% hint style="info" %}
This guide is intended for advanced users and it makes assumptions that you have knowledge on the technologies mentioned.
{% endhint %}

This guide will help you setup and install the NexusForever server on Windows.

### Prerequisites

* [Visual Studio 2022](https://visualstudio.microsoft.com/downloads/) with [.NET 6](https://dotnet.microsoft.com/download/dotnet/6.0) and C# 9.0
* [MySQL](https://www.mysql.com) or [MariaDB](https://mariadb.org) server
* WildStar 16042 client

{% hint style="info" %}
NexusForever does not distribute a client. You will need to find your own clean WildStar 16042 client on the internet.
{% endhint %}

### Branches

| Branch | Description | Recommended
| --- | --- | --- |
| [Master](https://github.com/NexusForever/NexusForever/tree/master) | Stable | For newer players |
| [Game Rework](https://github.com/NexusForever/NexusForever/tree/game_rework) | Active development | For contributors |
| [Develop](https://github.com/NexusForever/NexusForever/tree/develop) | Currently Inactive | 

{% hint style="info" %}
For more detailed information about the branches visit the GitHub repository. By clicking any of the branches names above. Default and recommend for such is Game Rework.
{% endhint %}

### Building

{% hint style="info" %}
Precompiled releases and binaries can also be found on the GitHub repository.&#x20;
{% endhint %}

Switch to the develop branch for all the newest features.\
The build process for NexusForever is straightforward, with the solution loaded in Visual Studio you only need to restore the NuGet packages and build the solution.

### Assets

#### Base Map Files

Base maps are generated files used by NexusForever that contain various bits of information about the maps in Wildstar including grid, zone and terrain height information.

The base maps can be generated using the MapGenerator which is included as part of the Visual Studio solution.\
The MapGenerator can take many parameters but the key ones are the path to your WildStar clients patch folder and the mode, using the generation mode will generate the base maps.

```
NexusForever.MapGenerator --i "C:\Program Files (x86)\NCSOFT\WildStar\Patch" --g
```

Once the process completes you'll find a folder called map in the same folder as the MapGenerator executable containing many .nfmap files, copy this folder to your NexusForever world server build folder.

#### Game Table Files

WildStar uses client side game tables (similar to dbc or db2 files from World of Warcraft) to supply the client with various bits of information about items, quest, spells, etc..., NexusForever utilises this information as well.

We can use the MapGenerator from the previous step to extract the game tables from the client, the only difference is the mode, using the extraction mode will extract the game tables.

```
NexusForever.MapGenerator --i "C:\Program Files (x86)\NCSOFT\WildStar\Patch" --e
```

Once the process completes you'll find a folder called tbl in the same folder as the MapGenerator executable containing many .tbl files and one or more .bin localisation files depending on the amount of client languages you have installed, copy this folder to your NexusForever world server build folder.

### Configuration Files

In the build folders for the 3 separate servers you'll find a configuration JSON file:

* StsServer.example.json
* AuthServer.example.json
* WorldServer.example.json

Copy or rename these files by removing the .example extension.\
Update the MySQL information in both these configuration files to match the 3 databases created earlier.

### Database Population

NexusForever uses Entity Framework migrations which are automatically managed during world server startup.\
Running the world server for the first time will create the databases and tables.



\




