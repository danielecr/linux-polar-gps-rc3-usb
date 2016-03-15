# linux-polar-gps-rc3-usb
Polar RC3 GPS device driver for linux. Try to make it working

http://desowin.org/usbpcap/

this is for capturing USB traffic between my RC3 and windows driver, while uploading to polarpersonaltrainer.com website.

Polar RC3 USB Identifier is 0da4:0006 (idVendor:idProduct)

# Howto?

usbpcap Terminal application let me choose one USB interface from which capture all traffic, and store it in a .pcap file.
Then I can open it in wireshark ( https://www.wireshark.org/ ) to analyze it.

All traffic means ALL traffic. First I have to filter it. To do so I follow this steps:

1. find bus_id and device address. How? filter by usb.idVendor == 0x0da4 (at least one time the OS must ask DEVICE Descriptor, and the device must reply with its identifiers)
2. filter by device_address. (it is the stricter option, of course)

So. I upload the .pcap file. device_address is 5

rc3polar.pcap


# Related

https://github.com/samop/Polar-Flowlink-linux/ here there is a project for understanding the polar format for workouts

here https://code.google.com/archive/p/polarhrm/ are some other references
