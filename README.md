# Alfred Workflow OCR
Take a snapshot and recognize text

[![alfred-ocr.png](https://i.postimg.cc/3JV8jSRK/alfred-ocr.png)](https://postimg.cc/N58vBxmV)

## Installation

Install `tesseract` on your system: https://github.com/thiagoalessio/tesseract-ocr-for-php#installation

## Usage

Use the keywork `OCR`, take a screenshot, paste the text

## What's inside?

Three lines of code:

```bash
export PATH=/usr/local/bin/:$PATH

screencapture -i /tmp/ocr_snapshot.png

tesseract /tmp/ocr_snapshot.png stdout
```

## Credits

Inspired by the work of https://github.com/oott123/alfred-clipboard-ocr
