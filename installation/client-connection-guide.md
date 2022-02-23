# Client Connection Guide

{% hint style="info" %}
**Links to the WildStar client will not be provided here.**\
If you still have the WildStar client from the time of shutdown you should be good to follow this guide, make sure it's version 16042!\
Otherwise some Google fu might be in order.
{% endhint %}

### Prerequisites

The current version of the ClientConnector requires the .NET 5.0 runtime, make sure you have this installed.

### Client Connector

Download the latest version of the client for the [GitHub release page](https://github.com/NexusForever/NexusForever/releases).

![Client Connector download from GitHub release page.](<../.gitbook/assets/image (3).png>)

Copy the ClientConnector to the Client64 directory found in the root WildStar client directory.

![Client64 directory which is found in the WildStar client directory.](<../.gitbook/assets/image (2).png>)

Run NexusForever.ClientConnector.exe from the Client64 folder, make sure to run the application as Administrator!

You should get a console window asking you to enter your hostname, this will be provided by the NexusForever server you are attempting to connect to, for a local installation enter localhost or 127.0.0.1 and press enter.

![127.0.0.1 entered for a local NexusForever installation.](<../.gitbook/assets/image (1).png>)

You should now, this is the language of your WildStar client, for English enter en and press enter.

![en entered for a English WildStar client.](../.gitbook/assets/image.png)

The WildStar client should now launch, once at the main menu you should see the connected hostname in the top right corner of the game.

![WildStar client main menu showing connected server.](<../.gitbook/assets/image (4).png>)

You will only need to enter the hostname and language the first time you use the ClientConnector.\
If you need to enter a new hostname or language delete the config.json file in the Client64 folder and launch the ClientConnector again.

### Other Launchers

Some servers use custom launchers, if you have a custom launcher contact the hoster of the NexusForever server for more information.
