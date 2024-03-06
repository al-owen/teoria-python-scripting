
## Que és un Script en Python?

Un script en Python és simplement un fitxer amb codi Python que està destinat a ser executat directament. Aquests fitxers tenen l'extensió `.py` i poden contindre instruccions que realitzen una tasca específica.

### Característiques dels Scripts en Python:

- **Automatització:** Permeten automatitzar tasques repetitives i monotones, com manipular fitxers, accedir a bases de dades o interactuar amb APIs web.
- **Facilitat d'ús:** La sintaxi de Python és clara i senzilla, facilitant l'aprenentatge i la implementació de scripts.
- **Portabilitat:** Els scripts en Python poden executar-se en múltiples plataformes sense necessitat de modificar el codi (Windows, MacOS, Linux).
- **Extensibilitat:** Es poden utilitzar mòduls i biblioteques per afegir funcionalitats als scripts, com ara interfícies gràfiques, operacions matemàtiques complexes o manipulació d'imatges.

## Com escriure un Script Bàsic en Python

Per escriure un script en Python, només necessites un editor de text pla i Python instal·lat al teu sistema. Exemple:

``` python
# HolaMundo.py 
print("Hola, món!")`
``` 

Per executar aquest script, guarda'l com `HolaMundo.py` i des de la línia de comandes o terminal, navega fins al directori on s'ha guardat el fitxer i executa:

```bash
python HolaMundo.py
```

Veuries la sortida `Hola, món!` a la teva consola.

### Estructura d'un Script Python

La majoria dels scripts en Python segueixen una estructura bàsica:

1. **Importació de Mòduls:** Al començament dels scripts, es solen importar els mòduls i biblioteques necessàries.
2. **Definició de Funcions:** Després, es poden definir funcions que realitzaran tasques específiques.
3. **Bloc Principal:** Finalment, un bloc principal on es criden les funcions definides anteriorment i s'executen les instruccions principals.

```python
# Exemple de script en Python
import os
def neteja_pantalla():
	os.system('clear' if os.name == 'posix' else 'cls')
def saluda(nom):
	print(f"Hola, {nom}!")
	if __name__ == "__main__":

neteja_pantalla()
saluda("Món")
```

Aquest script importa el mòdul `os`, defineix dues funcions (`neteja_pantalla` i `saluda`) i les executa dins del bloc principal.
