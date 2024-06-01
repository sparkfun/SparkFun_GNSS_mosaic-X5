---
icon: septentrio-logo
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

			<center>
			<article class="video-500px">
			<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8?si=jOPBat8rzMnL7Uz4&amp;start=26;&amp;end=35;" title="Septentrio: Getting Started Video (playback starts at ESD warning)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
			</article>
			</center>

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


# RxTools Software Suite

!!! tip
	Even if you aren't necessarily interested it, we highly recommend that users install the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) before plugging in their board. For Windows PCs, it also includes the USB driver for the module that enables the Ethernet-over-USB support and virtual `COM` ports.

Users should install the [RXTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) on their computer to interact with the mosaic-X5 module through the USB interface. The software package includes the USB-IP driver[^1] necessary to recognize the board as an ethernet device on Windows PCs (1).
{ .annotate }

1. On Linux, the standard Linux CDC-ACM driver is suitable.

[^1]: On Linux, the standard Linux CDC-ACM driver is suitable.


<center>
[:octicons-download-16:{ .heart } Download the RxTools Software from Septentrio](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools){ .md-button .md-button--primary target="blank" }
</center>

## System Requirements[^2]

<div class="grid" markdown>

<div markdown>

### Operating System

---

* Windows 7
* Windows 8
* Windows 10
* Fedora 23 *(or later)* using Qt technology.
	* The standalone tools (except `bin2asc`) will run on older distributions.

</div>

<div markdown>

### Hardware Requirements[^3]

---

The minimal hardware requirements *(1Hz update)*:

* CPU: 1 GHz processor
* RAM: 1 GB RAM
* Screen Resolution: 1024×768 or higher resolution

</div>

</div>

[^2]: The system requirements and installation instructions are from the RxTools *v22.1.0* user manual. This information may change in later iterations of the software suite. Please refer to the user manual *(of the version you are utilizing)* for the most accurate information.
[^3]: Higher data rates will require higher CPU speed and more memory capacity.

## Installation Instructions[^2]

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

	Users can install RxTools software suite by running the installation binary[^4](1), located in the `RxTools/linux-i386/` directory of the downloaded `*.zip` file[^5]. During the installation, users will be prompted for an installation directory. If there are any previous installations of RxControl,  please use a different directory to avoid conflicts.
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

## Getting Started

=== "Windows"
	Once **RxTools** have been installed, any of the individual GUI tools can be launched using the **RxLauncher** application.

	When connecting to a receiver using USB, two virtual serial ports will be created on your machine which can be used to communicate to the receiver.

	* Check the Device Manager to see the exact names of these virtual serial ports.
		* They ports will appear with the name `Septentrio` written beside them.
	* These virtual serial ports will be labeled as such when **RxControl** shows the Connection Dialog.

	!!! tip
		The virtual serial port names correspond to a given USB port. When plugging the device into a different USB port, the serial port will change.

=== "Linux"
	Once **RxControl** is installed, it can be launched by executing the link created by the installation program or by executing `./runRxControl` in the directory where the program is installed.

	* The **Data Link** and **SBF Converter** applications should be executed from the `/bin` directory of the installation folder, to ensure that the proper libraries are loaded. Users can also run these applications from the installation directory, in a manner similar to **RxControl** that is described above.
	* Other applications can also be executed by launching their appropriate script.
		* For example, users can execute `./runDataLink` from the `/bin` directory, located inside the installation folder.
