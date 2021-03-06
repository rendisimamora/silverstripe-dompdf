# PDF Generation via DOMPDF Library

Maintainer: Jeremy Shipman (jeremy@burnbright.net)

Makes use of: https://github.com/dompdf/dompdf 
Dompdf websites: http://dompdf.github.com/, http://pxd.me/dompdf/www/

Input:

 * HTML string (which could be rendered template)
 * HTML File
 
Output

 * PDF File location
 * SS File
 * PDF binary stream to browser

## Example usage

```php
	$pdf = new SS_DOMPDF();
	$pdf->setHTML($mydataobject->renderWith('MyTemplate'));
	$pdf->render();
	$pdf->toFile('mypdf.pdf');
```
	
## Debugging

The $pdf->streamdebug(); function is useful for quickly viewing pdfs, particularly
if your browser supports displaying pdfs, rather than downloading.

You can check your html before it is converted like this:

```php
	echo $mydataobject->renderWith('MyTemplate');die();
```
	
## Useful Tips

 * Use tables for layout if you get errors from floating divs.
 * See the [official dompdf website](http://pxd.me/dompdf/www/) for more info