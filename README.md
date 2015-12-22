# Tesseract OCR

Docker container running [tesseract-ocr](https://github.com/tesseract-ocr/tesseract) as executable

Usage as executable and extract as txt file

* `docker run --rm joergpatz/tesseract`
* ``docker run --rm -v `pwd`/src:/tmp joergpatz/tesseract [-l langID] john3_16.png outputtext``

Usage as executable and extract as [HOCR](https://en.wikipedia.org/wiki/HOCR) file

* ``docker run --rm -v `pwd`/src:/tmp joergpatz/tesseract [-l langID] john3_16.png outputtext hocr``

Usage inside the container

* ``docker run --rm -v `pwd`/src:/tmp -it --entrypoint /bin/bash joergpatz/tesseract``

included imagemagick library for converting files `convert -density 300 foobar.pdf foobar.tif`