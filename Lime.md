# Lime : memory dump tool
### Source
- https://github.com/504ensicslabs/lime
### Install
- Download the package
    - sudo git clone https://github.com/504ensicsLabs/LiME.git
- Move to /LinME/src and perform the command "make"
### Dump
- Start the dump
- sudo insmod ./lime-5.4.0-1011-aws.ko "path=lime.dump format=lime"
OR
- sudo insmod ./lime-5.4.0-1011-aws.ko "path=lime.dump format=raw"
### Checksum
- In order to guarantee the non-repudiation and the chain of custody
- md5sum lime.dump
- **Attention**: keep the hash on a secure place in order to be able to
proof the authenticity of the file
