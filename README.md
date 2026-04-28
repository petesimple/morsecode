Morse Code Trainer

A simple browser based Morse code trainer, sender, and listener built for GitHub Pages.

Type text and convert it to Morse. Play Morse as audio. Send manually with a keyboard or on screen tap button. Use the microphone listener to hear Morse tones and translate them in real time.

No login. No backend. No nonsense. Just dots, dashes, beeps, and a little radio goblin energy.

Live App

Add your GitHub Pages link here after publishing:

petesimple.github.io/morsecode/

Features

Text to Morse

Type regular text and convert it into Morse code.

Example:

SOS PETE

Becomes:

... --- ... / .--. . - .

Morse to Text

Paste or type Morse code and decode it back into readable text.

Use spaces between letters and a slash between words.

Example:

.... . .-.. .-.. --- / .-- --- .-. .-.. -..

Becomes:

HELLO WORLD

Audio Playback

Play converted Morse code as beeps from the browser.

Adjustable settings include:

* Speed in WPM
* Tone frequency in Hz
* Playback volume

Manual Sending

Send Morse manually using:

* The big on screen press and hold button
* The spacebar by default
* A custom assigned keyboard key

Short press equals dot.
Long press equals dash.
Pauses are used to detect letters and words.

Live Decode

The app watches your press timing and translates your manual Morse into text live.

It detects:

* Dot
* Dash
* Letter gap
* Word gap

Assignable Key

The default send key is:

Spacebar

You can assign another key inside the Settings panel.

This can be useful for external keyboards, arcade buttons, accessibility switches, or controller style inputs that map to keyboard keys.

Microphone Listener

The app can use the device microphone to listen for Morse tones and translate them live.

This works best when:

* The tone is clear
* The sound source is close to the microphone
* Background noise is low
* The threshold is adjusted so the green light turns on only during the beep

The mic listener includes:

* Start Mic Listener button
* Stop Mic button
* Signal level meter
* Tone threshold slider
* Mic unit timing control
* Live mic symbol buffer
* Live mic decoded message

Important Mic Note

The current microphone listener is a first pass volume based detector.

That means it listens for sound level above a threshold, then uses timing to decide whether the tone was a dot or dash.

It does not yet isolate a specific Morse frequency. Loud room noise, claps, voices, or music may confuse it.

A future version could add pitch filtering so the app listens mostly for a selected tone, such as 600 Hz or 700 Hz.

Recommended Testing

Test Text Conversion

1. Type a short message in the Text to Morse box.
2. Press Convert to Morse.
3. Press Play Morse.
4. Confirm the Morse output appears and plays as audio.

Test Manual Keying

1. Use the big Press and Hold button.
2. Tap quickly for dots.
3. Hold longer for dashes.
4. Pause between letters.
5. Watch the Live Decode panel.

Test Keyboard Sending

1. Click outside any text input.
2. Press and hold the spacebar.
3. Release to create a dot or dash.
4. Use Settings to assign a different key if desired.

Test Microphone Listener

1. Open the app on one device.
2. Press Start Mic Listener.
3. Play Morse beeps from another device nearby.
4. Adjust Tone Threshold until the green light turns on only during the beep.
5. Adjust Mic Unit MS if dots and dashes are not being detected correctly.

File Structure

The first version can run as one file:

index.html

Optional future PWA files:

manifest.json
service-worker.js
icons/

GitHub Pages Setup

1. Create a new GitHub repository.
2. Add the app as index.html.
3. Commit and push the file to the main branch.
4. Open the repository settings.
5. Go to Pages.
6. Choose Deploy from branch.
7. Select main and /root.
8. Save.

GitHub will publish the app at a URL similar to:

https://yourusername.github.io/morse-code-trainer/

Browser Support

The app is designed for modern browsers, including:

* Chrome
* Edge
* Safari
* Firefox
* Mobile Safari
* Chrome on Android

Microphone access requires HTTPS. GitHub Pages uses HTTPS, so the mic listener should work once the app is published.

Some browsers may require the user to interact with the page before audio playback begins.

Settings Saved Locally

The app saves settings in the browser using localStorage.

Saved settings include:

* WPM
* Tone frequency
* Volume
* Assigned key
* Mic threshold
* Mic unit timing

No data is sent to a server.

Roadmap Ideas

Future improvements could include:

* Pitch filtered microphone listening
* Practice quizzes
* Random letter drills
* Call sign practice
* Koch method training
* Farnsworth timing
* PWA install support
* Offline caching
* Gamepad button support
* Visual waveform display
* Export practice history
* Multiple tone profiles

License

Add your preferred license here.

Common choice:

MIT License

Built For

People learning Morse code, radio nerds, musicians who like timing games, accessibility experiments, and anyone who thinks a beep can become a sentence.
