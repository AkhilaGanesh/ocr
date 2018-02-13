# Tesseract-Ocr

## Introduction

Tesseract is an open source text recognizer (OCR) Engine, available under the Apache 2.0 license. It can be used directly, or (for programmers) using an API to extract printed text from images. It supports a wide variety of languages.

## Brief History

Tesseract was originally developed at Hewlett-Packard Laboratories Bristol and at Hewlett-Packard Co, Greeley Colorado between 1985 and 1994, with some more changes made in 1996 to port to Windows, and some C++izing in 1998. In 2005 Tesseract was open sourced by HP. Since 2006 it is developed by Google.

The latest stable version is 3.05.01, released on June 1, 2017. Latest source code for 3.05 is available from 3.05 branch on github.

## Installing Tesseract

Prerequisites:

* Python-tesseract requires python 2.5+ or python 3.x

* You will need the Python Imaging Library (PIL) (or the Pillow fork). Under Debian/Ubuntu, this is the package python-imaging or python3-imaging.

Installing via pip:
```
$ (env)> pip install pytesseract
```
## Usage

To retrieve specific information from receipts like
* Date
* Total
* Invoice Number


## Requirements

* flask

* numpy

* pillow

* pytesseract

* opencv-python

Installing via pip:
```
$ (env)> pip install requirement
```

* textcleaner [Find textcleaner.sh here!](http://www.fmwconcepts.com/imagemagick/textcleaner/index.php)

## Bugs

Tesseract works best when there are extremely clean segmentations of the foreground text from the background.

Furthermore these segmentations need to be as high resolution (DPI) as possible and the characters in the input image cannot appear “pixelated” after segmentation. If characters do appear pixelated then Tesseract will struggle to correctly recognize the text. To improve the accuracy preprocessing must be done. Textcleaner has been used to improve the quality of the image reuslting in 20-30% increase in Tesseract accuracy.

## Running Tesseract

```
docker build -t app
docker run -p 5000:5000 --name app app
```
