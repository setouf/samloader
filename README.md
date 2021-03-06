# samloader
Download firmware for Samsung devices (without any extra Windows drivers).
## Installation
```
pip3 install git+https://github.com/nlscc/samloader.git
```
## Usage
`checkupdate [model] [region]`: Check the latest firmware version

`download [version] [model] [region] [out]`: Download the specified firmware version for a given phone and region to a specified file or directory

`decrypt2 [version] [model] [region] [infile] [outfile]`: Decrypt enc2 encrypted firmwares

`decrypt4 [version] [model] [region] [infile] [outfile]`: Decrypt enc4 encrypted firmwares (requires network connection)
### Example
```
$ samloader checkupdate GT-I8190N BTU
I8190NXXAMJ2/I8190NBTUAMJ1/I8190NXXAMJ2/I8190NXXAMJ2
$ samloader download I8190NXXAMJ2/I8190NBTUAMJ1/I8190NXXAMJ2/I8190NXXAMJ2 GT-I8190N BTU .
Downloading file /neofus/9/GT-I8190N_BTU_1_20131118100230_9ae3yzkqmu_fac.zip.enc2 ...
MD5: cbe93cda7080a93b9d11246aa3d58828
[################################] 10570/10570 - 00:02:02
Done!
$ samloader decrypt2 I8190NXXAMJ2/I8190NBTUAMJ1/I8190NXXAMJ2/I8190NXXAMJ2 GT-I8190N BTU GT-I8190N_BTU_1_20131118100230_9ae3yzkqmu_fac.zip.enc2 GT-I8190N_BTU_1_20131118100230_9ae3yzkqmu_fac.zip
Decrypting with key f3f48b1cb4f8e84fc33f4ef270bf7578...
[################################] 169115/169115 - 00:00:08
Done!
```
