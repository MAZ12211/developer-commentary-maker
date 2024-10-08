Quick steps on how to use it:
1- Download [this template](https://github.com/MAZ12211/dev-commentary-maker/blob/main/data/songs/tutorial/dev-commentaries/normal-default-devCom.json)
2- Place it in `yourmod/data/songs/yoursong/dev-commentaries`.
3- Rename the file name with your own difficulty and variation.
Remember that this is difficulty and variation dependent meaning
let's say you want to have a dev commentary for a song called `philly-nice` in the normal difficulty.
Your file name should be called `normal-default-devCom.json`.
Here's how it works:
the first part is the difficulty name found in the metadata file.
the second part is the variation defaulted to default.

Example with an erect remix:
Pico erect remix in the erect difficulty:
data/songs/pico/dev-commentaries/erect-erect-devCom.json (for nightmare it's `nightmare-erect-devCom.json`)

Example with a playable character
Philly Nice Pico mix in the hard difficulty:
data/songs/philly-nice/dev-commentaries/hard-pico-devCom.json

4- Launch the game and play your song.
5- If you see a visual indicator that looks like a text bubble in the bottom left corner of the screen, you should be able to get a new button in the pause menu called `Developer Commentary`.

JSON STRUCTURE
`authors` and `commentary` are self explanatory.

`images` has `path`, `desc`, `x`, `y`.
You put your image name in `path` field.
let's say you have an image called `conceptArt.png`
You have to put it in the `path` field as `conceptArt`. It'll will look for `data/songs/yoursong/dev-commentaries/conceptArt.png`
Make sure you don't include the extension name by accident!

`desc` is the image description.
Use it if you have something to comment about the image itself.

`x` and `y` are self explanatory.
if you don't want to deal with manual placements, my script will try place them after the commentary text with rough spacing.

Helpful tips!
Use F5 to check how the commentary looks in-game quickly if you're done writing and are busy with formating.
If your game says something along the lines of `invalid char X at position X`, use a JSON validation tool such as [jsonlint](https://jsonlint.com/). It'll tell you what's wrong with it.
`Images` is entirely optional, you can remove it in the json file and just want to have `authors` and `commentary` only.
This script isn't limited to work with only base game difficulties, it can work with your own difficulties **as long as that custom difficulty is included in the metadata**, it should work fine without too much instability.
Use `\n` to make new lines in case your text went off the screen.
Use `\"qouted text\"` is used to make qouted text.

Limitations & Known issues
You can't scale the images easily in the script
If the image is too big (game's screensize is `1280x720`) you have to manually scale them down in an image resizer online.
The example images' size in the template is `640x340`, it works well if you want a fixed size without too much time spent on trial and error.

There's no way for the player to know if your song has a dev commentary or not outside of `PlayState` (the screen you're playing the song in)
There'll be a better visual indicator in Freeplay once I figure out how to lol
