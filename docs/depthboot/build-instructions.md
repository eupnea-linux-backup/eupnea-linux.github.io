# Build instructions

1. Open a terminal, clone the repo and start the script with this command:
    ```shell
    git clone --depth=1 https://github.com/eupnea-project/depthboot-builder && cd depthboot-builder && ./main.py
    ```
2. Follow the instructions inside the terminal.

3. Flash the created image file to a USB drive/SD-card using Etcher, ``dd`` or any other tool. If you are using Rufus,
   read [this](/docs/extra/rufus) first.
    - If the script was run within Crostini, copy depthboot.bin to a folder that is accessible from ChromeOS's Files
      App, then [flash](https://www.virtuallypotato.com/burn-an-iso-to-usb-with-the-chromebook-recovery-utility/) it
      using the Chromebook Recovery Utility extension.

4. Open the ChromeOS shell by pressing <kbd>CTRL</kbd><kbd>ALT</kbd><kbd>T</kbd>, type `shell` and press <kbd>
   Enter</kbd>.
    - If you get an error about `shell` not being a command:
      [Enable developer mode](https://www.androidauthority.com/how-to-enable-developer-mode-on-a-chromebook-906688/) and
      try again.

5. Inside the ChromeOS shell enable USB and Custom Kernel Booting by pasting the command below and pressing <kbd>
   Enter</kbd>.
    ```shell
    sudo crossystem dev_boot_usb=1 dev_boot_signed_only=0
    ```

6. Reboot with the USB drive/SD card plugged in and press <kbd>CTRL</kbd><kbd>U</kbd> or select "Boot from external
   disk".

After a black screen Depthboot will boot.

7. Please consider starring the [depthboot](https://github.com/eupnea-project/depthboot-builder) repo on GitHub to help
   us reach more people.
