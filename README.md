# el módulo tempfile

A veces, los programas necesitan crear archivos para almacenar datos que son usados en procesos intermedios, que con posterioridad cuando ya no son necesarios, son suprimidos. Python provee una serie de funciones que facilitan las operaciones con archivos pero, concretamente, para este tipo de archivos temporales cuenta con el módulo tempfile que ofrece algunas ventajas interesantes al programador, en este ámbito.

# Entre las ventajas del módulo se encuentran las siguientes:

Permite crear archivos y directorios temporales posibilitando el acceso a los directorios temporales que ofrecen los distintos sistemas operativos.
Crea automáticamente y con seguridad los nombres de los archivos y directorios temporales pudiéndose establecer un prefijo y/o un sufijo para definir dichos nombres, para favorecer con ello su localización y tratamiento.
Proporciona funciones que suprimen automáticamente los archivos y/o directorios temporales cuando ya no son necesarios. Estas funciones son TemporaryFile(), NamedTemporaryFile(), TemporaryDirectory() y SpooledTemporaryFile(). Además, para contar con mayor control sobre el borrado de los archivos y directorios temporales ofrece, alternativamente, las funciones mkstemp() y mkdtemp(), que requieren un borrado manual.




tomado de :
https://python-para-impacientes.blogspot.com/2016/04/tempfile-archivos-y-directorios.html