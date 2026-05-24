# [ PH4NTXM FIRMWARE OFFICIAL REPOSITORY ]

PH4NTXM is a secure firmware distribution designed to accompany the PH4NTXM Operating System.  
It can also be used with other Linux-based Operating Systems.  
It is built on top of the [Heads](https://github.com/linuxboot/heads) project.  
Providing a measured boot environment, TPM-based verification, and cryptographic integrity checks.

## [ BUILDING PH4NTXM FIRMWARE ]

Clone PH4NTXM Firmware Repository:

git clone https://github.com/PH4NTXMOFFICIAL/PH4NTXM-FIRMWARE.git

Build the ROM:

PH4NTXM builds inside a versioned Docker image.  
It requires docker.io so you can easily build the ROM, you can see available boards via /boards and replace BOARD= with your choice.  
The supported and tested workflow uses the provided Docker wrappers.

Install dependencies:

sudo apt install build-essential

Start build example:

sudo ./docker_repro.sh make BOARD=EOL_x220-maximized

Then your built ROM is available under /build

## [ FLASHING THE ROM ]

PH4NTXM produces a .rom file that must be flashed to the board's SPI chip.  
Important: You need an external SPI programmer (e.g., Bus Pirate, CH341A, or a dedicated flash programmer) to safely flash the firmware.  
Flashing without proper tools may brick your device. Always follow safety precautions and backup the original firmware before writing.