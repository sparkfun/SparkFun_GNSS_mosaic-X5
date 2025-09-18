---
icon: fontawesome/solid/computer
---

!!! danger "Important: Read Before Use!"
	!!! warning "ESD Sensitivity"
		The mosaic-X5 module is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.

		??? info "ESD Precaution"
			As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their module.

			- The Tri-band GNSS RTK breakout board features ESD protection on the USB-C connector and breakout's I/O:
				- USB data lines
				- I/O PTH pads
				- JST connector's pins
			- The mosaic-X5 module features internal ESD protection to the `ANT_1` antenna input.


			<div class="grid cards" markdown>

			<div markdown>

			<article class="video-500px" style="margin: auto;" markdown>
			<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8?si=jOPBat8rzMnL7Uz4&amp;start=26;&amp;end=35;" title="Septentrio: Getting Started Video (playback starts at ESD warning)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
			</article>

			</div>

			-   <a href="https://www.sparkfun.com/products/25572">
				<figure markdown>
				![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/6/1/2/7/TOL-25572-Anti-Static-Wrist-Strap-Feature.jpg)
				</figure>		

				---

				**iFixit Anti-Static Wrist Strap**<br>
				TOL-25572</a>

			</div>

!!! note
	The mosaic-X5 module has numerous capabilities and a multitude of ways to configure and interface with them. Without regurgitating all the information that is documented in Septentrio's user manuals and videos, we have tried to highlight a good majority of the module's aspects.

	With that said, please feel free to [file an issue](../github/file_issue/#discrepancies-in-the-documentation) if you feel we have missed something that may benefit other users. *(Don't forget to provide us with a link to the documentation and what section the information is located.)*


## RxTools Software Suite

!!! tip
	Even if you aren't necessarily interested it, we highly recommend that users install the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) before plugging in their board. For Windows PCs, it also includes the USB driver for the module that enables the Ethernet-over-USB support and virtual `COM` ports.

Users should install the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) on their computer to interact with the mosaic-X5 module through the USB interface. The software package includes the USB-IP driver[^1] necessary to recognize the board as an ethernet device on Windows PCs (1).
{ .annotate }

1. On Linux, the standard Linux CDC-ACM driver is suitable.

[^1]: On Linux, the standard Linux CDC-ACM driver is suitable.


<article style="text-align: center;" markdown>
[:octicons-download-16:{ .heart } Download the RxTools Software from Septentrio](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools){ .md-button .md-button--primary target="blank" }
</article>

??? info "System Requirements[^2]"

	=== "Operating Systems"
	
		* Windows 7
		* Windows 8
		* Windows 10
		* Fedora 23 *(or later)* using Qt technology.
			* The standalone tools (except `bin2asc`) will run on older distributions.
	
	=== "Hardware Requirements"
		The minimal hardware requirements *(1Hz update[^3])*:
	
		* CPU: 1 GHz processor
		* RAM: 1 GB RAM
		* Screen Resolution: 1024×768 or higher resolution

	[^2]: The system requirements and installation instructions are from the RxTools *v22.1.0* user manual. This information may change in later iterations of the software suite. Please refer to the user manual *(of the version you are utilizing)* for the most accurate information.
	[^3]: Higher data rates will require higher CPU speed and more memory capacity.


??? info "Installation Instructions[^2]"

	=== "Windows"
		Users can install RxTools software suite by running the installation executable[^4](1), located in the `RxTools\windows` directory of the downloaded `*.zip` file[^5]. During the installation process, users will be notified if a previous version of RxTools is already installed then that the previous version will be uninstalled. Next, users will need to provide an installation directory for the RxTools software suite. Users will then select which of the following applications[^6] are installed:
		{ .annotate }

		1. For RxTools v22.1.0, the installation filename is `RxTools_22_1_0_Installer.exe` for Windows PCs.

		<!-- Create Break from Annotation (list won't render without comment)-->

		<div class="grid" markdown>

		<div markdown>

		* RxControl
		* SBF Converter
		* SBF Analyzer
		* RxLogger

		</div>

		<div markdown>

		* RxUpgrade
		* RxDownload
		* RxPlanner

		</div>

		<div markdown>

		* Data Link
		* RxAssistant
		* RxLauncher

		</div>

		</div>


	=== "Linux[^1]"
		!!! warning
			It is recommended that users **<span style="color:red">NOT</span>** install RxControl as `root`, for security reasons and to avoid installation overwrites of other system settings. To make RxTools available to more than one user, provide a shared installation directory.

		Users can install RxTools software suite by running the installation binary[^4](1), located in the `RxTools/linux-i386/` directory of the downloaded `*.zip` file[^5]. During the installation, users will be prompted for an installation directory. If there are any previous installations of RxControl, please use a different directory to avoid conflicts.
		{ .annotate }

		1. For RxTools v22.1.0, the installation filename is `RxTools_22_1_0_Installer.bin` for Linux.

		??? info "Permission Settings"
			Once installed, users may need to reconfigure their permission settings:

			<div class="annotate" markdown>

			* RxTools will need rights to access the `/dev/ttyS*` serial ports.

				* To access the serial ports, users must be part of the `uucp` and `lock` groups (1). This can be configured by editing the `/etc/group`[^7] file and adding the username to the lines defining the `uucp` group and the `lock` group.

					For example, when adding the user `jsmith` to the `uucp` group, users would modify the `/etc/group` file as shown below:

					```bash
					{--uucp:x:14:uucp--} # (2)!
					{++uucp:x:14:uucp,jsmith++} # (3)!
					```

				* On Linux machine administered centrally on a local network, ask your system administrator to be included in the `uucp` and `lock` groups.
			* RxTools also needs read/write (`rw`) access(4) to the `/dev/ttyS*` serial ports.

				* Users can change the permissions with the `chmod`[^8] command:

					```bash
					chmod 660 /dev/ttyS<add port> # (5)!>
					```

			</div>

			1. On most Linux operating systems, the `/dev/ttyS*` devices are owned by `root` and belong to the `uucp` group with read/write (`rw`) access. Additionally, the devices are normally locked by writing a file in the `/var/lock/` directory, with the same permissions.
			2. Remove
			3. Replace with this line
			4. By default, users will normally have read/write (`rw`) access to the `/dev/ttyS*` serial ports.
			5. where users must specify the port number<br>*e.g. `/dev/ttyS0` might be port `COM1`*

			!!! note
				In order for these changes to take effect, users must update their environment by logging out and back in.

				Be aware that the X-session has to be restarted as well. On most systems, this can be done by pressing the key combination ++ctrl++ + ++alt++ + ++backspace++

		??? info "64-bit OS"
			In order to run the RxTools on a 64-bit Linux operating system, users might to install the 32-bit version of the `C` standard library.

			* For Fedora installations, this is the `glibc.i686` package.
			* The equivalent for Debian(/Ubuntu) installations is the `ia32-libs` package.

	[^4]: Users will need administrative privileges to install the RxTools software.
	[^5]: Users may need to extract the RxTools installation files from the downloaded, compressed file.
	[^6]: Please see the release notes for the issues and limitations of the RxTools applications.
	[^7]: Requires c privileges.
	[^8]: Changing these permissions also requires `root` privileges.


## USB Driver
=== "Windows"
	If users haven't already installed the [RxTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) on their Windows PC, they will need to install the USB driver[^1] necessary to recognize and interact with the mosaic-X5 module through the USB interface.

	A Windows USB driver for the mosaic-X5 can be installed through two methods:

	<div class="annotate" markdown>

	* RxTools Software Suite (1)
	* mosaic-X5 GNSS Receiver Module (2)

	</div>

	1. The driver is installed during the installation process.
	2. The installation file for the Windows USB driver will be available from the mass-storage device when the board is initially connected to the computer.

	Once installed, the driver emulates two virtual serial ports, which can be accessed as standard `COM` ports to the receiver.

	??? tip "Terminal Emulators"
		Most [terminal emulation programs](https://learn.sparkfun.com/tutorials/112) will not make a distinction between virtual or native COM ports. However, for virtual serial ports, the port settings *(i.e. baudrate, etc.)* are not relevant and the default configuration be used in the terminal emulation program. However, for the physical/native `COM` ports will have the following default setting: 

		* Baudrate: 115200bps
		* Data Bits: 8
		* Parity: No
		* Stop Bits: 1
		* Flow Control: None

	??? tip "Having Trouble?"
		For users who are having trouble installing the USB driver, we have an archived version *(v3.0.2[^9])* of the installation file. Users can download [**version 3.0.2**](./assets/component_documentation/driver/USB_driver_3_0_2_Installer.exe) of the driver, by clicking on the button below.

		[^9]:
			For the latest USB driver from Septentrio, please install their driver through the [RxTools software suite](../rxtools).<br>
			*This is driver version, was archived at the time that this guide was written. Please do not request for the file to be updated.*

		<article style="text-align: center;" markdown>
		[:octicons-download-16:{ .heart } Download USB Driver *(v3.0.2)*](./assets/component_documentation/driver/USB_driver_3_0_2_Installer.exe){ .md-button .md-button--primary target="blank" }
		</article>


=== "Linux"
	On Linux, the standard Linux CDC-ACM driver is suitable.


## Web Interface
With the USB driver installed, the mosaic-X5 module supports Ethernet-over-USB. The default IP address allocated for the Ethernet-over-USB interface is `192.168.3.1`. This IP can be entered in any browser to open a connection to the receiver's Web Interface as shown below.

<div class="grid" markdown>

<div markdown>

<figure markdown>
[![navigation tabs in the web interface](./assets/img/hookup_guide/navigation_tabs.png){ width="600" }](./assets/img/hookup_guide/navigation_tabs.png "Click to enlarge")
<figcaption markdown>All the drop-down navigation tabs in the web interface.</figcaption>
</figure>

</div>

<div markdown>

<article class="video-500px" style="margin: auto;" markdown>
<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8" title="Septentrio: Getting started with the Septentrio mosaic receiver module" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</article>

</div>

</div>


!!! info
	The default IP address cannot be changed; this feature is only to be used when a single receiver is connected to your computer.

??? failure "Invalid IP Address *(WiFi Only)*"
	[One of the documentation pages on Septentrio's website](https://customersupport.septentrio.com/s/article/What-is-the-default-IP-address-to-connect-via-WiFi), specifies a default IP address of `192.168.20.1` for the web interface. However, that address is for a WiFi enabled product and cannot be used with this product.
