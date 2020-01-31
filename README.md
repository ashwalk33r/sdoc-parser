# sdoc-parser
*.SDOC file format parser

find . -iname '*.pdf' -exec pdftotext {} {}.txt \;
find . -iname '*.txt' -exec head -n -1 {} \; > notes.txt
