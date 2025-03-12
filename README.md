# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.

## Usage

This board enables the following components:

- [ILITEK ILI9163C](https://www.buydisplay.com/download/ic/ILI9163.pdf) touchscreen driver
- [Texas Instruments TSC2003](https://www.ti.com/lit/ds/symlink/tsc2003.pdf) display driver

:bulb: These drivers should also be added to your workspace:

- [ILITEK ILI9163C driver](https://github.com/catie-aq/zephyr_ilitek-ili9163c) for Zephyr OS
- [Texas Instruments TSC2003](https://github.com/catie-aq/zephyr_ti-tsc2003) for Zephyr OS

:pushpin: This shield defines:

- the default display controller: `zephyr,display` to `ili9163c`
- the default touchscreen controller: `zephyr,touch` to `tsc20030`

:triangular_ruler: Process as follow:

This shield from 6TRON includes a macro generator to create the shield device tree. The only required parameter is the **port** identificator to which it is connected.

- Device tree generation in **app.overlay**: `ZEST_DISPLAY_LCD(port)`
- Add shield to build configuration: `zest_display_lcd`

## Advanced Usage

This shield can be hardware-modified to suit the user's application. To configure the hardware for a custom setup, the shield includes a macro generator with the following parameters:

- **nss** : LCD SPI Chip select pin default to `SPI_SS`
- **dc** : LCD SPI Data/Command pin default to `DIO2`
- **pwm** : LCD backlight pin default to `PWM1`
- **irq** : Touchscreen IRQ pin default to `DIO3`

:triangular_ruler: Alternative process:

- Device tree generation in **app.overlay**: `ZEST_DISPLAY_LCD_ALT(port, irq, nss, dc, pwm)`
- Add shield to build configuration: `zest_display_lcd_alt`
