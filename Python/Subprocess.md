### Funcions Principals del Mòdul `subprocess`

#### subprocess.run()

La funció `run()` és la manera recomanada de llançar un nou procés en Python 3.5 i posteriors. Aquesta funció executa el comandament descrit per `args`, espera a que finalitze i retorna un objecte `CompletedProcess`. Per exemple:

``` python
import subprocess
result = subprocess.run(['ls', '-l'], capture_output=True, text=True) print(result.stdout)`
```

Aquest codi llista tots els fitxers en el directori actual en format llarg.

#### subprocess.Popen()

`Popen` és la classe central del mòdul `subprocess` per a la creació de processos. Ofereix més flexibilitat que `run()` per gestionar processos, com la possibilitat de comunicar-se amb el procés (enviar dades a la seua entrada estàndard o llegir de la seua sortida estàndard i error estàndard) i controlar la seua execució. Per exemple:


``` python
import subprocess
proc = subprocess.Popen(['cat'], stdin=subprocess.PIPE, stdout=subprocess.PIPE, text=True) stdout, stderr = proc.communicate('Hola, món!')
print(stdout)
```


Aquest exemple utilitza `cat` per llegir una cadena proporcionada pel programa i la imprimeix.

### Arguments Importants

- **args**: Una seqüència que indica el comandament a executar i els seus arguments, o una única cadena si `shell=True`.
- **stdin, stdout, stderr**: Especifica com s'han de manejar els fluxos d'entrada, sortida i error del procés. Pot ser `subprocess.PIPE`, `subprocess.DEVNULL`, un fitxer existent obert en mode d'escriptura o lectura, o altres opcions.
- **capture_output**: Si es defineix a `True`, captura la sortida i l'error estàndard del procés.
- **shell**: Si es defineix a `True`, els comandaments s'executen a través d'una shell intermediària. No obstant això, l'ús de `shell=True` és menys segur en certes situacions, així que s'ha d'utilitzar amb precaució.