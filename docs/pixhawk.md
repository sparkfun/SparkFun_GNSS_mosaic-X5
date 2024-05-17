---
icon: septentrio-logo
---

!!! danger "Important: Read Before Use!"
	!!! warning "ESD Sensitivity"
		The mosaic-X5 module is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.

		??? info "ESD Precaution"
			As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their module.

			<div class="grid cards" markdown>

			- <center>
				<article class="video_cards">
				<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8?si=jOPBat8rzMnL7Uz4&amp;start=26;&amp;end=35;" title="Septentrio: Getting Started Video (playback starts at ESD warning)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
				</article>
				</center>

			-   - The Tri-band GNSS RTK breakout board features ESD protection on the USB-C connector and breakout's I/O:

					- USB data lines
					- I/O PTH pads
					- JST connector's pins
				- The mosaic-X5 module features internal ESD protection to the `ANT_1` antenna input.

			</div>

!!! note
	The mosaic-X5 module has numerous capabilities and a multitude of ways to configure and interface with them. Without regurgitating all the information that is documented in Septentrio's user manuals and videos, we have tried to highlight a good majority of the module's aspects.

	With that said, please feel free to [file an issue](../github/file_issue/#discrepancies-in-the-documentation) if you feel we have missed something that may benefit other users. *(Don't forget to provide us with a link to the documentation and what section the information is located.)*

??? tip "USB Driver"
	sdf

## USB Driver
If users haven't already installed the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) on their computer, they may need to install the USB driver[^1] necessary to recognize and interact with the mosaic-X5 module through the USB interface.

[^1]: On Linux, the standard Linux CDC-ACM driver is suitable.

A Windows USB driver is provided with the mosaic-X5 GNSS receiver.

emulates two virtual serial ports, which can be used as standard COM ports to access the receiver. The Windows USB diver can be installed through the RxTools software suite. On Linux, the standard Linux CDC-ACM driver is suitable. Most terminal emulation programs will make no distinction between virtual and native COM ports. Note that the port settings (baudrate, etc) for virtual serial ports are not relevant, and can be left in their default configuration in the terminal emulation program. When connecting the USB cable to a Windows PC, a new drive appears in the file manager. This drive contains an installer for the USB driver. Running this installer is not needed if you have already installed the RxTools suite. A second drive is created when the receiver is configured as a USB mass-storage device.



<div class="grid cards col-1" markdown>

-   <center>
	<article class="video">
	<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8" title="Septentrio: Getting started with the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

</div>

## Web Interface
When an USB cable is connected, the mosaic-X5 module supports Ethernet-over-USB.


The IP address allocated to the Ethernet-over-USB interface is `192.168.3.1`. That address cannot be changed, so that this feature is only to be used when a single receiver is connected to your computer. 

The default IP for connecting to the Web Interface of a Septentrio receiver is`192.168.3.1`. This IP can be entered in any browser to open a connection to the receiver's Web Interface as shown below.

!!! failure "Invalid IP Address"
	[One of the documentation pages on Septentrio's website](https://customersupport.septentrio.com/s/article/What-is-the-default-IP-address-to-connect-via-WiFi), specifies a default IP address of `192.168.20.1` for the web interface. However, that address is for a WiFi enabled product.

### Sharing Internet Access
By default, the receiver is not allowed to access the Internet over USB. Note that this requires allowing Internet sharing on your computer. The procedure to do so depends on your operating system. For example, on Windows, it involves enabling "Allow other network users to connect through this computer’s Internet connection." in the properties of the adapter providing Internet access. When Internet sharing is enabled, the receiver gets its IP address from a DHCP server on your computer. Depending on your computer’s routing table, it maybe that it is not reachable anymore at `192.168.3.1`.





Hostname: the module hostname is based on the last seven digits of the serial number.  
For example, the hostname of the module shown below is mosaic-X5-3054938.



### Update the Module's Firmware
!!! info "Latest Firmware"
	For the latest firmware released by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources) for the mosaic-X5 module.

<div class="grid cards" markdown>

-   To check for the latest firmware published by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources) for the mosaic-X5 module. Users can click on the button below, to be redirected to the latest firmware for the mosaic-X5.

	<center>
	[:septentrio-logo: Find the Latest Firmware](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources){ .md-button .md-button--primary target="blank" }
	</center>

-   Currently, at the time that this board was released, the firmware for the mosaic-X5 module was *v4.14.0*[^2]. Users can download [**version 4.14.0**](./assets/component_documentation/firmware/mosaic-X5_fwp_4.14.0.zip) of the firmware, by clicking on the button below.

	[^2]:
		For the latest firmware published by Septentrio, please visit their [product page](https://www.septentrio.com/en/products/gps/gnss-receiver-modules/mosaic-x5#resources).<br>
		This is firmware version, was archived at the time that this guide was written. Please do not request for the file to be updated; instead visit the product page to download the latest firmware.

	<center>
	[:octicons-download-16:{ .heart } Download Firmware *(v4.14.0)*](./assets/component_documentation/firmware/mosaic-X5_fwp_4.14.0.zip){ .md-button .md-button--primary target="blank" }
	</center>

</div>

<div class="grid cards col-1" markdown>

-   <center>
	<article class="video">
	<iframe src="https://www.youtube.com/embed/bp8kNbzMl_c" title="Septentrio: How to upgrade the firmware of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

</div>


### GPS Data
Besides logging data with just the ++"LOG"++ button, users can configure/enable the output of data streams and data logging to the SD card through the web interface or RxTools software suite. The videos below illustrate how these features can be operated through the web interface.


<div class="grid cards" markdown>

-   ### Data Logging
	Say...

	<center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/Y9tvOebnoxk" title="Septentrio: How to log data to the SD card of the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   ### Output Data
	Say...

	<center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/ArtePkC58-o" title="Septentrio: How to output NMEA data on the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

</div>

??? info
	<center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/vU6iwJ-ac6A" title="Septentrio: How to log and stream data in NMEA OR SBF format for GNSS/INS receivers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

### RTK Corrections
Without having to setup a personal base station, users can receive RTK corrections through the internet from 3rd-party services. Link


<div class="grid cards" markdown>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/bUt8cL9Ue1Y" title="Septentrio: Share internet connection with your GNSS / GPS receiver over USB" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/UVUVXpA8rB4" title="Septentrio: How to receive corrections over an IP connection" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/aAPoRpSR0tY" title="Septentrio: How to receive corrections via NTRIP on the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

</div>



### Videos
Users can find other instruction videos on [Septentrio's YouTube Channel](https://www.youtube.com/channel/UCrA9wMw1y1f-KeOnnhq4lrA/)

https://www.youtube.com/playlist?list=PLUxLg2_PvvdE0e2i2std6XyPnF6UdecAD

https://www.youtube.com/watch?v=bp8kNbzMl_c&list=PLUxLg2_PvvdHZ73CnfhS7ZePIIIUR7bON


<div class="grid cards" markdown>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/SzI0skGHKEw" title="Septentrio: Anti-jamming feature test-run" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/H6uVVEJ5U5w" title="Septentrio: How to activate Wideband Interference Mitigation" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/Ib_B_KcfmPs" title="Septentrio: How to use the spectrum plot" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

</div>



<div class="grid cards" markdown>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/j_zHbl99FsI" title="Septentrio: How to reset a receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/D-iqzQnDbWw" title="Septentrio: How to copy the configuration from one to another receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/2XizOW3Dzzk" title="Septentrio: How to monitor the CPU of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/9qN6b1JC3uE" title="Septentrio: How to generate and save a diagnostic report of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/bp8kNbzMl_c" title="Septentrio: How to upgrade the firmware of a Septentrio receiver" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/WU8MYrDALsE" title="Septentrio: How to log SBF data for support for Septentrio's GNSS/ GPS receivers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/vU6iwJ-ac6A" title="Septentrio: How to log and stream data in NMEA OR SBF format for GNSS/INS receivers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

-   <center>
	<article class="video_cards">
	<iframe src="https://www.youtube.com/embed/WU8MYrDALsE" title="Septentrio: How to log SBF data for support for Septentrio's GNSS/ GPS receivers" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	</center>

</div>
