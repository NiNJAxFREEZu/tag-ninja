# tag-ninja
Automatic FLAC audio recognition and tagging using AudD API.

## How it works
Takes a splice of the given `.flac` audio track, sends it to AudD audio recognition API and tags it based off information provided in the response `json` file.

To keep `.flac` file small, `tag-ninja` only tags the most important information about the track - all of them are listed below:
- Track title
- Album title
- Artist
- Track number
- Total track count in the album
- Album cover (soon™)

## Before you use

## How to use
Run the executable and give path to audio track you want to tag as the first and only argument

For example:
```bash
$ ./tag-ninja track01.flac
```

## Dependencies
- curl (HTTP requests)
- flac (`.flac` file support and tagging utility)
- jq (json processing)

All dependencies are available in most major distros repositories.
