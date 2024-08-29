# Show Sensors

![Show Sensors](./images/show_sensors.png)

Starts the "sensors" utility in an instance of Konsole (terminal emulator) with its window positioned in the top right corner of the (main) screen with the defined dimensions and keeping the window above others.

**IMPORTANT:** My life, my work and my passion is free software. Corrections, tweaks and improvements are very welcome (**pull requests** 😉)! Please consider giving us a ⭐, fork, support this project or even visit our professional profile (see [About](#about)). **Thanks!** 🥰

# Donations

Please consider to deposit a donation through PayPal by clicking on the next button...

[![Donation Account](./images/paypal.png)](https://www.paypal.com/donate/?hosted_button_id=TANFQFHXMZDZE)

This is free software and you are equally free to specify any amount of money you want.

**Support free software and my work!** ❤️👨‍👩‍👧🐧

# Table of Contents

   * [Install](#install)
      + [Install required utilities](#install-required-utilities)
      + [Disable "Remember window size"](#disable-remember-window-size)
      + [Make the Script Executable](#make-the-script-executable)
      + [Create a shortcut (KDE, Suggestion)](#create-a-shortcut-kde-suggestion)
   * [Final considerations](#final-considerations)
   * [Future](#future)
- [About](#about)

## Install

### Install required utilities

Install the "lm_sensors", "wmctrl" and "xdotool" utilities.

**NOTE:** After installing "lm_sensors" on your system, run the command `sudo sensors-detect` to determine which kernel modules you need to load to use "lm_sensors" most effectively. It is generally safe and recommended to accept the default answers to all questions, unless you know what you're doing.

### Disable "Remember window size"

You need to disable "Remember window size" in the Konsole (terminal emulator).

Following on Konsole "Settings" -> "Configure Konsole...".

### Make the Script Executable

```
chmod +x show_sensors
```

**TIP:** To test `./show_sensors`.

### Create a shortcut (KDE, a suggestion)

Follow "System Settings" > "Keyboard" > Shortcuts > "Add New" > "Command or Script...".

Add the command (eg: "/home/myuser/.scripts/show_sensors").

Add the keyboard shortcut ("Add custom shortcut") (eg: "Alt+Shift+S").

## Final considerations

In reality, this script can be adapted to any other CLI application and any other terminal emulator.

In this example, we use the "htop" application, which is started with "root" credentials...

```
konsole -p tabtitle="MY SUDO HTOP SHORTCUT" -e bash -c "sudo htop" &
```

**NOTE:** The strategy that uses the value in `tabtitle="MY SUDO HTOP SHORTCUT"` (Konsole) is so that "wmctrl" applies the adjustments to the console window as soon as possible and in a guaranteed way, but `xdotool` can use other search strategies. More details in the code itself.

## Future

- Parameterize the script so that it can be easily used with other commands.
- Allowing the window to be positioned in nine possible predefined positions: top left diagonal, top centered, top right diagonal, centered left, centered, centered right, bottom left diagonal, bottom centered and bottom right diagonal.

# About

Show Sensors 🄯 BSD-3-Clause  
Eduardo Lúcio Amorim Costa  
Brazil-DF  
https://www.linkedin.com/in/eduardo-software-livre/

![Brazil](./images/brazil.png)
