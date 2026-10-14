# MewCapture security

MewCapture runs as admin on both PCs, because it adds a firewall rule so the other PC can reach it. Since it has that much access, we kept what it's allowed to do as small as we could. This page goes over how it captures the game, what goes over your network, how it runs FFmpeg and how updates get checked.

## The game and anti-cheat

On the main PC MewCapture only captures the screen or the game window, the same way Discord streaming does, with Windows Graphics Capture or DXGI desktop duplication. It never injects anything into the game, never puts a DLL in it, never hooks it and never reads its memory. For the keys and mouse overlay it only asks Windows which keys are held down, like any app can.

Your main PC is never the recording or streaming PC. Anti-cheats take screenshots of the main PC and scan them, also with AI, for things like ESP, so the overlay only ever runs on the second PC, and so do the projector, OBS, recording and streaming. Don't send the overlay or MewCapture's output back to the main PC to put your game under it there. MewCapture shows a red warning when its output or the projector runs on a PC with an anti-cheat, and when OBS or another streaming app runs on your main PC.

## Your network

The two PCs only talk on your own network or a cable between them. The main PC sends the game on UDP port 47801, the PCs find each other on UDP 47800, and clips go back to the main PC on TCP 47802. The firewall rule MewCapture adds on the second PC only opens those three ports.

A main PC can only send hotkeys, the input overlay or clips once you pressed Connect on the second PC and checked both show the same code. The app remembers which PCs you connected and ignores the rest. The local connection between the app and its projector window uses a random key that changes every time the app starts, so other apps on the PC can't read it.

Stream keys stay on the second PC in the app's own settings. They only ever get sent to the streaming site you picked, and bug reports and the Something's Wrong summary never include them.

## Running FFmpeg

Capture, encoding and recording run through FFmpeg, which comes with the app. When the app starts it, it hands over file names, window handles and settings as plain values and never types them into a command prompt, so a weird file or window name can't turn into a command. You won't see a console window pop up, and FFmpeg closes when the app closes, even if the app crashes.

## Downloads and updates

The only thing MewCapture downloads is its own updates, from the MewDMA/MewCapture releases on GitHub. Updates go through Tauri's built in updater and every update file is signed by us. The key that checks that signature is built into the app, so a fake or changed update can't install. The app checks for a new version when it starts and once a day, and never in the middle of a stream or recording.

## Bug reports

Report a bug or idea sends your message to mewdma.net, plus the PC info listed in the form, so you can see what gets sent before you send it. It never sends your PC name, Windows user name, window titles or stream keys.
