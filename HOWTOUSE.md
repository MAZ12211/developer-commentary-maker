# Quick steps on how to use it

1. [Use the example folder as a template](https://github.com/MAZ12211/developer-commentary-maker/tree/main/example/data/songs/philly-nice/dev-commentaries) to know the proper path on where to put your commentary files.
2. Rename the file name with your own.
The filename format goes like this: `difficulty-variation-devCom.json` and they're placed in `yourmod/data/songs/yoursong/dev-commentaries` if you haven't noticed yet in the example folder.
[Read the official FNF Modding Documentation if you're not sure what to replace the variation part.](https://funkincrew.github.io/funkin-modding-docs/02-custom-songs-and-custom-levels/02-04-what-are-variations.html)

## Examples

- `erect-erect-devCom.json` will work in the `Erect` difficulty `Erect` variation (Erect remix).
- `hard-pico-devCom.json` will work in the `Hard` difficulty `Pico` variation (for playable characters).
- `normal-default-devCom.json` will work in the `Normal` difficulty `default` variation (pretty much what you want if you don't plan on remixes or playable characters).

I hope you understand how it works now

---

4. Once you set up your commentary files and double check on the difficulty and the variation, launch the game and play your song.
5. If it works, you should see a visual indicator that looks like a text bubble in the bottom left corner of the screen which means there's a new button in the pause menu called `Developer Commentary`.

## JSON STRUCTURE

`authors` and `commentary` are self explanatory.

`images` has `path`, `desc`, `x`, `y`.
You put your image name in `path` field, with `data/songs/yoursong/dev-commentaries/` being the root path.
So if you have an image called `conceptArt.png`, you would put it in the `path` field as just `conceptArt`.
Make sure you don't include the extension name by accident!

`desc` is the image description.
Use it if you have something to comment about the image itself.

`x` and `y` are self explanatory.
if you don't want to deal with manual placements, my script will try placing them after the commentary text with rough spacing.

## Helpful tips

Use `F5` to hot reload your game to quickly check how the commentary looks in-game quickly if you're done writing and are busy with formatting.
If your game says something along the lines of `invalid char X at position X`, use a JSON validation tool such as [jsonlint](https://jsonlint.com/). It'll tell you what's wrong with it.
`Images` is, like mentioned before, entirely optional, you can remove it in the json file and just want to have `authors` and `commentary` only.
This script isn't limited to working with only base game difficulties, it can work with your own difficulties like `Mania` or something like that, **as long as that custom difficulty is included in the metadata**, it should work fine without too much instability.
Use `\n` to make new lines in case your text went off the screen.
Use `\"qouted text\"` is used to make qouted text.

## Limitations & Known Issues

- You can't scale the images easily in the script.
If the image is too big (the game's screensize is `1280x720`), you have to manually scale them down in an image resizer online.
The example images' size in the template is `640x340`, it works well if you want a fixed size without too much time spent on trial and error.

- There's no way for the player to know if your song has a dev commentary or not outside of `PlayState` (the screen you're playing the song in)
There'll be a better visual indicator in Freeplay once I figure out how to lol
