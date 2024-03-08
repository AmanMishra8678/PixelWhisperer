# PixelWhisperer
# Steganography Encoder/Decoder

This Python script provides a simple implementation of steganography for encoding and decoding data within images. Steganography is the art of concealing information within other data to protect the secrecy of the message.


## Introduction

Steganography involves hiding data within an image's least significant bits, allowing for the concealment of information without noticeable degradation in the image's visual quality. This script supports encoding textual data or binary files into images and decoding the hidden data from images.

## Requirements

- Python 3.x
- OpenCV (`cv2`) library
- numpy
Install the required library using:

```bash
pip install opencv-python numpy
```

## Usage

The script can be used in two modes: encoding and decoding.

### Encoding

To encode data into an image, use the following command:

```bash
python steganography.py -e <image_path> -t "Your secret text here" -b <n_bits>
```

or for binary file encoding:

```bash
python steganography.py -e <image_path> -f <file_path> -b <n_bits>
```

### Decoding

To decode hidden data from an image, use the following command:

```bash
python steganography.py -d <encoded_image_path> -f <output_file_path> -b <n_bits>
```

## Options

- `-t, --text`: The text data to encode into the image (for encoding only).
- `-f, --file`: The file to hide into the image (for encoding only).
- `-e, --encode`: Encode the specified image.
- `-d, --decode`: Decode the specified encoded image.
- `-b, --n-bits`: The number of least significant bits of the image to encode (default is 2).

## Examples

### Encoding

```bash
python steganography.py -e input_image.jpg -t "Hello, this is a secret message." -b 2
```

```bash
python steganography.py -e input_image.jpg -f secret_file.txt -b 3
```

### Decoding

```bash
python steganography.py -d encoded_image.png -f output_file.txt -b 2
```

## License

This script is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
