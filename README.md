# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.
## Usage
This board enable the following driver:
- [ILITEK ILI9163C](https://www.buydisplay.com/download/ic/ILI9163.pdf) display driver

:bulb: Display driver should also be added to your workspace:
- [ILITEK ILI9163C driver for Zephyr OS](https://github.com/catie-aq/zephyr_ilitek-ili9163c)

The `zephyr,display` label is exposed by the overlay.
Shield name: `zest_display_lcd`

A full demonstration using the LVGL library is available here:
[zephyr_zest-display-lcd_demo](https://github.com/catie-aq/zephyr_zest-display-lcd_demo).
