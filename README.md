# sdoc-parser
"Samsung Notes > export *.SDOC file to PDF" parser

`sudo apt install poppler-utils`

then

`find . -iname '*.pdf' -exec pdftotext {} {}.txt \;`

`for f in *.txt; do cat "$f"; printf "%s\n\n" '--'; done > output`

`sed -i 's/\x0C//g' output`

`find . -name "*.pdf" -type f -delete`

`find . -name "*.txt" -type f -delete`

or

`find . -iname '*.pdf' -exec pdftotext {} {}.txt \; && for f in *.txt; do cat "$f"; printf "%s\n\n" '--'; done > output && sed -i 's/\x0C//g' output && find . -name "*.pdf" -type f -delete && find . -name "*.txt" -type f -delete`
