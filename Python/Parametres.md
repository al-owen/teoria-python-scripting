Per passar paràmetres a un script de Python des de la línia de comandes, pots utilitzar la variable `sys.argv` del mòdul `sys`. Aquesta variable és una llista de Python que conté els arguments de la línia de comandes com a cadenes. El primer element de la llista (`sys.argv[0]`) és sempre el nom del script. Els elements següents són els arguments passats al script.

Aquí tens un exemple de com utilitzar `sys.argv` per llegir els arguments de la línia de comandes en un script de Python:

```python

import sys  # Imprimim tots els arguments passats, incloent el nom del script 
for i, arg in enumerate(sys.argv):
	print(f"Argument {i}: {arg}")# Comprovar si s'han passat arguments 
	adicionals 
if len(sys.argv) > 1:# Els arguments comencen en sys.argv[1]
	primer_argument = sys.argv[1] 
	print(f"El primer argument passat és: {primer_argument}")
else:
	print("No s'han passat arguments addicionals.")
```
Per executar aquest script amb paràmetres, utilitzaries la línia de comandes d'aquesta manera (suposant que el script es diu `meu_script.py`):

``` bash
python meu_script.py argument1 argument2
```

Aquesta comanda passaria `argument1` i `argument2` al teu script de Python, on serien accessibles com a `sys.argv[1]` i `sys.argv[2]`, respectivament.
