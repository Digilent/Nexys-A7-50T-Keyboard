Nexys A7-50T Keyboard Demo
==============

Description
--------------
This project is a Vivado demo using the Nexys A7-50T's USB HID Host port and USB UART bridge, written in Verilog. When programmed onto the board, whenever the user presses a key on a keyboard connected to the USB HID port (J5, labeled "USB HOST"), a scan code is sent to the Nexys A7-50T through a PS/2 interface. This scan code is read and transmitted to the computer via the USB-UART bridge. When the key is released, a scan code of 0xF0XX is transmitted, indicating that the key with PS/2 code "XX" has been released.

To use this demo, the Nexys A7-50T must be connected to a serial terminal on the computer it is connected to over the MicroUSB cable. For more information on how to set up and use a serial terminal, such as Tera Term or PuTTY, refer to [this tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).

For example: If the user presses the space bar on a keyboard connected to the Nexys A7-50T, the scan code "29" will be sent to the computer.  When the space bar is released, "F0 29" will be printed.

Requirements
--------------
* **Nexys A7-50T**: To purchase a Nexys A7-50T, see the [Digilent Store](FIXME)
* **Vivado 2020.1 Installation**: To set up Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator**: For more information, see the [Installating and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**
* **USB Keyboard**

Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Nexys-A7-50T-GPIO/releases).
2. Open the project in Vivado 2020.1 by double clicking on the included XPR file found at "\<archive extracted location\>/Nexys-A7-50T-Keyboard/Nexys-A7-50T-Keyboard.xpr".
3. In the Flow Navigator panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug a Basys 3 into the computer running Vivado using a MicroUSB cable.
5. Open a serial terminal emulator (such as TeraTerm) and connect it to the Nexys A7-50T's serial port, using a baud rate of 9600.
6. In the green bar at the top of the window, click **Open target**. Select **Auto connect** from the drop down menu.
7. In the green bar at the top of the window, click **Program device**.
8. In the "Program Device" Wizard, enter "\<archive extracted location\>vivado_proj/Nexys-A7-50T-Keyboard.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
9. The demo will now be programmed onto the Nexys A7-50T. See the Introduction section of this README for a description of how this demo works.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project.

Check out the Nexys A7-50T's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/nexys-a7/start) to find more documentation, demos, and tutorials.

For technical support or questions, please post on the [Digilent Forum](https://forum.digilentinc.com).

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)


