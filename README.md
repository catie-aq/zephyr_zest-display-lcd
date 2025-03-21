# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.

## Usage

This board enables the following components:

- [ILITek ILI9163C](https://www.buydisplay.com/download/ic/ILI9163.pdf) display driver
- [Texas Instruments TSC2003](https://www.ti.com/lit/ds/symlink/tsc2003.pdf) touchscreen driver

:bulb: These drivers should also be added to your workspace:

- [ILITek ILI9163C driver](https://github.com/catie-aq/zephyr_ilitek-ili9163c)
- [Texas Instruments TSC2003 driver](https://github.com/catie-aq/zephyr_ti-tsc2003)

:pushpin: This shield defines:

- the default display controller: `zephyr,display` to `ili9163c_zest_display_lcd_<X>`
- the default touchscreen controller: `zephyr,touch` to `tsc2003_zest_display_lcd_<X>`

:triangular_ruler: To use this shield:

- Update your device tree by adding the `ZEST_DISPLAY_LCD(port)` macro to the `app.overlay` file.\
  Replace `port` with the number of the Zest_Core port to which the shield is connected, e.g.:

  ```c
  ZEST_DISPLAY_LCD(1) /* Zest_Display_LCD connected to Zest_Core first port */
  ```

- Activate support for the shield by adding `--shield zest_display_lcd` to the west command.

## Advanced Usage

This shield can be hardware-modified to suit your application.

In that case, use instead the alternate variant of the shield:

- Update your device tree by adding the `ZEST_DISPLAY_LCD_ALT(port, nss, dc, pwm, irq)` macro to the `app.overlay` file, with:
  - `port`: number of the Zest_Core port to which the shield is connected,
  - `nss`: display controller SPI Slave Select pin,
  - `dc`: display controller Data/Command pin,
  - `pwm`: display backlight PWM pin,
  - `irq`: touchscreen controller IRQ pin
- Activate support for the shield by adding `--shield zest_display_lcd_alt` to the west command.
