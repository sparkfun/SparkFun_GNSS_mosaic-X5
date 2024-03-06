---
icon: material/book-open-page-variant
---

!!! danger
	!!! warning "ESD Sensitivity"
		The mosaic-X5 module is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.

		??? info "ESD Precaution"
			As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their module.

			<div class="grid cards col-2" markdown>

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


	!!! warning "Active Antenna"
		Never inject an external DC voltage into the SMA connector for the GPS antenna, as it may damage the mosaic-X5 module. For instance, when using a splitter to distribute the antenna signal to several GNSS receivers, make sure that no more than one output of the splitter passes DC. Use [DC-blocks](https://en.wikipedia.org/wiki/DC_block) otherwise.

		??? info
			A 3 - 5.5V DC voltage can be applied to the main antenna from the `VANT` pin, obviating the need for an external antenna supply or [bias-tee](https://en.wikipedia.org/wiki/Bias_tee).


# Introduction
<div class="grid cards desc" markdown>

-   <a href="https://www.sparkfun.com/products/23088">
	**mosaic-X5 GNSS Breakout**<br>
	**SKU:** GPS-23088

	---

	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com//assets/parts/2/3/3/1/6/23088_Mosaic_X5_Feature-_newQR_.jpg)
	</figure></a>

	<center>
	<article class="video_desc">
	<iframe src="https://www.youtube.com/embed/TSkIvtaVZc0" title="Product Showcase: SparkFun Tri-band GNSS RTK Breakout - mosaic-X5" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
	</article>
	![QR code to play video](./assets/img/qr_code/product_video.png){ .qr }


	[![QR code to product page](./assets/img/qr_code/product-low.png){ .tinyqr }&nbsp;&nbsp;Purchase from SparkFun :fontawesome-solid-cart-plus:{ .heart }](https://www.sparkfun.com/products/23088){ .md-button .md-button--primary }
	</center>


-   At the heart of the Triband GNSS RTK Breakout is [Septentrio](https://www.septentrio.com/en)'s mosaic-X5, their most compact, ultra-low power, multi-band, multi-constellation, high-precision GNSS receiver. The receiver supports the GPS (USA), GLONASS (Russia), Beidou (China), Galileo (Europe), and NavIC (India) constellations, including regional systems *(i.e. SBAS and QZSS)*. With its [**Real Time Kinematics**](https://learn.sparkfun.com/tutorials/813) (RTK) capabilities, the module can achieve a horizontal accuracy of 6mm (~0.25in), vertical accuracy of 1cm (~0.4in) using RTK, and timing precision of 5ns (5 billionths of a second). It also features Septentrio's unique [AIM+ technology](https://www.septentrio.com/en/learn-more/advanced-positioning-technology/aim-jamming-protection) for interference mitigation and anti-spoofing, ensuring best-in-class reliability and scalable position accuracy.

	The mosaic-X5 is a sophisticated chip running an internal web server that can be accessed through the USB interface with a standard browser using a Linux/Windows computer. Septentrio also provides dozens of [video tutorials](https://www.youtube.com/@SeptentrioGNSS/videos) to guide users through the configuration settings of their GNSS receivers utilizing the web interface.

	Beyond the capabilities of the mosaic-X5 module, this board is seamless to operate with no programming skills required. Gone are the times when a microcontroller was required to interface with the GNSS receiver and log data to an SD card. The mosaic-X5 Triband GNSS RTK Breakout can start/stop logging data, without a single line of code, just utilizing a simple button.

	This breakout board is a perfect middle ground for users who would like to integrate the mosaic-X5 module into a project/enclosure with access to a majority of the module's available pins, similar to Septentrio's developer kit, but in the smaller form factor of their evaluation kit. Or maybe... you just needed a PPS output at a 3.3V logic level. *Please, check out the rest ouf our guide for more details on the capabilities of this board (that we couldn't fit in this product description).*

</div>



??? danger "Important: Read Before Use!"
	!!! warning "ESD Sensitivity"
		The mosaic-X5 module is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.

		??? info "ESD Precaution"
			As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their module.

			<div class="grid cards col-2" markdown>

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


	!!! warning "Active Antenna"
		Never inject an external DC voltage into the SMA connector for the GPS antenna, as it may damage the mosaic-X5 module. For instance, when using a splitter to distribute the antenna signal to several GNSS receivers, make sure that no more than one output of the splitter passes DC. Use [DC-blocks](https://en.wikipedia.org/wiki/DC_block) otherwise.

		??? info
			A 3 - 5.5V DC voltage can be applied to the main antenna from the `VANT` pin, obviating the need for an external antenna supply or [bias-tee](https://en.wikipedia.org/wiki/Bias_tee).


??? question "Product Comparison"
	Below is a simple comparison table between our breakout board and Septentrio's development and evaluation kits:

	<div class="annotate" markdown align="center">
	<table markdown>
	<tr markdown>
	<td></td>
	<th markdown style="text-align:center">
		mosaic-X5 Development Kit<br>
		<hr>
		<figure markdown>
		![Product Thumbnail](./assets/img/hookup_guide/mosaic-development-kit.png){ width="200" }
		</figure>
	</th>
	<th markdown style="text-align:center">
		mosaic-go Evaluation Kit<br>
		<hr>
		<figure markdown>
		![Product Thumbnail](./assets/img/hookup_guide/mosaic-go-evaluation-kit.png){ width="200" }
		</figure>
	</th>
	<th markdown style="text-align:center">
		mosaic-X5 GNSS Breakout<br>
		<hr>
		<figure markdown>
		![Product Thumbnail](./assets/img/hookup_guide/product.png){ width="200" }
		</figure>
	</th>
	<th markdown style="text-align:center">
		RTK mosaic-X5<br>
		<hr>
		<figure markdown>
		![Product Thumbnail](./assets/img/hookup_guide/rtk_mosaic-x5.png){ width="200" }
		</figure>
	</th>
	</tr>
	<tr>
		<td style="vertical-align:middle;">GNSS Antenna</td>
		<td style="text-align:center; vertical-align:middle;">Dual</td>
		<td style="text-align:center">
			Single (mosaic-X5)<br>
			Dual (mosaic-H)
		</td>
		<td style="text-align:center; vertical-align:middle;">Single</td>
		<td style="text-align:center; vertical-align:middle;">Single</td>
	</tr>
	<tr>
		<td>USB Connector</td>
		<td style="text-align:center">micro-B</td>
		<td style="text-align:center">micro-B</td>
		<td style="text-align:center">Type-C</td>
		<td style="text-align:center">Type-C</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">Ethernet</td>
		<td style="text-align:center; vertical-align:middle;">
			Yes<br>
			<i>10/100 Base-T</i>
		</td>
		<td style="text-align:center; vertical-align:middle;">No</td>
		<td style="text-align:center; vertical-align:middle;">No</td>
		<td style="text-align:center">
			Yes<br>
			<i>10/100 Base-T</i>
		</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">WiFi</td>
		<td style="text-align:center; vertical-align:middle;">No</td>
		<td style="text-align:center; vertical-align:middle;">No</td>
		<td style="text-align:center; vertical-align:middle;">No</td>
		<td style="text-align:center">
			Yes - Network Bridge<br>
			<i>10 Base-T</i>
		</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">COM Ports</td>
		<td style="text-align:center">4</td>
		<td style="text-align:center">2</td>
		<td style="text-align:center">4</td>
		<td style="text-align:center">
			1 - mosaic-X5<br>
			1 - ESP32
		</td>
	</tr>
	<tr>
		<td>&micro;SD Card Slot</td>
		<td style="text-align:center">Yes</td>
		<td style="text-align:center">Yes</td>
		<td style="text-align:center">Yes</td>
		<td style="text-align:center">Yes</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">Reset/Log Buttons</td>
		<td style="text-align:center; vertical-align:middle;">Yes</td>
		<td style="text-align:center; vertical-align:middle;">No*</td>
		<td style="text-align:center; vertical-align:middle;">Yes</td>
		<td style="text-align:center; vertical-align:middle;">Yes</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">Logic-Level</td>
		<td style="text-align:center">
			1.8V<br>
			3.3V
		</td>
		<td style="text-align:center; vertical-align:middle;">3.3V</td>
		<td style="text-align:center; vertical-align:middle;">3.3V</td>
		<td style="text-align:center">
			3.3V<br>
			5V
		</td>
	</tr>
	<tr>
		<td>PPS Signal</td>
		<td style="text-align:center">Header Pin</td>
		<td style="text-align:center">6-Pin JST Connector</td>
		<td style="text-align:center">SMA Connector</td>
		<td style="text-align:center">Screw Terminal</td>
	</tr>
	<tr>
		<td>Enclosure Material</td>
		<td style="text-align:center; vertical-align:middle;">N/A</td>
		<td style="text-align:center; vertical-align:middle;">Metal</td>
		<td style="text-align:center; vertical-align:middle;">N/A</td>
		<td style="text-align:center; vertical-align:middle;">Aluminum</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">Dimensions</td>
		<td style="text-align:center; vertical-align:middle;">N/A</td>
		<td style="text-align:center; vertical-align:middle;">71 x 59 x 12mm ± 1mm</td>
		<td style="text-align:center; vertical-align:middle;">70.9 x 50.8 x 8mm</td>
		<td style="text-align:center">
			180.6 x 101.8 x 41mm<br>
			<i>Enclosure Only</i>
		</td>
	</tr>
	<tr>
		<td style="vertical-align:middle;">Weight</td>
		<td style="text-align:center; vertical-align:middle;">N/A</td>
		<td style="text-align:center; vertical-align:middle;">58g  ± 1g</td>
		<td style="text-align:center; vertical-align:middle;">22.6g</td>
		<td style="text-align:center">
			415.15g<br>
			<i>Enclosure Only</i>
		</td>
	</tr>
	
	</table>
	
	</div>

	!!! note "mosaic-go Evaluation Kit"
		The reset pin is exposed on 4-pin JST connector and the log pin is connected to the latch pin of the SD card slot.



## :fontawesome-solid-list-check:&nbsp;Required Materials
To get started, users will need a few items. Now some users may already have a few of these items, feel free to modify your cart accordingly.

<div class="annotate" markdown>

* Computer with an operating system (OS) that is compatible with all the software installation requirements (1)

	!!! warning "Software Compatibility"
		The [RxTools software suite](https://www.septentrio.com/en/products/gps-gnss-receiver-software/rxtools) from Septentrio, automatically installs the required USB-over-Ethernet driver and provides users with an interface for the receiver configuration, monitoring, data logging, and analysis. However, it only appears to be available for Windows and Linux operating systems.

* [USB 3.1 Cable A to C - 3 Foot](https://www.sparkfun.com/products/14743) - Used to interface with the mosaic-X5 GNSS Breakout (2)
* [SparkFun Tri-band GNSS RTK Breakout - mosaic-X5](https://www.sparkfun.com/products/23088) (3)
* [GNSS Multi-Band L1/L2/L5 Surveying Antenna](https://www.sparkfun.com/products/21801)
	* [SMA Male to TNC Male Cable](https://www.sparkfun.com/products/21740)
	* [Antenna Mount](https://www.sparkfun.com/products/21257)

</div>

1. A list of the compatible GNSS receiver software, is provided on the [Septentrio website](https://www.septentrio.com/en/products/gps-gnss-receiver-software).
2. If your computer doesn't have a USB-A slot, then choose an appropriate cable or adapter.
3. For the best performance, use a compatible L1/L2/L5 GNSS antenna.


<div class="grid cards col-4" markdown>

-   <a href="https://www.sparkfun.com/products/14743">
	<figure markdown>
	![USB 3.1 Cable A to C - 3 Foot](https://cdn.sparkfun.com/assets/parts/1/2/9/7/2/14743-USB_3.1_Cable_A_to_C_-_3_Foot-01.jpg)
	</figure>

	---

	**USB 3.1 Cable A to C - 3 Foot**<br>
	CAB-14743</a>

-   <a href="https://www.sparkfun.com/products/23088">
	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com//assets/parts/2/3/3/1/6/23088_Mosaic_X5_Feature-_newQR_.jpg)
	</figure>

	---

	**mosaic-X5 (Tri-band + RTK) GNSS Breakout**<br>
	GPS-23088</a>

-   <a href="https://www.sparkfun.com/products/21801">
	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/5/9/7/SparkFun_GNSS_SPK6618H_Triband_Antenna_-_2.jpg)
	</figure>		

	---

	**GNSS Multi-Band L1/L2/L5 Surveying Antenna - TNC (SPK6618H)**<br>
	GPS-21801</a>

-   <a href="https://www.sparkfun.com/products/21740">
	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/5/7/0/SparkFun_Reinforced_Interface_Cable_-_SMA_Male_to_TNC_Male_-_1.jpg)
	</figure>

	---

	**Reinforced Interface Cable - SMA Male to TNC Male (10m)**<br>
	CAB-21740</a>

-   <a href="https://www.sparkfun.com/products/21257">
	<figure markdown>
	![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/0/2/7/21257-_PRT_M90SD_Magnetic_Stand-_01.jpg)
	</figure>		

	---

	**GNSS Magnetic Antenna Mount - 5/8" 11-TPI**<br>
	PRT-21257</a>

</div>


!!! danger "ESD Protection"
	The Septentrio mosaic-X5 module is sensitive to [ESD](https://en.wikipedia.org/wiki/Electrostatic_discharge "Electrostatic Discharge"). Use a proper grounding system to make sure that the working surface and the components are at the same electric potential.

	<div class="grid cards col-2" markdown>

	- <center>
		<article class="video_cards">
		<iframe src="https://www.youtube.com/embed/hrL5J6Q5gX8?si=jOPBat8rzMnL7Uz4&amp;start=26;&amp;end=35;" title="Septentrio: Getting Started Video (playback starts at ESD warning)" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
		</article>
		</center>

		!!! warning
			As recommended by the manufacturer, we highly recommend that users take the necessary precautions to avoid damaging their module.


	-   <a href="https://www.sparkfun.com/products/15255">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/7/2/2/15255-iFixit_Pro_Tech_Toolkit-06.jpg)
		</figure>		

		---

		**iFixit Pro Tech Toolkit**<br>
		TOL-15255</a>

	</div>


??? note "Antennas & Accessories"
	For the best performance, we recommend users choose a compatible L1/L2/L5 (tri-band) GNSS antenna and utilize a low-loss cable. For additional options, please check out the [GPS Antenna](https://www.sparkfun.com/categories/18) category of our product catalog.

	=== "L5 Antennas"
	
		<div class="grid cards col-4" markdown>

		-   <a href="https://www.sparkfun.com/products/21801">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/5/9/7/SparkFun_GNSS_SPK6618H_Triband_Antenna_-_2.jpg)
			</figure>		

			---

			**GNSS Multi-Band L1/L2/L5 Surveying Antenna - TNC (SPK6618H)**<br>
			GPS-21801</a>

			??? info "Adapter Cable"
				For our TNC antennas, users will need a TNC to SMA adapter cable.
		
				<div class="grid cards col-3" markdown>
		
				-   <a href="https://www.sparkfun.com/products/17833">
					<figure markdown>
					![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/6/9/8/0/17833-Interface_Cable_-_SMA_Male_to_TNC_Male__300mm_-01.jpg)
					</figure>		
		
					---
		
					**Interface Cable - SMA Male to TNC Male (300mm)**<br>
					CAB-17833</a>
		
				-   <a href="https://www.sparkfun.com/products/21739">
					<figure markdown>
					![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/5/6/9/SparkFun_Reinforced_Interface_Cable_-_SMA_Male_to_TNC_Male_-_4.jpg)
					</figure>
		
					---
		
					**Reinforced Interface Cable - SMA Male to TNC Male (300mm)**<br>
					CAB-21739</a>
		
				-   <a href="https://www.sparkfun.com/products/21740">
					<figure markdown>
					![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/5/7/0/SparkFun_Reinforced_Interface_Cable_-_SMA_Male_to_TNC_Male_-_1.jpg)
					</figure>
		
					---
		
					**Reinforced Interface Cable - SMA Male to TNC Male (10m)**<br>
					CAB-21740</a>
		
				</div>


		-   <a href="https://www.sparkfun.com/products/15192">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/6/1/1/15192-GNSS_Multi-band_Magnetic_Mount_Antenna_SMA_-_5m-01.jpg)
			</figure>

			---

			**GNSS Multi-Band Magnetic Mount Antenna - 5m (SMA)**<br>
			GPS-15192</a>

			??? info "Kit Version"
				We also offer this product in a kit, which includes a ground plate and USB-C cable.

				<div class="grid cards col-1" markdown>

				-   <a href="https://www.sparkfun.com/products/18293">
					<figure markdown>
					![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/7/6/2/3/18293-SparkFun_GPS-RTK_Accessory_Kit-01.jpg)
					</figure>		

					---

					**SparkFun GNSS-RTK Accessory Kit**<br>
					KIT-18293</a>

				</div>


		-   <a href="https://www.sparkfun.com/products/17108">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/6/0/7/0/17108-AA.200_____MagmaX2_Active_Multiband_GNSS_Magnetic_Mount_Antenna-01A.jpg)
			</figure>

			---

			**MagmaX2 Active Multiband GNSS Magnetic Mount Antenna - AA.200**<br>
			GPS-17108</a>

		</div>


	=== "Mounting Hardware"

		<div class="grid cards col-4" markdown>

		-   <a href="https://www.sparkfun.com/products/21257">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/1/0/2/7/21257-_PRT_M90SD_Magnetic_Stand-_01.jpg)
			</figure>		

			---

			**GNSS Magnetic Antenna Mount - 5/8" 11-TPI**<br>
			PRT-21257</a>

			!!! info "5/8"-11 TPI"
				This product is meant to be used with our surveying antennas. To mount those antennas to a camera tripod, check out our [tripod adapter](https://www.sparkfun.com/products/17546).

		-   <a href="https://www.sparkfun.com/products/22197">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/2/0/9/7/22197-_01.jpg)
			</figure>		

			---

			**GNSS Antenna Mounting Hardware Kit**<br>
			KIT-22197</a>

			!!! info "5/8"-11 TPI"
				This product is meant to be used with our surveying antennas. To mount those antennas to a camera tripod, check out our [tripod adapter](https://www.sparkfun.com/products/17546).

		-   <a href="https://www.sparkfun.com/products/17519">
			<figure markdown>
			![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/6/5/9/3/17519-GPS_Antenna_Ground_Plate-01.jpg)
			</figure>		

			---

			**GPS Antenna Ground Plate**<br>
			GPS-17519</a>

			!!! info "1/4"-20 TPI"
				This product is meant to be used with our magnetic antennas and a camera tripod with a standard ¼"-20 UNC camera mounting screw.

		</div>


??? note "Data Logging"
	The Septentrio mosaic-X5 module is capable of logging data to an &micro;SD card. Please check out the [memory cards and accessories](https://www.sparkfun.com/categories/351) in our product catalog.

	<div class="grid cards col-4" markdown>

	-   <a href="https://www.sparkfun.com/products/15107">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/3/4/7/0/15107-microSD_Card_-_1GB__Class_4_-01.jpg)
		</figure>		

		---

		**microSD Card - 1GB (Class 4)**<br>
		COM-15107</a>

	-   <a href="https://www.sparkfun.com/products/13004">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/9/9/5/8/13004-03.jpg)
		</figure>		

		---

		**microSD USB Reader**<br>
		COM-13004</a>

	</div>

??? note "JST Cable & Transceivers"
	In remote applications, users may need to utilize one of our radio transceivers for RTK correction data. Users may also find our breadboard cable convenient for connecting your module to a development board.

	<div class="grid cards col-2" markdown>

	-   <a href="https://www.sparkfun.com/products/19032">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/8/6/3/4/19032-SiK_Telemetry_Radio_V3_-_915MHz__100mW-01.jpg)
		</figure>

		---

		**SiK Telemetry Radio V3 - 915MHz, 100mW**<br>
		WRL-19032</a>

	-   <a href="https://www.sparkfun.com/products/20029">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/9/7/9/0/SparkFun_LoRaSerial_Enclosed_-_20029-1.jpg)
		</figure>

		---

		**SparkFun LoRaSerial Kit - 915MHz (Enclosed)**<br>
		WRL-20029</a>

	-   <a href="https://www.sparkfun.com/products/18079">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/7/3/9/5/18079-Breadboard_to_GHR-06V_Cable_-_6-Pin_x_1.25mm_Pitch-01a.jpg)
		</figure>

		---

		**Breadboard to JST-GHR-06V Cable - 6-Pin x 1.25mm Pitch**<br>
		CAB-18079</a>

	-   <a href="https://www.sparkfun.com/products/12044">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/8/6/2/7/12044-01.jpg)
		</figure>

		---

		**Breadboard - Mini Modular (Red)**<br>
		PRT-12044</a>

	</div>



??? note "Headers and Wiring"
	To add headers or hookup wires, users will need [soldering equipment](https://www.sparkfun.com/categories/49) and [headers](https://www.sparkfun.com/categories/381)/[wire](https://www.sparkfun.com/search/results?term=hook-up+wire).


	!!! tip "New to soldering?"
		Check out our [How to Solder: Through-Hole Soldering](https://learn.sparkfun.com/tutorials/5) tutorial for a quick introduction!

		<div class="grid cards col-4" markdown align="center">

		-   <a href="https://learn.sparkfun.com/tutorials/5">
			<figure markdown>
			![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg)
			</figure>

			---
	
			**How to Solder: Through-Hole Soldering**</a>

		</div>


	<div class="grid cards col-4" markdown>

	-   <a href="https://www.sparkfun.com/products/9325">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/8/7/3/09325_9161-Solder_Lead_Free_-_100-gram_Spool-01.jpg)
		</figure>		

		---

		**Solder Lead Free - 100-gram Spool**<br>
		TOL-09325</a>

	-   <a href="https://www.sparkfun.com/products/24063">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/4/3/8/5/KIT-24063-PINECIL-Soldering-Iron-Kit-Feature.jpg)
		</figure>

		---
		
		**PINECIL Soldering Iron Kit**<br>
		KIT-24063</a>

	-   <a href="https://www.sparkfun.com/products/14579">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg)
		</figure>

		---

		**Chip Quik No-Clean Flux Pen - 10mL**<br>
		TOL-14579</a>


	-   <a href="https://www.sparkfun.com/products/116">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/0/6/00116-02-L.jpg)
		</figure>

		---

		**Break Away Headers - Straight**<br>
		PRT-00116</a>

	-   <a href="https://www.sparkfun.com/products/11375">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/7/1/2/0/11375-Hook-Up_Wire_-_Assortment__Solid_Core__22_AWG_-01.jpg)
		</figure>

		---

		**Hook-Up Wire - Assortment (Stranded, 22 AWG)**<br>
		PRT-11375</a>

	</div>


??? note "Jumper Modification"
	To modify the [jumpers](../hardware_overview/#jumpers), users will need [soldering equipment](https://www.sparkfun.com/categories/49) and/or a [hobby knife](https://www.sparkfun.com/categories/379).


	!!! tip "New to jumper pads?"
		Check out our [Jumper Pads and PCB Traces Tutorial](https://learn.sparkfun.com/tutorials/664) for a quick introduction!

		<div class="grid cards col-4" markdown align="center">

		-   <a href="https://learn.sparkfun.com/tutorials/664">
			<figure markdown>
			![Tutorial thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
			</figure>

			---
			
			**How to Work with Jumper Pads and PCB Traces**</a>

		</div>


	<div class="grid cards col-4" markdown>

	-   <a href="https://www.sparkfun.com/products/9325">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/8/7/3/09325_9161-Solder_Lead_Free_-_100-gram_Spool-01.jpg)
		</figure>		

		---

		**Solder Lead Free - 100-gram Spool**<br>
		TOL-09325</a>

	-   <a href="https://www.sparkfun.com/products/22265">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/2/2/0/2/TOL-22265-Beginner-Tool-Kit-Feature.jpg)
		</figure>

		---

		**SparkFun Beginner Tool Kit**<br>
		TOL-22265</a>

	-   <a href="https://www.sparkfun.com/products/14579">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/1/2/7/2/5/14579-Chip_Quik_No-Clean_Flux_Pen_-_10mL-01.jpg)
		</figure>

		---

		**Chip Quik No-Clean Flux Pen - 10mL**<br>
		TOL-14579</a>

	-   <a href="https://www.sparkfun.com/products/9200">
		<figure markdown>
		![Product Thumbnail](https://cdn.sparkfun.com/assets/parts/2/6/4/6/09200-Hobby_Knife-01.jpg)
		</figure>

		---

		**Hobby Knife**<br>
		TOL-09200</a>

	</div>




## :material-bookshelf:&nbsp;Suggested Reading

As a more sophisticated product, we will skip over the more fundamental tutorials (i.e. [**Ohm's Law**](https://learn.sparkfun.com/tutorials/voltage-current-resistance-and-ohms-law) and [**What is Electricity?**](https://learn.sparkfun.com/tutorials/what-is-electricity)). However, below are a few tutorials that may help users familiarize themselves with various aspects of the board.

!!! tip
	Check out the [www.gps.gov](https://www.gps.gov/) website to learn more about the U.S.-owned [Global Positioning System (GPS)](https://www.gps.gov/systems/gps/) and the [Global Navigation Satellite Systems (GNSS) of other countries](https://www.gps.gov/systems/gnss/).


<div class="grid cards col-4" markdown align="center">

-   <a href="https://learn.sparkfun.com/tutorials/9">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/parts/5/9/7/4/10890-01.jpg)
	</figure>

	---

	**GPS Basics**</a>

-   <a href="https://learn.sparkfun.com/tutorials/813">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/178-100/assets/learn_tutorials/8/1/3/Location-Wandering-GPS-combined.jpg)
	</figure>

	---

	**What is GPS RTK?**</a>

-   <a href="https://docs.sparkfun.com/SparkFun_RTK_mosaic-X5">
	<figure markdown>
	![Tutorial Thumbnail](https://docs.sparkfun.com/SparkFun_RTK_mosaic-X5/assets/img/thumbnail.jpg)
	</figure>

	---

	**RTK mosaic-X5 Hookup Guide**</a>

-   <a href="https://learn.sparkfun.com/tutorials/8">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/7/d/f/9/9/50d24be7ce395f1f6c000000.jpg)
	</figure>

	---

	**Serial Communication**</a>

-   <a href="https://learn.sparkfun.com/tutorials/112">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/1/1/2/thumb.jpg)
	</figure>

	---

	**Serial Terminal Basics**</a>

-   <a href="https://learn.sparkfun.com/tutorials/36">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/3/6/Bench_Power_Supply.jpg)
	</figure>

	---

	**How to Power a Project**</a>

-   <a href="https://learn.sparkfun.com/tutorials/5">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/e/3/9/9/4/51d9fbe1ce395f7a2a000000.jpg)
	</figure>

	---

	**How to Solder: Through-Hole Soldering**</a>

-   <a href="https://learn.sparkfun.com/tutorials/664">
	<figure markdown>
	![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/learn_tutorials/6/6/4/PCB_TraceCutLumenati.jpg)
	</figure>

	---

	**How to Work with Jumper Pads and PCB Traces**</a>

</div>

??? info "Related Blog Posts"
	Additionally, users may be interested in these blog post articles on GNSS technologies:

	<div class="grid cards col-4" markdown align="center">

	-   <a href="https://www.sparkfun.com/news/4276">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/4/2/7/6/GPSvGNSSHomepageImage4.png)
		</figure>

		---

		**GPS vs GNSS**</a>
	
	-   <a href="https://www.sparkfun.com/news/7138">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/7/1/3/8/SparkFun_RTK_Facet_-_Surveying_Monopod.jpg)
		</figure>

		---

		**What is Correction Data?**</a>
	
	-   <a href="https://www.sparkfun.com/news/7533">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/7/5/3/3/rtk-blog-thumb.png)
		</figure>

		---

		**Real-Time Kinematics Explained**</a>
	
	-   <a href="https://www.sparkfun.com/news/7401">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/7/4/0/1/Screen_Shot_2023-06-26_at_8.30.22_PM.png)
		</figure>

		---

		**New Video: Unlocking High-Precision RTK Positioning**</a>

	-   <a href="https://www.sparkfun.com/news/9514">
		<figure markdown>
		![Tutorial Thumbnail](https://cdn.sparkfun.com/c/264-148/assets/home_page_posts/9/5/1/4/DIY-Surveying-Blog__1_.jpg)
		</figure>

		---

		**DIY RTK Surveying**</a>

	</div>
