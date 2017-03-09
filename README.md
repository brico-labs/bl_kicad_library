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


