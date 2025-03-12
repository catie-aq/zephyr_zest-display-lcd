# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.

## Usage

This board enables the following components:

- [ILITEK ILI9163C](https://www.buydisplay.com/download/ic/ILI9163.pdf) touchscreen driver
- [Texas Instruments TSC2003](https://www.ti.com/lit/ds/symlink/tsc2003.pdf) display driver

:bulb: These drivers should also be added to your workspace:

- [ILITEK ILI9163C driver](https://github.com/catie-aq/zephyr_ilitek-ili9163c) for Zephyr OS
- [Texas Instruments TSC2003](https://github.com/catie-aq/zephyr_ti-tsc2003) for Zephyr OS

This shield defines:

- the default display controller: `zephyr,display`
- the default touchscreen controller: `zephyr,touch`

> [!NOTE]
> Shield name: `zest_display_lcd`
