# Pràctica CI - Ferran De La Varga Antoja

Petita pràctica de Gestió de Projectes de Software ([GPS](https://www.fib.upc.edu/ca/estudis/graus/grau-en-enginyeria-informatica/pla-destudis/assignatures/GPS))

## Vídeo
Link del vídeo conforme s'executa i que tot funciona:  https://drive.google.com/open?id=1PyDvJxk5Fyq1QRTrfThvhhtw-1kxg9Bc&authuser=ferran.de.la.varga%40estudiantat.upc.edu&usp=drive_fs

Es necessita un compte UPC per visualitzar-ho.

Aquest vídeo no mostra el "coverage" ja que s'ha afegit posteriorment. Amb el coverage afegit també complia i s'executa correctament.

## Explicació fitxer
El fitxer `python-app.yml` ubicat al directori `.github/workflows` permet realitzar integració contínua; el fitxer complia el projecte i passa els tests.

Estructura del fitxer:

1r - Es determina la versió de Python a utilitzar.

2n - Instala els requisits definits al fitxer `requirements.txt` (en aquest projecte és buit).

3r - Complia el projecte, si dona errors es para.

4t - Executa el projecte, si dona errors es para.

5è - Executa els tests definits al fitxer `test.py`, si un test no passa s'atura.

6è - Executa el coverage i es mostra la quantitat de tests passats i els ignorats.

## Què aporta aquest fitxer a CI?
Amb aquest sistema podem fer releases de petites funcionalitats d'un projecte fàcilment, amb la seguretat i confiança que només es publicarà la nova versió si aquest complia s'executa i passa tots els tests. Cada cop que volem realitzar un canvi al projecte, el pujaríem al repositori i automàticament faríem la comprovació de passar tots els tests.
