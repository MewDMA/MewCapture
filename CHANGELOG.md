# MewCapture changelog

All changes to MewCapture, newest first.

## v1.0.9

- Streaming and Clip That stopped with MC-206 when a sound was set to Own track and file. That file is only for recordings and now only gets made while you record.
- Recording no longer fails over and over (MC-206) on PCs with two graphics chips: MewCapture tests the encoder the way the recording really uses it and picks one that works.
- After an update the second PC played no sound until you turned on Hear it on this PC. It's on now.
- Hear it on this PC no longer plays your main PC mic out loud or your second PC apps twice.
- The projector shows the whole game picture like the Scenes preview, and Scenes now tells you the size of the picture coming from the main PC.
- The projector's Minimize, Fullscreen and Close bar no longer gets stuck on the second PC's screen, and the hidden projector stays hidden at exactly your output size.
- Test my connection no longer always picks Max, cable only. It stays on Balanced or lower unless the PCs share a direct cable.
- Stop recording and Stop streaming stop again when nothing else is on.
- A webcam with its background blurred or removed isn't squashed anymore, and own track files from a recording that restarted aren't overwritten.

## v1.0.8

- MewCapture looks like mewdma.net now: a dark space background, violet and pink accents, Space Grotesk headings and Inter for everything else, without the glows. Everything works the same as before, every MC error code too.
- Sound only: the main PC can send just the sound you pick, no picture. Pick Sound only under What to Send.
- The second PC shows Getting the sound and puts it in the mixer like always. Start recording saves an .m4a with just the sound by itself, or stream your scenes with that sound under them.
- Simpler, one switch for each thing:
  - Hear it on this PC (in Audio) is the only switch for hearing the sound on the second PC, Sound only too. It replaces Listen to the recording and the speakers switches.
  - Using OBS is one switch in Output. It opens the projector and sends the sound to OBS, no separate sound switch.
  - Own track is picked only in the second PC's mixer, not on the main PC too.
  - Your overlay is set up only in Your Overlay at the top. Scenes points there instead of having its own copy, and the background color moved to its More options.
  - The Get Started list on Home is gone, the Start guide does that job.

## v1.0.7

- Recording works again. It said MC-205 and saved nothing because the encoder check and the recording needed the projector to keep changing, and a still picture (waiting for the game, a paused game) stopped both. Clip That had the same cause and saves clips again.
- The Scenes preview is the live game now, smooth and sharp, instead of a still picture a few times a second.
- Picking a preset selects it right away with a check mark, and the confirmation stays put instead of jumping.
- The mixer holds its layout in a small window, and own track now also saves that source as its own file.
- Listen to the recording: hear exactly what your recording gets.
- The main PC asks plainly what to send: the whole screen (and which one) or one window.
- The second PC can start sending on the main PC when MewCapture is open there.
- Clearer connection help: both PCs on the same router or a direct cable, in the Start guide too, and the PC list just says Connected or Not connected.
- Output shows how many Mbps and GB per hour your size, fps and quality add up to.
- Click any guide picture to see it big.
- MewCapture opens at its normal size again after using Small window, the main PC stays on Balanced unless you change it, and both clip buttons say Clip That.
- Removed things that confused people: the speakers option in the mixer and the anti-cheat line in Something's Wrong.

## v1.0.6

- The Second PC just says it's getting the game and at how many fps, without HEVC, Mbps or a delay next to it.
- No more delay or ping numbers in the projector stats or the ticket summary either, they only measured a tiny ping between the PCs.

## v1.0.5

- Something's Wrong has the Fix it button for the firewall again, right under the problem.
- The summary in Something's Wrong is a plain text block you can select, and Copy the summary is its own button that says Copied when it's on your clipboard.
- Every Copy button works the same way now and never selects or moves the text next to it.
- The second PC no longer shows a delay in milliseconds, since that number only measured a tiny ping between the PCs and wasn't the delay you see.

## v1.0.4

- Start guide on Home: pick main PC or second PC and it walks you through the setup, picking the encoder, quality, scenes and sound for you.
- The safety popup now shows the first time you pick main PC or second PC too, not only when you switch.
- No more "couldn't find a video encoder" while it's sending fine. It checks NVIDIA NVENC, AMD AMF, Intel QuickSync (built-in graphics) and the CPU, and shows which one it uses.
- The projector is always fullscreen. Its bar shows when you hover near the top edge and hides when you move away, and Minimize moves it out of your way while OBS keeps getting it.
- Set up OBS for me handles every case: OBS not installed (we link to obsproject.com), closed, open with or without WebSocket, live or recording, and a MewCapture scene collection that's already there. It never changes your other scene collections.
- Send the sound to OBS without playing it on the second PC's speakers.
- The mixer on the second PC takes any app as a source. You can rename everything and keep any source in the mix, on its own track or in its own file. Push to talk and the second PC mic are gone, the mic comes from the main PC.
- Scenes have a sharp preview in the right shape, and the lock only locks. Switch scenes automatically is gone.
- Chat can pop out into its own window or dock to the side of MewCapture.
- Every dropdown looks like the rest of the app.
- Removed Start receiving when MewCapture opens, Forget them and the Network section. Getting the game shows its numbers right in the status line.

## v1.0.3

- The old overlay warning is gone, it also went off for things like Snipping Tool. The red warning now only shows when the second PC's output comes back to the main PC: MewCapture's output or the projector on a PC with an anti-cheat, or OBS on the main PC with the projector, NDI or a stream from the second PC in it. Anti-cheats take screenshots of the main PC and scan them, also with AI, for things like ESP, so the overlay only ever runs on the second PC.
- Sound categories: put your apps into Game, Communication, Music, Browser, Other or your own. For each one pick if it plays on the main PC or the second PC and if recordings keep it on its own track. MewCapture remembers it.
- Small window turns into Big window, so you can get back, and Stop sending brings the normal size back too.
- Switch to main PC or second PC is a big button at the top of Updates and About.
- Home has the same four cards in one line, Guides always included.
- Something's Wrong has Check again at the top and Copy the summary above the summary.
- Dropdowns look like the rest of the app, and the main PC lost its More info bits.

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
