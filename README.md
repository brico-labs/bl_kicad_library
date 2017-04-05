# Biblioteca de BricoLabs para KiCAD

Contiene símbolos de componentes _footprints_, _templates_ y _DataSheets_ para
proyectos en KiCAD.

## Como usarla

Cuando tengas listo tu directorio de proyecto, en el que suponemos que
controlas las versiones con __git__, ejecuta un comando como este:

~~~~
git submodule add https://github.com/brico-labs/bl_kicad_library library
~~~~

Con esto le dices a __git__ que añada la librería KiCAD de BricoLabs
como un submódulo de tu repo en git, en el directorio _library_. Si
quieres ser más específico con el nombre del directorio lo puedes
llamar como más te guste, p.ej. *bl_kicad_library*

Después de añadir la biblioteca de BricoLabs como submódulo tienes que
configurar KiCAD para que sepa donde está la biblioteca.

### Configurar el editor de esquemas (_eeschema_) de KiCAD

Dentro de la opción _Preferences::Component Libraries_, y suponiendo
que has llamado _library_ a tu clone de github, añadimos el path que
apunte a `library/symbols`.

Una vez añadido el _path_ añadimos la biblioteca de BricoLabs
apuntando al fichero `library\symbols\bl_kicad.lib`.

Y ya disponemos de todos los symbolos nuevos en el proyecto.

### Configurar el editor de PCB (_pcbnew_) de KiCAD

Dentro de la herramienta _pcbnew_ arrancamos el
_Preferences::Footprint libraries wizzard_ y apuntamos al directorio
de nuestro proyecto `library/modules/bl_kicad.pretty`. Podremos
escoger si queremos añadirlo a este proyecto específico o a todos
nuestros proyectos de forma global. Si estas usando la biblioteca como
submodulo git de tu proyecto lo lógico es añadirla solo como
biblioteca de proyecto.

## Clonando tu proyecto

Si estas usando la biblioteca como submódulo git, a la hora de clonar
tu proyecto debes seguir estos pasos:

~~~~{bash}
git clone http://github.com/mi_proyecto
cd mi_proyecto
git submodule init
git submodule update
~~~~

Si no inicias (_init_) y actualizas (_update_) los submodulos, el
directorio correspondiente a la biblioteca de componentes BricoLabs
estará vacío en tu copia del proyecto.
