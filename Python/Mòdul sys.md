El mòdul `sys` de Python és una part integral de l'estàndard de biblioteques de Python i proporciona accés a algunes variables utilitzades o mantingudes per l'intèrpret de Python i a funcions que interactuen fortament amb l'intèrpret. Es tracta d'un mòdul que ofereix accés a variables i funcionalitats, estretament relacionades amb el sistema i l'intèrpret de Python.

### Funcionalitats Clau del Mòdul `sys`

1. **sys.argv**: Una llista de cadenes d'arguments de línia de comandes passats a un script de Python. `argv[0]` és el nom del script (depèn del sistema operatiu si aquest camí és complet o només el nom del fitxer). Els arguments restants es troben a `argv[1:]`.
    
2. **sys.exit()**: Permet sortir de Python, opcionalment passant un argument específic al sistema operatiu. És útil per acabar l'execució d'un script quan es compleix una condició específica.
    
3. **sys.path**: Una llista de cadenes que especifica la ruta de cerca per a mòduls. Quan importeu un mòdul, Python busca en les rutes llistades a `sys.path`. Aquesta llista es pot modificar durant l'execució del programa per incloure altres directoris on buscar mòduls.
    
4. **sys.version**: Una cadena que conté la versió del intèrpret Python en ús, juntament amb informació addicional sobre la compilació. Això és útil per comprovar programàticament la versió de Python en execució.
    
5. **sys.platform**: Una cadena que indica la plataforma sota la qual s'està executant Python (per exemple, 'win32', 'darwin', 'linux', etc.). Això és útil per escriure codi que depèn de la plataforma.
    
6. **sys.stdin, sys.stdout, i sys.stderr**: Objectes de fitxer que corresponen a l'entrada estàndard, la sortida estàndard i l'error estàndard del sistema, respectivament. Aquests objectes poden ser redirigits per gestionar l'entrada i sortida del programa de manera programàtica.
    
7. **sys.getsizeof()**: Una funció que retorna la mida, en bytes, d'un objecte, proporcionant una manera de mesurar l'ús de la memòria.
    
8. **sys.executable**: Una cadena que conté el camí cap al intèrpret de Python en ús. Això pot ser útil per reiniciar el programa actual amb el mateix intèrpret o per llançar altres scripts de Python.
    
9. **sys.modules**: Un diccionari que mapeja els noms de mòduls als mòduls que ja han estat carregats. Això permet a un programa inspeccionar o manipular els mòduls que són accessibles.
    

### Exemple d'Ús de `sys.argv`

Un ús comú de `sys` és accedir als arguments de la línia de comandes amb `sys.argv`. Aquí teniu un exemple simple:

``` python
import sys  
# Imprimeix tots els arguments de la línia de comandes 
for i, arg in enumerate(sys.argv):
print(f"Argument {i}: {arg}")
```

Executar aquest script des de la línia de comandes amb alguns arguments mostrarà els valors d'aquests arguments.
