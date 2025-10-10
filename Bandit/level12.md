# Level 13

### Recursive unzipping and decrypting of a hexdump

**Password:**  `FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn`

## Process
Ran the following commands to get the password:
```
mkdir /tmp/mydirec
cd /tmp/mydirec
ls
xxd -r data > binary
file binary
mv binary binary.gz
gzip -d binary.gz
file binary
bzip2 -d binary
file binary.out
gzip -d binary.out
mv binary.out binary.gz
gzip -d binary.gz
ls
file binary
tar -xf binary
file data5.bin
tar -xf data5.bin
ls
file data6.bin.out
ls
file data8.bin
my data8.bin data8.gz
gzip -d data8.gz
ls
file data8
cat data8
```

## What I Learnt
`gzip` and `bzip2` are file compression/decompression commands. `file` can be used to display the true type of the file. `gzip` requires the file to have a `.gz` extensions whereas `bzip2` does not. `tar -xf` is also used to unarchive a file. `xxd` is used to convert hexdump to binary and vice versa.

## References
https://david-varghese.medium.com/overthewire-bandit-level-12-level-13-2ec761a88907