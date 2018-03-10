# How to connect wifi via command line interface (terminal) on linux?
`nmcli d wifi connect [wifi_name] password [wifi_pass] ifname [interface]`

For example :
  Wifi name = carlo
  Wifi pass = gaza
  Interface = wlan0
`nmcli d wifi connect carlo password gaza ifname wlan0`

You can get the interface name with command `ifconfig`
