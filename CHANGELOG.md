# MewCapture changelog

All changes to MewCapture, newest first.

## v1.0.2

- On first launch MewCapture asks if this is your main PC or your second PC, and Get Started only shows the steps for that PC. You can switch it later in Updates and About.
- The second PC has a big Pick your overlay window button right on its screen. It shows your open windows with a picture of each, removes the background for you and shows a live preview with the slider under it.
- The projector window is now only for OBS. It's off unless you turn on Using OBS? Open the projector window, and recording, streaming and Clip That work without it. When it's open and no game is coming in yet, it shows our logo and Waiting for the game.
- Fixed the second PC freezing with a black box when you pressed Start receiving.
- If the PCs can't find each other after about 20 seconds, both PCs now show what usually fixes it, with the address box tucked away inside.
- You can send your main PC mic too, and it gets its own track in recordings.
- The overlay safety note shows once as a popup instead of staying on the main PC's screen.
- Start sending no longer shrinks the window. Press Small window if you want it smaller.
- The sound list shows every open app and remembers what you ticked.
- The second PC tabs have more room, and options you rarely need are behind More.
- New sharper guide pictures with the button to press marked in pink.

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
