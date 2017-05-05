# Screen Backlight Keys #

Problem: When using the Nvidia binary driver, the on-screen backlight indicator
goes up and down by the keys, but the backlight remains at full brightness.

Fix:
 - Edit /etc/default/grub
 - In the line starting with `GRUB_CMDLINE_LINUX_DEFAULT`, add `acpi_backlight=native` inside the parenthesis.
 - Example: `GRUB_CMDLINE_LINUX_DEFAULT="quiet splash acpi_backlight=native"`
 - Reboot
 