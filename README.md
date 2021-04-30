# el módulo tempfile

A veces, los programas necesitan crear archivos para almacenar datos que son usados en procesos intermedios, que con posterioridad cuando ya no son necesarios, son suprimidos. Python provee una serie de funciones que facilitan las operaciones con archivos pero, concretamente, para este tipo de archivos temporales cuenta con el módulo tempfile que ofrece algunas ventajas interesantes al programador, en este ámbito.

# Entre las ventajas del módulo se encuentran las siguientes:

Permite crear archivos y directorios temporales posibilitando el acceso a los directorios temporales que ofrecen los distintos sistemas operativos.
Crea automáticamente y con seguridad los nombres de los archivos y directorios temporales pudiéndose establecer un prefijo y/o un sufijo para definir dichos nombres, para favorecer con ello su localización y tratamiento.
Proporciona funciones que suprimen automáticamente los archivos y/o directorios temporales cuando ya no son necesarios. Estas funciones son TemporaryFile(), NamedTemporaryFile(), TemporaryDirectory() y SpooledTemporaryFile(). Además, para contar con mayor control sobre el borrado de los archivos y directorios temporales ofrece, alternativamente, las funciones mkstemp() y mkdtemp(), que requieren un borrado manual.

# TemporaryFile(). Crea archivo temporal (sin nombre)

La función TemporaryFile() crea un archivo temporal de forma segura y devuelve un objeto (sin nombre) para ser utilizado como espacio de almacenamiento temporal y será suprimido tan pronto como sea cerrado.

tempfile.TemporaryFile(mode='w+b', buffering=None, encoding=None, newline=None, suffix=None, prefix=None, dir=None)

Por defecto, la apertura del archivo temporal es "w+b" (lectura/escritura en modo binario) para un procesamiento consistente entre distintos sistemas operativos, aunque también es frecuente el modo "w+t" (lectura/escritura para textos).

Los argumentos suffix y prefix, si se usan, se corresponden con la cadena de sufijo y/o de prefijo que se empleará en la construcción de los nombres de los archivos temporales. El argumento dir se utiliza para especificar un directorio para ubicar los archivos y en caso de que no se especifique ninguno se utilizará el directorio temporal del sistema, que suele ser el recomendado.

En cuanto a los argumentos buffering, encoding y newline, tienen el mismo uso que con la función open(). Son para establecer la política de almacenamiento en el búfer, especificar un nombre de codificación de caracteres y fijar cómo será el salto de líneas en los archivos creados en modo texto.


tomado de :
https://python-para-impacientes.blogspot.com/2016/04/tempfile-archivos-y-directorios.html