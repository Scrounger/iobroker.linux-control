![Logo](admin/linux-control.png)
# ioBroker.linux-control

[![NPM version](http://img.shields.io/npm/v/iobroker.linux-control.svg)](https://www.npmjs.com/package/iobroker.linux-control)
[![Downloads](https://img.shields.io/npm/dm/iobroker.linux-control.svg)](https://www.npmjs.com/package/iobroker.linux-control)
![Number of Installations (latest)](http://iobroker.live/badges/linux-control-installed.svg)
![Number of Installations (stable)](http://iobroker.live/badges/linux-control-stable.svg)
[![Dependency Status](https://img.shields.io/david/Scrounger/iobroker.linux-control.svg)](https://david-dm.org/Scrounger/iobroker.linux-control)
[![Known Vulnerabilities](https://snyk.io/test/github/Scrounger/ioBroker.linux-control/badge.svg)](https://snyk.io/test/github/Scrounger/ioBroker.linux-control)

[![NPM](https://nodei.co/npm/iobroker.linux-control.png?downloads=true)](https://nodei.co/npm/iobroker.linux-control/)

**Tests:**: [![Travis-CI](http://img.shields.io/travis/Scrounger/ioBroker.linux-control/master.svg)](https://travis-ci.org/Scrounger/ioBroker.linux-control)

## linux-control adapter for ioBroker
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VWAXSTS634G88&source=url)

Controlling Linux devices and get information about your system

**This adapter uses Sentry libraries to automatically report exceptions and code errors to the developers.** For more details and for information how to disable the error reporting see [Sentry-Plugin Documentation](https://github.com/ioBroker/plugin-sentry#plugin-sentry)! Sentry reporting is used starting with js-controller 3.0.

## Configuration

### General
![General](docs/en/img/general.png)

|setting|description|
|-------|-----------|
|datapoint id|id under which all datapoints are to be stored|
|IP|IP address of your linux device|
|Port|SSH Port of your linux device|
|polling interval|polling interval in minutes|
|user|ssh user for login|
|password / passpharse|ssh password for login or passpharse if you use a rsa key|
|use Sudo| using sudo |
|rsa key|path and filename of your rsa key. Access rights must be available!|
|timeout|connection timeout|

### Datapoints
![Datapoints](docs/en/img/datapoints.gif)

The adapter creates predefined datapoints with information and the possibility to control the Linux device. These can be selected here.
In addition, for each individual host, individual data points or entire channels can be placed on the blacklist by drag & drop so that they are not created for the host.

**Due to the many different Linux distributions this feature is only tested with Debian 10, Ubuntu 18 / 20 LTS!**

### Services
![Services](docs/en/img/services.png)

If the retrieval of services under datapoints is activated, you can define here per host for which services only information should be retrieved.

### Folders
![Folders](docs/en/img/folders.png)

Here you can retrieve information about the size of folders, count of the files included in these folders and the timestamp of the last change in this folder.

|setting|description|
|-------|-----------|
|Host|Host which should be used|
|datapoint id|id under which all datapoints are to be stored|
|Path|path of the folder|
|filename pattern|pattern for files names which should be regonized.|
|Unit|Unit for size|
|decimal places|decimal places|
|count of files|create datapoint for count of files|
|last change|create datapoint for timestamp of the last change in this folder|

### Custom Commands
![Custom Commands](docs/en/img/myCommands.png)

Here, very individual commands can be defined and then written to your own defined data points.
It is important that the retrieved data is transmitted in the correct type! The type must then be configured accordingly.


## Changelog

<!--
    Placeholder for the next version (at the beginning of the line):
    ### __WORK IN PROGRESS__
-->

### __WORK IN PROGRESS__
* (Scrounger) bug fixes

### 0.2.2 (2020-08-09)
* (Scrounger) bug fixes

### 0.2.1 (2020-08-09)
* (Scrounger) bug fixes

### 0.2.0 (2020-08-08)
* (Scrounger) optional folder datapoints for count of files and last change added
* (Scrounger) enable options for hosts, folders and user commands added
* (Scrounger) using sudo implemented
* (Scrounger) type array for user commands added
* (Scrounger) ignore whole datapoints node by using drag and drop 
* (Scrounger) error handling for user commands improved
* (Scrounger) Sentry implemented
 

### 0.1.0 (2020-05-20)
* (Scrounger) added datapoints blacklist configurable for each host individually
* (Scrounger) added poll interval configurable for each host individually
* (Scrounger) configuration bug fixes

### 0.0.3 (2020-05-16)
* (Scrounger) added services whitelist configurable for each host individually

### 0.0.1
* (Scrounger) initial release

## License
MIT License

Copyright (c) 2020 Scrounger <scrounger@gmx.net>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.