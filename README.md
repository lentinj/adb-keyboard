# Interactive ADB keyboard

Small script to send keypresses over an ADB shell to any Android phone, e.g. to use your laptop keyboard to compose SMS.

It's not pretty, and the ``input`` command this uses has a number of shortcomings:

* Running the command takes ~1s, meaning latency is quite high. Characters are batched to try and lessen this, but you're going to have to be a good touch-typer.
* Non-ASCII characters are not supported. https://stackoverflow.com/questions/14224549/adb-shell-input-unicode-character

There are much more sensible ways of doing this, but they all require switching to a virtual keyboard (and back again when you're done). And I don't speak unicode so that won't annoy me.

## Prerequisites

The script requires Python 3. Not tested with Python 2, but might work.

## Usage

Enable ADB on your phone and connect. Run ``adb-keyboard`` and start typing. Ctrl-C to finish.

There are some special key combinations listed at the top of the script.
