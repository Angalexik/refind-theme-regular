# rEFInd theme Regular Nord

A simplistic clean and minimal theme for rEFInd using the Nord color palette

 **press F10 to take screenshot**
 
(default settings)
![Screenshot 01](https://raw.githubusercontent.com/bobafetthotmail/refind-theme-regular/master/src/white_theme.png )

(dark theme selected)
![Screenshot 02](https://raw.githubusercontent.com/bobafetthotmail/refind-theme-regular/master/src/dark_theme.png)



### Installation [Quick]:

1. Just paste this command in your terminal and enter your choices.
   ```
   sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/bobafetthotmail/refind-theme-regular/master/install.sh)"
   ```
2. To further adjust icon size, font size, background color and selector color edit `/boot/efi/EFI/refind/refind-theme-regular/theme.conf` as root/SuperUser.

### Installation [Manual]:

1. Clone git repository to your $HOME directory.
   ```
   git clone https://github.com/bobafetthotmail/refind-theme-regular.git
   ```

2. Remove unused directories and files.
   ```
   sudo rm -rf refind-theme-regular/{src,.git}
   ```
   ```
   sudo rm refind-theme-regular/install.sh
   ```

3. Locate refind directory under EFI partition. For most Linux based system is commonly `/boot/efi/EFI/refind/`. Copy theme directory to it.

   **Important:** Delete older installed versions of this theme before you proceed any further.

   ```
   sudo rm -rf /boot/efi/EFI/refind/{regular-theme,refind-theme-regular}
   ```
   ```
   sudo cp -r refind-theme-regular /boot/efi/EFI/refind/
   ```

4. To adjust icon size, font size, background color and selector color edit `theme.conf`.
   ```
   sudo vi /boot/efi/EFI/refind/refind-theme-regular/theme.conf
   ```

5. To enable the theme add `include refind-theme-regular/theme.conf` at the end of `refind.conf`, and comment out or delete any other themes you might have installed.
   ```
   sudo vi /boot/efi/EFI/refind/refind.conf

   ```

**NOTE**: If your not geting your full resolution or have color issues then try disabling the CSM in your UEFI settings.

**More information**

[rEFInd](http://www.rodsbooks.com/refind/) The official rEFInd website
