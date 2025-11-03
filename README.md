# UrlToFile README

<img src="Media/LLLogo.gif" width="100" height="100"> <img src="Media/ascii-art-text.png" width="400" height="400">

Right click Copy saved to a file useful if you have to create a file with alot of urls in it

## Installation ##

Download latest release and extract to a folder on your pc.

Require's Windows DOT NET V4.8 Works on Windows 7 / 8 /10 / 11

Open a Window's Terminal / Windows Command Prompt

## Usage ##
There is a slight delay before first url is grabbed to give you time to setup the browser etc

```command
urltofile -o then $"filename" 
          -v for verbose output
          -r to replace the file

urltofile -o $'filename' -v for verbose add -r if file exists 
utltofile -o $'filename' 

```

## Example Windows Batch File
```command
@echo off

if [%1]==[] (
		goto nofilegiven
)
@urltofile -o $%1 -r -v

if errorlevel 1 goto error
if not exist %1 goto error

goto end
:nofilegiven
echo "sorry a file is required eg: urlname"
goto end

error
echo "sorry issues with mp3 url creation try urltofile -h"
:end

```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.
## License

https://img.shields.io/badge/LegionLost

[MIT](https://choosealicense.com/licenses/mit/)
