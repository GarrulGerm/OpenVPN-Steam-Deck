# OpenVPN-Steam-Deck
Works for Desktop mode and emulators.


1. .ovpn cert from a private server of your choice. (this is not a guide on hosting an OpenVPN Private server for PPSSPP on SteamDeck)
2. For the sake of simplicity please leave your .ovpn file in your Downloads folder. You may move it wherever you wish after.

Steps:
1. Navigate to the desktop environment on your Steam Deck and download PPSSPP from the discover tab
2. In "Applications" under "System" Select "Konsole" and enter the following commands to enable package installation on your SteamDeck.

    
    I. Enter the command `passwd` to create a root password. Do not forget it. 
    
    II. Make SteamOS readable: `sudo steamos-readonly disable`
    
    III. The pacman keyring must be initialized: `sudo pacman-key --init`
    
    IV. Now populate the keyring using: `sudo pacman-key --populate archlinux`
    
    V. You can now install packages on your Steam Deck: `sudo pacman -S openvpn` and confirm your installation
    
    VI. Once the terminal is done you may install networkmanager: `sudo pacman -S networkamanager-openvpn` and confirm your installation
    
    VII. If required packages are done installing and there were no error messages displayed enter the following.
    
    VIII. Navigate to your downloads in terminal using `cd`, `ls`, and `cd Downloads/`. Alternatively, you may simply browse to that file path in dolphin, right click in             the filespace, and select "open in terminal"
    
    IX. Enter the following into terminal: `nmcli connection import type openvpn file YOUR.ovpn` You should see a confirmation in the bottom right hand side of your screen.
    
    VIII. Navigate to your downloads in terminal using 'cd', 'ls', and `cd Downloads/`. Alternatively, you may simply browse to that file path in dolphin, right click in             the filespace, and select "open in terminal"
    
    IX. Enter the following into terminal: 'nmcli connection import type openvpn file YOUROVPN.ovpn' You should see a confirmation in the bottom right hand side of your             screen.

    X. IMPORTANT make steamos readonly: `sudo steamos-readonly enable`

    XI. Enjoy! You may need to follow additional settings or steps for your respective private server.

    XII. Untested: Add Konsole as a non-steam game in game mode. Open konsole and run: `nmcli connection up YOUR.OVPN` this may allow the use of Openvpn in game mode.
