## UrlToFile README

<img src="Media/LLLogo.gif" width="110" height="110"> <img src="Media/ascii-art-text.png" width="600">

Right click Copy saved to a file useful if you have to create a file with alot of urls in it

## Installation ##

Download the latest release and extract to a folder on your pc.

Require's Windows
<a href="https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net481-offline-installer">
  <img src="Media/logo_net.svg" width=20 height=20>
</a>
 V4.81 Works on Windows 7 / 8 /10 / 11


Written in <img src="Media/logo_csharp.png" width=20 height=20> 

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

Check you have downloaded the latest version if there are any issues <a href="mailto:legionslost@proton.me?subject=urltofile">legionslost@proton.me</a> 
or you can support me via <a href="https://buymeacoffee.com/legionslost"> <img src="Media/bmc.webp" width=50 height=50> <img src="Media/qr-code.png" width="100" height="100"></a>

