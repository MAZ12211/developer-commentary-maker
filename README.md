# Dev Commentary Maker

This is a utility mod that lets fnf modders add their own dev commentaries to any song in the mod without too much setup and code.

This is difficulty dependent meaning you can make the dev commentary from the easy difficulty be different from the hard difficulty.
This is done in charters' favor to comment on (for example) their favorite charting moments in the song
or how they placed the mines cleverly in the song to be enjoyable/satisfying for the player
or how they handled charting multiple difficulties.

This is also because of Erect and Nightmare (or alternative variation) difficulties that may have different music and visuals.

You can also have images in your dev commentary if you want to talk about concept art for example.

## Quick steps on how to use it

1- Download [this template](https://github.com/MAZ12211/dev-commentary-maker/blob/main/data/songs/tutorial/normal-devCom.json)
2- Place it in `yourmod/data/songs/yoursong` (It's the same place that has the chart and the metadata file)
3- Rename/replace the first part of the file name (`normal`) with your own difficulty
Remember that this is difficulty dependent meaning for example if you rename it to `hard-devCom.json`, your dev commentary won't show up in normal and easy difficulty.
So, you have to duplicate the file and rename it.
4- Launch the game and head to your song.
5- If you see a text bubble in the bottom left corner of the screen, you should be able to get a new button in the pause menu called `Developer Commentary`.

## JSON STRUCTURE

`authors` and `commentary` are self explanatory.

`images` has `path`, `desc`, `x`, `y`.
You put your image name in `path` field.
let's say you have an image called `conceptArt.png`
You have to put it in the `path` field as `conceptArt`. It'll will look for `data/songs/yoursong/conceptArt.png`
Make sure you don't include the extension name by accident!

`desc` is the image description.
Use it if you have something to comment about the image itself.

`x` and `y` are self explanatory.
if you don't want to deal with manual placements, my script will try place them after the commentary text with frankly not so clean spacing.

## Helpful tips

Use F5 to check how the commentary looks in-game quickly if you're done writing and are busy with formating.
If your game says something along the lines of `invalid char X at position X`, use a JSON validation tool such as [jsonlint](https://jsonlint.com/).
`Images` is entirely optional, you can remove it in the json file and just want to have `authors` and `commentary` only.
This script isn't limited to work with only base game difficulties, it can work with your own difficulties **as long as that custom difficulty is included in the metadata**, it should work fine without too much instability.
Use `\n` frequently.
