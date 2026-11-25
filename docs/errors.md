# MewCapture error codes

Made from `app/shared/errors.json`. Every error in the app has one of these codes, with its fix.

## Main PC

| Code | Message | Why | Fix |
|---|---|---|---|
| MC-101 | We couldn't find a video encoder that works on this PC. | None of NVENC (NVIDIA), AMF (AMD), QuickSync (Intel built-in graphics) or the CPU encoder would start, which usually means the graphics driver is old or broken. | Update your graphics driver from NVIDIA, AMD or Intel, restart the PC and try again. |
| MC-102 | We couldn't capture {what}. | Windows didn't let us capture it, which happens when the window got closed or minimized or the game blocks other apps from capturing it. Screen can't be captured either while the PC is locked or a Windows prompt that asks for admin rights is open. | Make sure the window is open and not minimized, unlock the PC and close any Windows prompt, then press Start sending again. If you picked a game window, try Screen instead. |
| MC-103 | The stream keeps stopping, we keep starting it again for you. | Capturing or encoding crashed 5 times in a row: {detail} | Leave it running, it picks back up when it can. If it doesn't, update your graphics driver or pick a lower quality or 30 fps. |
| MC-104 | We couldn't grab the sound from {app}. | Sound from single apps needs Windows 10 version 2004 or newer and the app has to play its sound through Windows, and your mic has to be plugged in and not taken over by another app. | Update Windows or tick All PC sound instead, and for your mic replug it and check it's the one picked under Sound. The video still gets sent either way. |
| MC-105 | We didn't find your second PC. | MewCapture isn't open on the second PC, Start wasn't pressed there, or the two PCs are on different networks. | Open MewCapture on the second PC, go to Second PC and press Start receiving, then search again. You can also type the address from its Connect tab under Type the address yourself. |
| MC-106 | That address doesn't look right. | It has to look like 192.168.1.20, the address the second PC shows on its Connect tab under This PC. | Copy the address from the second PC and try again. |

## Second PC

| Code | Message | Why | Fix |
|---|---|---|---|
| MC-201 | Receiving keeps stopping, we keep starting it again for you. | The receiver stopped: {detail} | Close other apps that might use port 47801, then stop and start receiving again. If it keeps happening, restarting the PC fixes most of these. |
| MC-202 | We couldn't capture your overlay window. | The window got closed or minimized, or your overlay blocks other apps from capturing its window. | Open your overlay, make sure it isn't minimized and add it again. |
| MC-203 | We couldn't save in that folder. | The folder doesn't exist anymore, the drive is full or Windows blocks saving there. | Pick another folder, like your Videos folder, and try again. |
| MC-204 | We couldn't open the firewall for MewCapture. | Your antivirus or the settings of a work or school PC blocked us from adding the rule to Windows Firewall, so the main PC might not be able to reach this PC. | Allow MewCapture in your antivirus or firewall for private and public networks, then press Fix it again. On a work or school PC, whoever manages it has to allow ports 47800 to 47802. |
| MC-205 | The recording isn't getting a picture from the projector. | The projector window is closed or minimized, or this PC's graphics driver can't capture windows. | Stop receiving and start it again so the projector opens again. If it still says this, turn on Using OBS in Output to see the projector, then update your graphics driver. |
| MC-206 | The recording kept stopping, so we stopped it. | Capturing or encoding on this PC crashed 5 times in a row: {detail} | Pick a lower size or fps or Small files, and update this PC's graphics driver. |
| MC-207 | Turn on the clip buffer first. | Clips come from the last seconds MewCapture keeps, and that's off right now. | Turn on With overlay or Clean in the Clips tab, or pick the Clips only preset. |
| MC-208 | We couldn't save that clip. | The clips folder is full or blocked, or nothing was kept yet. | Wait a few seconds after you start and try again, or pick another save folder. |
| MC-209 | We couldn't find OBS on this PC. | OBS isn't installed, or it's the portable version that keeps its settings in its own folder. | Install OBS from obsproject.com, open it once and press Set up OBS for me again. For portable OBS, add a Window Capture of MewCapture Projector yourself. |
| MC-210 | Another app is using port 47800, so we can't start receiving. | MewCapture finds the main PC through that port, and another app on this PC already has it, most of the time another MewCapture that's still running. | Close the other MewCapture from its tray icon, or the app that uses port 47800, then press Start receiving again. If you can't find it, restarting the PC fixes it. |
| MC-211 | The stream to {name} dropped, we keep connecting it again for you. | The connection to {name} stopped or got refused: {detail} | Check your internet, and the server and stream key in Output. Your recording and clips keep going meanwhile. |

## Network

| Code | Message | Why | Fix |
|---|---|---|---|
| MC-301 | Windows Firewall isn't letting the main PC in yet. | The rule that lets the main PC reach this PC on ports 47800 to 47802 is missing, or Windows has another rule for MewCapture that blocks it. | Press Fix it and we put our rules back, which only let other PCs reach MewCapture on this PC. |
| MC-302 | This PC is only connected through a VPN. | A VPN sends everything through its own network, so the other PC can't be found. | Turn the VPN off or turn on its option to allow the local network (LAN), then search again. |
| MC-303 | A VPN is on, {name}. | Some VPNs hide your home network, so the two PCs can't find each other. | If the other PC isn't found, turn the VPN off or allow the local network (LAN) in its settings. |
| MC-304 | The main PC is on Wi-Fi. | Wi-Fi works, but drops and delay show up as stutter on the second PC. | Plug the main PC into your router with a cable, or use a cable between the two PCs, Direct cable in the guide shows how. |
| MC-305 | Your PCs can't see each other on this network. | Most of the time Start wasn't pressed on the second PC, one PC is on a guest network, or the router keeps devices apart (AP or client isolation, common on guest Wi-Fi and some mesh systems). | Press Start receiving on the second PC and put both PCs on your main network, not the guest one. If that doesn't help, turn off AP or client isolation in your router or use a cable between the two PCs. |
| MC-306 | This PC isn't connected to a network. | We didn't find a network cable or Wi-Fi connection that's turned on. | Plug in the network cable or turn on Wi-Fi, then check again. |
| MC-307 | The link between your PCs is dropping packets. | Wi-Fi on either PC, a busy network or a long or damaged cable loses some of the stream, and that shows up as stutter on the second PC. | Use a cable to your router or a direct cable between the two PCs, or pick a lower quality on the main PC. |
| MC-308 | That main PC stopped asking to connect. | We haven't heard from it for more than 2 minutes, most of the time because MewCapture closed there or the PC went to sleep. | Open MewCapture on the main PC and say yes here when it asks again. |

## Safety

| Code | Message | Why | Fix |
|---|---|---|---|
| MC-402 | Your main PC is getting the second PC's output. | MewCapture's output or the projector is running on this PC, and {name} runs here, so it's the PC you game on. Anti-cheats take screenshots of the main PC and scan them, also with AI, for things like ESP, so the overlay only ever runs on the second PC. | Press Stop receiving here and record or stream on the second PC. The main PC only ever sends the game to the second PC, never the other way. |
| MC-403 | OBS on your main PC has the second PC's output in it. | Its scenes have {what}, so your overlay ends up on the main PC's screen. Anti-cheats take screenshots of the main PC and scan them, also with AI, for things like ESP, so the overlay only ever runs on the second PC. | Remove that source from OBS on the main PC and record or stream on the second PC, with MewCapture or OBS there. |

## App

| Code | Message | Why | Fix |
|---|---|---|---|
| MC-601 | Some MewCapture files are missing. | Your antivirus most likely removed {file}. | Reinstall MewCapture, and if it happens again add the MewCapture folder as an exception in your antivirus. |
| MC-611 | Something went wrong: {detail} | We didn't expect this error. | Try again, and if it keeps happening send us a report with Report a bug or idea or open a ticket in our Discord. |
