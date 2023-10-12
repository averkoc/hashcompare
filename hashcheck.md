# How to check downloaded big files

It is good practise to check the integrity of downloaded big files to prevent using corrupted files. If the file's correct hash-value (e.g. SHA-256 hash) is available you should calculate the downloaded files hash-value and compare it to the correct one. If they are the same then your download 
have succeeded without errors.

You can calculate the SHA-256 hash for a file in Windows by using powershell and command **get-filehash filename**. Below is an example how Windows user john calculates the downloaded VirtualBox ova-file's LE18SERVER.ova SHA-256 hash.  

```
C:\Users\john>powershell get-filehash c:\Users\john\Downloads\LESERVER18LTS.ova

Algorithm       Hash                                                                     Path
---------       ----                                                                     ----
SHA256          B3C79B8EDABA737D195EC2A688A93CC0D2A4730DB8F458841E7DDF2C2AE88253        C:\Users\john\Downloads\LESERVER18LTS...
C:\Users\john>
```
If the hash matches the given correct one then your downloaded file is non-corrupted. Instead of doing visulally the comparison, you can double-click the calculated hash and copy/paste it to this tool [hashceck](https://averkoc.github.io/hash.html).


