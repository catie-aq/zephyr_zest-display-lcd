# Zest_Display_LCD

Zest_Display_LCD board support for Zephyr OS.

## Usage
The `zephyr,display` label is exposed by the overlay, allowing to use the SPI interface with the default 6TRON SPI interface (`sixtron_spi`).

The `backlight_lcd` label is exposed by the overlay, allowing to use the PWM interface with the default 6TRON PWM interface (`pwm1`).

Shield name: `zest_display_lcd`
