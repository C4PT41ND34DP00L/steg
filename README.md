# Steg

Steg is a simple python library for hiding and extracting messages from losslessly compressed images using least-significant-bit (LSB) steganography. Current supported image formats include PNG, TIFF, BMP, and ICO.

## Installation
```
$ pip install steg
```

## Usage
```
# Import library
from steg import steg_img

# Hiding
# Select your payload and carrier files
s = steg_img.IMG(payload_path=<payload path>, image_path=<carrier path>)
# Create a new image containing your payload
s.hide()

# Extracting
# Select the carrier image
s_prime = steg_img.IMG(image_path=<path of containing hidden payload>)
# Extract the payload
s_prime.extract()
```
