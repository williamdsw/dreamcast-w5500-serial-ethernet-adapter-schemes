# WIZnet W5500 Ethernet for Sega Dreamcast

### About

These are hardware schemes based on the [WIZnet W5500 Ethernet Adapter by SWAT](http://www.dc-swat.ru/blog/hardware/1147.html) for Dreamcast.

### Components

For the SCIF serial port:

- [DC SD Adapter V2](https://s.click.aliexpress.com/e/_c3AjvPdd) or a [Coders Cable](https://dreamcast.wiki/Coder's_cable);
- [W5500 Ethernet Adapter](https://s.click.aliexpress.com/e/_c4poacBl) or a [Lite W5500 Ethernet Adapter](https://s.click.aliexpress.com/e/_c37pLoLz);
- [SD Adapter for MicroSD](https://s.click.aliexpress.com/e/_c3gHQMOF) (Optional: if you don't want to soldering and it will connect in the SD port of the DC SD Adapter)
- [Micro SD Sniffer](https://s.click.aliexpress.com/e/_c4KTzam7) (Optional: if you want to use with the SD Adapter for MicroSD or directly on the Micro SD port of the DC SD Adapter)
- [Dupont cables female to female](https://s.click.aliexpress.com/e/_c3PJ8LpV) (Optional: if you don't want or don't know how to soldering)

<!-- TODO For the SCI interface: -->

Also you will need a [DreamShell](https://github.com/DC-SWAT/DreamShell) or homebrew build with W5500 drivers to use it.

### Schemes

#### W5500 Ethernet Adapter (Blue model board)

| DC SD Adapter V2 (pin) | SD Adapter for MicroSD + SD Sniffer | W5500 (Blue model board) |
| ---------------------- | ----------------------------------- | ------------------------ |
| GND (3)                | GND                                 | GND                      |
| RX (4)                 | DAT0                                | MISO                     |
| TX (5)                 | CMD                                 | MOSI                     |
| RTS (6)                | CD                                  | SCS                      |
| CTS (7)                | CLK                                 | SCLK                     |
| 3.3V (10)              | VCC                                 | 3.3V                     |

Status: Power and data working.

![](Images/Adapter1.jpeg)

#### Lite W5500 Ethernet Adapter (Green model board)

| DC SD Adapter V2 (pin) | SD Adapter for MicroSD + SD Sniffer | W5500 (Green model board) |
| ---------------------- | ----------------------------------- | ------------------------- |
| GND (3)                | GND                                 | GND                       |
| RX (4)                 | DAT0                                | MISO                      |
| TX (5)                 | CMD                                 | MOSI                      |
| RTS (6)                | CD                                  | CS                        |
| CTS (7)                | CLK                                 | SCK                       |
| 3.3V (10)              | VCC                                 | V (3.3V)                  |

Status: Only power, data not working.

![](Images/Adapter2.jpeg)

### Ways of Testing

- [W5500 Tester CDI by JaderFox](./w5500_test.cdi)

![](Images/JaderFox.png)

- [Windows CE Dreamcast Community Edition (Network -> System Logs)](https://github.com/maximqaxd/wince-dc)

![](Images/WINCE_1.png)

![](Images/WINCE_2.png)

- [Dreamshell (Network -> Connect Ethernet -> Start FTP Server and/or Start HTTP Server)](https://github.com/DC-SWAT/DreamShell)

![](Images/Dreamshell.jpeg)
