# Marvelmind UDP C library and example #

### About the library ###

Marvelmind UDP C library provides an example of receiving location and other data from Marvelmind Super-Modem or from Dashboard via UDP in supported operating systems:

* Microsoft Windows
* GNU/Linux (including Raspberry Pi)
* Mac OS X

### Building the example ###

To build the example on GNU/Linux or another *nix-OS you need to have installed GCC. Then unpack the archive, change directory to unpacked library and run make in console. Then you can execute ./marvelmind_udp_c to watch received UDP data. 

If you want to build a project for MS Windows, you may use integrated development environment (such a MS Visual Studio, Code::Blocks etc.): create empty console project and add 3 source files (udp_example.c, udp_marvelmind.h, udp_marvelmind.c) into the project and run build. You may need to change the project settings to successfully build it.
<br />
Notes about using the example: <br />
1. You should achieve a good tracking before using the example. <br />
Please refer to operating manual for details: [https://marvelmind.com/pics/marvelmind_navigation_system_manual.pdf](https://marvelmind.com/pics/marvelmind_navigation_system_manual.pdf) <br />
2. Streaming UDP data from the Dashboard should be enabled via menu 'Settings/UDP settings'. Set the checkbox 'UDP stream output' and specify destination IP address and port. <br/>
3. Streaming UDP data from the Super-Modem should be enabled in Super-Modem's settings in the dashboard. 
Enable 'Wi-Fi' setting in 'Wi-Fi/UDP settings' group of settings, specify Wi-Fi network name and password, specify 'UDP destination IP address' and 'UDP destination port'.

### Command line options of the example ###

 ./marvelmind_udp_c 0 127.0.0.1 49100    - listens UDP port 49100 for incoming UDP data
 ./marvelmind_udp_c 48 192.168.0.100 49200    - sends request to IP address 192.168.0.100, port 49200 to get location data for mobile beacon n48

or for Microsoft Windows:

 marvelmind_udp.exe_c 0 127.0.0.1 49100    - listens UDP port 49100 for incoming UDP data
 marvelmind_udp_c.exe 48 192.168.0.100 49200    - sends request to IP address 192.168.0.100, port 49200 to get location data for mobile beacon n48



