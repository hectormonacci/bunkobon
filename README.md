# bunkobon

Recibe un PDF secuencial en tamaño A6, entrega un PDF A4 con
las páginas A6 impuestas para encuadernar en pliegos de 16
páginas A6.

Ejemplo: ```bunkobon input.pdf``` (produce input-bunkobon.pdf)

## Alternativas que probé, no 100% satisfactorias:

1. En PERL, instalar con ```sudo cpan install Perl::PDF::Imposition```
   y usar con ```pdf-impose.pl --schema ea4x4 --paper a6 input.pdf```
   [no elimina las hojas en blanco al final]

2. En PYTHON, instalar con ```sudo pip install pdfimpose``` (inspirado en el anterior)
   y usar con ```pdfimpose perfect -s 2x2 input.pdf```
   [pliegos de 8 páginas, y papel resultante 210 x 296 mm]

3. En JAVA, bookbinder (GUI, parece abandonado, sin output)

4. En C++, podofoimpose (no me funciona el "Plan" que encontré)

5. En PYTHON, pdfbook2 (sólo hace 2up y no sabe reordenar pliegos)

6. En PERL, pdfbklt (se queja de xref mal formado en input)

## Alternativas que no probé:

1. bookletcreator.com (pago, GUI, Mac y Win)

## Nuestro bunkobon:

Sólo dos dependencias: pdftk y pdfjam (que implica LaTeX).
