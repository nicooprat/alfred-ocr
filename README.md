# Alfred Workflow OCR
Take a snapshot and recognize text

[![alfred-ocr.png](https://i.postimg.cc/3JV8jSRK/alfred-ocr.png)](https://postimg.cc/N58vBxmV)

## Installation

1. Install `tesseract` on your system: https://github.com/thiagoalessio/tesseract-ocr-for-php#installation
2. Download the [workflow](https://github.com/nicooprat/alfred-ocr/blob/master/OCR.alfredworkflow)
3. Double click to install it in Alfred

## Usage

Use the keywork `OCR`, take a screenshot, wait for the notification, paste the text.

[![Capture-d-e-cran-2018-11-09-a-10-06-07.png](https://i.postimg.cc/jdsggtDc/Capture-d-e-cran-2018-11-09-a-10-06-07.png)](https://postimg.cc/5jRSjcqQ)

## What's inside?

Three lines of code:

```bash
export PATH=/usr/local/bin/:$PATH

screencapture -i /tmp/ocr_snapshot.png

tesseract /tmp/ocr_snapshot.png stdout
```

## Credits

Inspired by the work of https://github.com/oott123/alfred-clipboard-ocr
