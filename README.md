# iot-edge-opc-publisher-nodeconfiguration

This .NET Core application allows to configure [OPC Publisher](https://github.com/Azure/iot-edge-opc-publisher) using IoTHub direct method calls.


## Features

The application is/can:
* Read the current node configuration from the OPC Publisher device/module specified by id/iothubdevicename and im/iothubmodule name.
* Save the current node configuration in a backup file.
* Purge the current node configuration of OPC Publisher.
* Send the specified new node configuration to OPC Publisher.


## Getting Started

### Prerequisites

The application required .NET Core and OPC Publisher deployed either standalone or as IoT Edge module.

### Installation

You need to compile the solution with Visual Studio and then run it.

### Quickstart

The application supports several command line options to control its functionality. 

Here the usage output:
        OPC Publisher node configuration
        Current directory is: <current directory>
        Log file is: <hstname>-publishernodeconfig.log
        Log level is: info
        
        Usage: iot-edge-opc-publisher-configuration.exe [<options>]
        
        OPC Publisher configuration tool.
        To exit the application, just press CTRL-C while it is running.
        
        Options:
          -h, --help                 show this message and exit
              --ic, --iotHubConnectionString=VALUE
                                     IoTHub owner or service connectionstring
              --id, --iothubdevicename=VALUE
                                     IoTHub device name of the OPC Publisher
              --im, --iothubmodulename=VALUE
                                     IoT Edge module name of the OPC Publisher which
                                       runs in the IoT Edge device specified by id/
                                       iothubdevicename
              --pc, --purgeconfig    remove all configured nodes before pushing new ones
              --bf, --backupfile=VALUE
                                     the filename to store the existing configuration
                                       of OPC Publisher
                                       Default: './<hostname>-publishernodeconfig.bak'
              --nc, --nodeconfigfile=VALUE
                                     the filename of the node configuration to be set
              --lf, --logfile=VALUE  the filename of the logfile to use
                                       Default: './johanngnb-publishernodeconfig.log'
              --ll, --loglevel=VALUE the loglevel to use (allowed: fatal, error, warn,
                                       info, debug, verbose).
                                       Default: info

