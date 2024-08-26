BluetoothCommunicator example
This repository contains an open source sample application of the BluetoothCommunicator library.
The library, using Bluetooth Low Energy, allows you to communicate in P2P mode between two or more android devices in a very simple way.


The application is a Bluetooth chat, when the app is open in the first screen (search) it discovers nearby devices with the app open in the same search screen and shows them in a list containing the code number name of the phones (the name is customizable in the library, but not in the app).

When the user clicks on one of the names the app sends a connection request to that phone and if the latter accepts it, both apps start the chat screen where the two devices can send text messages (the library can send also raw data) to each other.

When one of the user press the back button the connection stops and the apps will return to the search screen.


  

If you want to see the demo app in action you can download it from here.


BluetoothCommunicator library
BluetoothCommunicator is a library originally created for RTranslator but can be used in any more generic case where a P2P communication system is needed between two or more android devices (approximately up to 4 with a direct connection between all devices, even more with a star structure), for an example app see this repository or RTranslator.

Features
BluetoothCommunicator automatically implements (they are active by default):

reconnection in case of temporary connection loss.

reliable message sending:

splitting and rebuilding of long messages.

sending messages with a queue in order to always send the messages even in case of connection problems (they will be sent as soon as the connection is restored) and in the right order.
