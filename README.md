# sdoc-parser
"Samsung Notes > export *.SDOC file to PDF" parser

`
sudo apt-get update`

sudo apt install poppler-utils

python
update-alternatives --list python
ls /usr/bin/python*
update-alternatives --install /usr/bin/python python /usr/bin/python3.6 1
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.6 1
update-alternatives --list python
python --version

sudo apt-get install -y qpdf

sudo apt-get install poppler-utils ocrmypdf tesseract-ocr-pol leptonica-progs ghostscript tesseract-ocr
`

then

`find . -printf '%p' -name '*.pdf' -exec ocrmypdf '{}' '{}' \; && find . -iname '*.pdf' -exec pdftotext {} {}.txt \; && for f in *.txt; do cat "$f"; printf "%s\n\n" '--'; done > & sed -i 's/\x0C//g' output && find . -name "*.pdf" -type f -delete && find . -name "*.txt" -type f -delete`

or

`find . -printf '%p' -name '*.pdf' -exec ocrmypdf '{}' '{}' \;`

`find . -iname '*.pdf' -exec pdftotext {} {}.txt \;`

`for f in *.txt; do cat "$f"; printf "%s\n\n" '--'; done > output`

`sed -i 's/\x0C//g' output`

`find . -name "*.pdf" -type f -delete`

`find . -name "*.txt" -type f -delete`
