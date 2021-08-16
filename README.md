# lara-pdf-merger
PDF Merger for laravel 8.xx. Work with PHP 8

Updated by Dayanne Garcia August 2021 dayannegarcia@ystevo.com

PDFMerger created by Jarrod Nettles December 2009 jarrod@squarecrow.com

Updated by Vasiliy Zaytsev February 2016 vasiliy.zaytsev@ffwagency.com

- Uses tcpdf 6.2.12 by Nicola Asuni
- Uses patched tcpdi_parser 1.0 by Paul Nicholls with own TCPdiParserException
- Uses TCPDI 1.0 by Paul Nicholls with FPDF_TPL extension 1.2.3 by Setasign

I have made some changes to make it compatible with PHP 8 and laravel 8.x.

### Example Usage
```php
include 'PDFMerger.php';

$pdf = new PDFMerger; // or use $pdf = new \PDFMerger; for Laravel

$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4');
$pdf->addPDF('samplepdfs/two.pdf', '1-2');
$pdf->addPDF('samplepdfs/three.pdf', 'all');


$pdf->merge('file', 'samplepdfs/TEST2.pdf'); // generate the file

$pdf->merge('download', 'samplepdfs/test.pdf'); // force download

// REPLACE 'file' WITH 'browser', 'download', 'string', or 'file' for output options
```
