# MewCapture changelog

All changes to MewCapture, newest first.

## v1.0.1

- All the text in the app, the guide and the docs got rewritten so it reads like we'd tell you in a ticket.
- Buttons now say exactly what they do, like Start sending, Start receiving and Save clip.
- The second PC now picks up a stream that's already running more reliably, since the main PC sends the video settings with every keyframe.
- Bug reports go into their own MewCapture inbox on our site.
- The public repo now looks like MewTools, with the guide, screenshots and our security page in docs.

## v1.0.0

- First release. MewCapture lets you record or stream your game with your overlay on it, no capture card needed, just install it on both PCs.
- The main PC sends the screen or game window through your graphics card's encoder (HEVC or H.264) at low priority and shows how little it uses. You pick which apps you hear, and Discord gets its own track. It never touches the game, and it warns you if an overlay runs on the main PC.
- The second PC has scenes with the game, your overlay (we remove its background for you, with a live preview), your webcam with background blur, images, text, countdowns, browser sources and a keys and mouse overlay. It also has studio mode, scene hotkeys, cut, fade and move transitions, and scenes can switch when a game opens.
- You can record, stream to Twitch, YouTube and Kick at the same time, or capture the projector in OBS, and Set up OBS for me does that part for you.
- Clip That works on either PC, with the overlay or clean, and you can trim a clip before saving and send a clean one to the main PC.
- The mixer has meters, mute and push to talk, and recordings keep the game, your mic and Discord on separate tracks.
- The PCs pair once with a 4-digit code, then find each other and reconnect on their own over Wi-Fi, Ethernet or a cable.
- Something's Wrong checks both PCs and the connection and makes a summary for a ticket.
