# tag-ninja
Automatic FLAC audio recognition and tagging using AudD API.

## How it works
Takes a splice of the given `.flac` audio track, sends it to AudD audio recognition API and tags it based off information provided in the response `json` file.

`tag-ninja` tags the most important information about the track - all of them are listed below:
- Track title
- Album title
- Artist
- Track number (album order)
- Album cover

## Before you use
Create an account at [AudD](https://audd.io) and generate an API token. This token will be necessary to make song recognition requests.
Then, place the token in a text file `tag-ninja\api_token`.  

By default `tag-ninja` looks for a token file named `api_token` in it's own directory. You can always change it by editing the source code, which I strongly recommend.

## How to use
Run the executable and give path to audio track you want to tag as the first and only argument

For example:
```bash
$ ./tag-ninja track01.flac
```

## Dependencies
- curl (HTTP requests)
- flac (`.flac` file support and tagging utility)
- jq (`json` file processing)

All dependencies are available in most major distros repositories.

## Known issues
Since [AudD](https://audd.io) response `json` does not always have the same structure, some of the time `tag-ninja` is unable to get the album cover. I will be patching this soon.

## Special thanks
Thanks for [AudD](https://audd.io) for providing me free extra requests for additional testing.
