# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.

## Usage

This board enable the following driver:

- [ILITEK ILI9163C](https://www.buydisplay.com/download/ic/ILI9163.pdf) display driver
- [Texas Instruments TSC2003](https://www.ti.com/lit/ds/symlink/tsc2003.pdf) display driver

:bulb: Display driver should also be added to your workspace:

- [ILITEK ILI9163C driver](https://github.com/catie-aq/zephyr_ilitek-ili9163c) for Zephyr-Os
- [Texas Instruments TSC2003](https://github.com/catie-aq/zephyr_ti-tsc2003) for Zephyr-OS

> [!NOTE]
> The node label for the ILI9163C component is `ili9163c`. It is **chosen** by `zephyr,display`. \
> The node label for the TSC2003 component is `tsc20030`. It is **chosen** by `zephyr,touch`. \
> Shield name: `zest_display_lcd`.
