# Eubank-s-EBASIC-source

OCR'd the PDF pages of "A microprocessor implementation of extended basic by Gordon Eubanks"
by using pdftk to burst each individual page.

$ pdftk amicroprocessori1094517862.pdf burst

Then converted the PDF pages to *.tif so they could be OCR'd with tesseract
The PDF's are 72 DPI, and need to be 300 to 450 DPI to get descent results.

$ convert -density 400 pg_0014.pdf -background white -despeckle -depth 8 pg_0014.tif

$ tesseract pg_0014.tif p014 -psm 6

All that is needed is a cleanup of the text and formatted as the original PDF pages.


