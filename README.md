![indicator-sysmonitor](https://user-images.githubusercontent.com/9158844/37069705-90f272a2-21c5-11e8-806f-92b20cbf47ae.png)


Indicator-SysMonitor - v0.8.3
===================
An Application Indicator showing cpu temperature, memory, network speed, disk IO, cpu usage, public IP address and internet connection status .

Works with Unity, Xubuntu, Gnome-Shell + app-indicator extension together with any other desktop environments that support AppIndicators.

Also works with the Budgie-Desktop

Offers the possibility to run your own command and display its output.

----

## Custom scripts

Create your own scripts (for example in bash).  Give the script execute permission (chmod +x scriptname)

A script must output one line of text - e.g. using "echo" in bash

The indicator can change the icon being displayed by recognising the output of a sensor "USE_ICON:full_path_to_.svg"

## Set the display order of the indicator

To force the indicator to appear on the left-side of all indicators you must use a override file as described here:

 - http://askubuntu.com/questions/26114/is-it-possible-to-change-the-order-of-icons-in-the-indicator-applet

----

Installation - Budgie-Desktop:

On Budgie-Remix and 'buntu with Budgie-Desktop PPA - manual installation

    sudo apt-get install python3-psutil curl git
    git clone https://github.com/czysoft/indicator-sysmonitor.git
    cd indicator-sysmonitor
    sudo make installbudgie
    budgie-panel --replace &
    
    Then use Raven to add the "Panel Sys Monitor" applet

Installation - App Indicator based desktops:

On Ubuntu and derivatives - manual installation


    sudo apt-get install python3-psutil curl git gir1.2-appindicator3-0.1
    git clone https://github.com/czysoft/indicator-sysmonitor.git
    cd indicator-sysmonitor
    sudo make install
    nohup indicator-sysmonitor &
    
To remove:

    cd indicator-sysmonitor
    sudo make uninstall


Changelog:
 
 - v0.8.3 - add disk IO Infomation
