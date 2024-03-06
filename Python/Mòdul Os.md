El mòdul `os` de Python ofereix una manera portable de utilitzar funcionalitats dependents del sistema operatiu. Aquest mòdul permet interactuar amb el sistema operatiu sota el qual s'executa Python, com ara accedir al sistema de fitxers, obtenir informació sobre processos, entorn d'execució i molt més. A continuació, es detallen algunes de les característiques i funcions més rellevants que proporciona el mòdul `os`:

### Gestió del Sistema de Fitxers

- **os.chdir(path)**: Canvia el directori de treball actual a la ruta especificada.
- **os.getcwd()**: Retorna el directori de treball actual com a cadena de text.
- **os.listdir(path='.')**: Llista els noms dels fitxers i directoris en el directori donat.
- **os.mkdir(path, mode=0o777)**, **os.makedirs(path, mode=0o777, exist_ok=False)**: Crea un nou directori o directoris. `makedirs` pot crear directoris múltiples (ruta completa) si no existeixen.
- **os.remove(path)**, **os.rmdir(path)**, **os.removedirs(path)**: Elimina fitxers i directoris. `removedirs` pot eliminar directoris múltiples recursivament.
- **os.rename(src, dst)**: Renombra o mou un fitxer o directori a un nou lloc.

### Interacció amb el Sistema Operatiu

- **os.system(command)**: Executa la comanda en el sistema, això permet executar comandes del shell.
- **os.getenv(key, default=None)**: Obté el valor d'una variable d'entorn, retornant `default` si la variable no existeix.
- **os.putenv(key, value)**: Estableix el valor de la variable d'entorn `key` al valor `value`.
- **os.exit(code)**: Sorteix de Python amb el codi d'estat donat. És un alias de `sys.exit()`.

### Treball amb Rutes de Fitxers

- **os.path.join(path, *paths)**: Uneix un o més components de ruta intel·ligentment. Això és útil per crear rutes de forma portable.
- **os.path.abspath(path)**: Retorna la ruta absoluta d'una ruta, normalitzant el camí i resolent qualsevol referència relativa.
- **os.path.exists(path)**: Comprova si un camí existeix o no.
- **os.path.isfile(path)**, **os.path.isdir(path)**: Comproven si el camí donat és un fitxer o un directori, respectivament.

### Funcions per a la Gestió de Processos

- **os.fork()**: Crea un procés fill duplicant el procés actual (només Unix/Linux).
- **os.kill(pid, sig)**: Envia una senyal a un procés amb l'identificador de procés `pid`.

### Exemple d'Ús

Aquí teniu un exemple simple que utilitza algunes de les funcions del mòdul `os` per interactuar amb el sistema de fitxers:

``` python
import os
# Canvia el directori de treball 
os.chdir('/tmp')  # Llista els fitxers i directoris en el directori actual 
print("Contingut de /tmp:", os.listdir())  # Crea un nou directori nou_directori = "exemle" 
if not os.path.exists(nou_directori):
	os.mkdir(nou_directori)
	print(f"Directori {nou_directori} creat.")`
```
