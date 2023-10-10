SparkFun Tri-band GNSS RTK Breakout - mosaic-X5
========================================

[![SparkFun Tri-band GNSS RTK Breakout - mosaic-X5](https://cdn.sparkfun.com/assets/parts/2/3/3/1/6/23088-_01.jpg)](https://www.sparkfun.com/products/23088)

[*SparkFun Tri-band GNSS RTK Breakout - mosaic-X5 (GPS-23088)*](https://www.sparkfun.com/products/23088)

At the heart of the Triband GNSS RTK Breakout is [Septentrio](https://www.septentrio.com/en)'s mosaic-X5, their most compact, ultra-low power, multi-band, multi-constellation, high-precision GNSS receiver. The receiver supports the GPS (USA), GLONASS (Russia), Beidou (China), Galileo (Europe), and NavIC (India) constellations, including regional systems *(i.e. SBAS and QZSS)*. With its [**Real Time Kinematics**](https://learn.sparkfun.com/tutorials/813) (RTK) capabilities, the module can achieve a horizontal accuracy of 6mm (~0.25in), vertical accuracy of 1cm (~0.4in) using RTK, and timing precision of 5ns (5 billionths of a second). It also features Septentrio's unique [AIM+ technology](https://www.septentrio.com/en/learn-more/advanced-positioning-technology/aim-jamming-protection) for interference mitigation and anti-spoofing, ensuring best-in-class reliability and scalable position accuracy.

The mosaic-X5 is a sophisticated chip running an internal web server that can be accessed through the USB interface with a standard browser using a Linux/Windows computer. Septentrio also provides dozens of [video tutorials](https://www.youtube.com/@SeptentrioGNSS/videos) to guide users through the configuration settings of their GNSS receivers utilizing the web interface.

Beyond the capabilities of the mosaic-X5 module, this board is seamless to operate with no programming skills required. Gone are the times when a microcontroller was required to interface with the GNSS receiver and log data to an SD card and when users had to carry around an SD card reader to extract the data from the SD card. The mosaic-X5 Triband GNSS RTK Breakout can start/stop logging data or mount/unmount the SD card, without a single line of code, just utilizing a simple button. For the users who prefer a command-line interface, Septentrio has you covered. Users can still control and configure the mosaic-X5 module through a CLI, which is useful for scenarios such as production line testing *(in fact, that is how we tested this board)*.

This breakout board is a perfect middle ground for users who would like to integrate the mosaic-X5 module into a project/enclosure with access to a majority of the module's available pins, similar to Septentrio's developer kit, but in the smaller form factor of their evaluation kit. Or maybe... you just needed a PPS output at a 3.3V logic level. *Please, check out our [hookup guide](https://docs.sparkfun.com/SparkFun_GNSS_mosaic-X5) for more details on the capabilities of this board (that we couldn't fit in this product description).*

Repository Contents
-------------------

* **[/docs](/docs/)** - Online documentation files
    * [assets](/docs/assets/) - Assets files
        * [board_files](/docs/assets/board_files/) - Files for the product design
            * [Eagle design files](/docs/assets/board_files/eagle_files.zip) (.zip)
            * [Schematic](/docs/assets/board_files/schematic.pdf) (.pdf)
            * [Dimensions](/docs/assets/board_files/dimensions.pdf) (.pdf)
        * [component_documentation](/docs/assets/component_documentation/) - Datasheets for hardware components
        * [img/hookup_guide/](/docs/assets/img/hookup_guide/) - Images for hookup guide documentation
* **[/Hardware](/Hardware/)** - Eagle design files (.brd, .sch)
* **[/Production](/Production/)** - Production files


Documentation
--------------

* **[Hookup Guide (mkdocs)](http://docs.sparkfun.com/SparkFun_GNSS_mosaic-X5/)** - Hookup guide for the mosaic-X5 GNSS Breakout hosted by GitHub pages.

*Need to download or print our hookup guide?*

* [Print *(Print to PDF)* from Single-Page View](http://docs.sparkfun.com/SparkFun_GNSS_mosaic-X5/print_view)

Product Variants
----------------

* [GPS-23088](https://www.sparkfun.com/products/23088)- v1.0, Initial Release

Version History
---------------

* [v10](https://github.com/sparkfun/SparkFun_GNSS_mosaic-X5/releases/tag/v01) - Initial Release


License Information
-------------------

This product is ***open source***!

Please review the [`LICENSE.md`](./LICENSE.md) file for license information.

If you have any questions or concerns about licensing, please contact technical support on our [SparkFun forums](https://forum.sparkfun.com/viewforum.php?f=152).

Distributed as-is; no warranty is given.

- Your friends at SparkFun.
