# How to check downloaded big files

Ensure the integrity of large downloaded files by comparing their SHA-256 hash with the correct one. If they match, the download is error-free. In Windows, use PowerShell’s get-filehash filename to calculate the SHA-256 hash. For example, Windows user John calculates the SHA-256 hash for the downloaded VirtualBox ova-file ‘LE18SERVER.ova’.
```
C:\Users\john>powershell get-filehash c:\Users\john\Downloads\LESERVER18LTS.ova

Algorithm       Hash                                                                     Path
---------       ----                                                                     ----
SHA256          B3C79B8EDABA737D195EC2A688A93CC0D2A4730DB8F458841E7DDF2C2AE88253        C:\Users\john\Downloads\LESERVER18LTS...
C:\Users\john>
```
If the hash matches the given correct one then your downloaded file is non-corrupted. Instead of visually comparing the hashes, you can copy the your calculated hash and paste it to this tool [hashceck](https://averkoc.github.io/hash.html) into hash2-textbox.


