# ScreenshotBOF

An alternative screenshot capability for Cobalt Strike that uses WinAPI and does not perform a fork & run. Screenshot downloaded in memory.

## Self Compilation
1. git clone the repo
2. open the solution in Visual Studio
3. Build project BOF

## Usage
1. import the screenshotBOF.cna script into Cobalt Strike
2. use the command screenshot_bof {local filename}
```
beacon> screenshot_bof sad.bmp
[*] Running screenshot BOF by (@codex_tf2)
[+] host called home, sent: 4860 bytes
[+] received output:
[*] Tasked beacon to printscreen and save to sad.bmp
[+] received output:
[+] PrintScreen saved to bitmap...
[*] started download of sad.bmp
```

## Notes
- no evasion is performed, which should be fine since the WinAPIs used are not malicious

## Why did I make this?
Cobalt Strike uses a technique known as fork & run for many of its post-ex capabilities, including the screenshot command. While this behaviour provides stability, it is now well known and heavily monitored for. This BOF is meant to provide a more OPSEC safe version of the screenshot capability.

## Credits
- Made using https://github.com/securifybv/Visual-Studio-BOF-template
- Save BMP to file from https://stackoverflow.com/a/60667564
- in memory download from https://github.com/anthemtotheego/CredBandit