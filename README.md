# Alfred Workflow OCR
Take a snapshot and recognize text

[![alfred-ocr.png](./alfred-ocr.png)](./alfred-ocr.png)

## Installation

1. [Install `tesseract` on your system](https://github.com/tesseract-ocr/tesseract/wiki#macos): `sudo port install tesseract` or `brew install tesseract` and then `brew install tesseract-lang` if you need additional langugages.
2. Download the [workflow](https://github.com/nicooprat/alfred-ocr/blob/master/OCR.alfredworkflow)
3. Double click to install it in Alfred

## Usage

Use the keywork `OCR`, take a screenshot, wait for the notification, paste the text. For better results, you can also add a language as optionnal argument like this: `OCR fra` ([full list of language codes here](https://github.com/tesseract-ocr/tesseract/blob/b67ea2c1a70c56053e142a5fb7cc18fb29cdc4b8/src/training/language-specific.sh#L21)).

[![Capture-d-e-cran-2018-11-09-a-10-06-07.png](https://i.postimg.cc/jdsggtDc/Capture-d-e-cran-2018-11-09-a-10-06-07.png)](https://postimg.cc/5jRSjcqQ)

## What's inside?

Just a tiny bash script:

```bash
export PATH="/opt/homebrew/bin:/usr/local/bin:${PATH}"

screencapture -i /tmp/ocr_snapshot.png

if [{query} = ""]; then
tesseract --dpi 300 /tmp/ocr_snapshot.png  stdout 2>&1
else
tesseract --dpi 300 /tmp/ocr_snapshot.png stdout  -l {query} 2>&1
fi
```

## Discussion

On Alfred forum: https://www.alfredforum.com/topic/12006-ocr-extract-text-from-snapshot/

## Credits

Inspired by the work of https://github.com/oott123/alfred-clipboard-ocr. Thanks [bergmul](https://github.com/bergmul) for his help.
