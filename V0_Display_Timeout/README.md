# V0 Display Timeout

This is a sample configuration file for adding a timeout to a V0 display to prevent OLED burn in. All values that should be filled in by the user are marked with `TODO` in comments.

This configuration creates 3 macros:

* `DISPLAY_ON`: Turns the display on.
* `DISPLAY_OFF`: Turns the display off.
* `DISPLAY_TIMEOUT`: Automatically turns the display off after a given `TIMEOUT` parameter or a default number of seconds. If the display's click wheel is pressed before the display times out, the timeout is reset.
* `DISABLE_DISPLAY_TIMEOUT`: Disables the display timeout.

These macros can be incorporated into `PRINT_START` and `PRINT_END` so that the display is always on during printing and automatically turns off afterwards.