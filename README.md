# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.

## Usage
The `zephyr,display` label is exposed by the overlay, allowing to use the spi interface with the default 6TRON spi interface (`sixtron_spi`).

The `backlight_lcd` label is exposed by the overlay, allowing to use the pwm interface with the default 6TRON pwm interface (`pwm1`).

Shield name: `zest_display_lcd`
