# Win10_BrightnessSlider
this app puts a Monitor Brightness icon to on Taskbar Tray. So you can access it with 1 click.
targeting laptops. 

* trying to fix: **[Please Feedback Here](https://github.com/blackholeearth/Win10_BrightnessSlider/issues/16)**  fallback mode doesn't handle management not supported exception.  

* **tested on** win10 build 10240 x64.
* **tags:** Windows 10 MONITOR Brightness Slider Icon on Taskbar Tray
* **Note For Developers**  : code version is  first working version (maybe 1.01). but **executable is always up to date**

**Download Link**  [Click Here To Download](https://github.com/blackholeearth/Win10_BrightnessSlider/blob/master/Win10_BrightnessSlider/bin/Debug/Win10_BrightnessSlider.exe?raw=true)

#### Features

* Supports ddc/ci monitors
* Seperate Sliders For Multiple Monitors
* Volume like Slider to Change Monitor Brightness
* Option to Run At Startup
* Ability to *"Rescan Monitor"* after a Monitor Plugged in/out

#### ScreenShots

![alt text](https://github.com/blackholeearth/Win10_BrightnessSlider/blob/master/ss1.jpg?raw=true)

![alt text](https://github.com/blackholeearth/Win10_BrightnessSlider/blob/master/ss2.jpg?raw=true)

![alt text](https://github.com/blackholeearth/Win10_BrightnessSlider/blob/master/ss3.jpg?raw=true)


 
#### If you get error "Not Supported" 
#####  now there is ddc/ci , version1.02 gracefully fallback to ddc/ci mode  

1) paste this  windows powershell 
   
   $monitor = Get-WmiObject -ns root/wmi -class wmiMonitorBrightNessMethods$monitor.WmiSetBrightness(80,10) 
  
   if the code above gives error. then, there is nothing i can do . 
   because, WmiSetBrightness is provided by microsoft.  please dont open issue about this.
    
2) try install/update your graphic driver  

 
#### ChangeLog
v1.04
* added: author page to  menu item  that shows version no.
* trying to fix: fallback doesnt handle management not supported exception.

v1.02

* added: seperately change brightness of multiple monitors.
* added: supports setting Brighness on ddc/ci Monitors(at startup, it may show -1,  )
* fixed: slider showing itself on second screen onhide 
* fixed: popup stays under taskbar, if taskbar is autoHiding  

v1.01

* fixed: slider wasn't positioning itself according to taskbar position (Top Or Bottom Or Left Or Right of Screen)

