TP Arquitectura y Sistemas Operativos

Abrí VirtualBox e inicié la máquina virtual con Ubuntu.
Al arrancar, lo primero que hice fue usar pwd para ver en qué directorio estaba parado. Tenía entendido que podía estar en cualquier lado, así que preferí asegurarme antes de empezar.

Después creé la carpeta donde iba a trabajar:

mkdir tp_ArqySO
cd tp_ArqySO
ls

Como la carpeta era nueva, no tenía nada, lo cual era lo esperado.

En esta parte ya empezaron algunos problemas. El teclado dentro de la máquina virtual no coincidía con el de Windows y me costaba escribir ciertos caracteres. Esto me hizo cometer algunos errores, así que en un momento decidí borrar todo con:

rm -r tp_ArqySO

y empezar de nuevo más prolijo. También limpié la consola varias veces con Ctrl + L para no confundirme.

Después intenté usar git init, pero me apareció un error porque no tenía Git instalado. Tuve que buscar cómo instalarlo y ejecuté:

sudo apt update
sudo apt install git -y

Ingresé la contraseña y se instaló correctamente. Ahí sí pude volver a ejecutar git init y crear el repositorio.

Luego creé los archivos que pedía el TP:

touch README.md datos_usuario.txt

Verifiqué con ls que estuvieran creados.

Después usé:

git add .

Entendí que esto sirve como para “avisarle” a Git qué archivos quiero incluir antes de guardarlos.

Cuando quise hacer el commit, me apareció otro error porque Git no tenía configurado mi nombre y mail. Eso no lo sabía, así que tuve que configurarlo con:

git config --global user.name Nahuel
git config --global user.email nahuel@tp.com

Después de eso pude hacer:

git commit -m PrimerCommit

y se guardaron los archivos.

Más adelante generé el historial de comandos con:

history > historial_comandos.txt

y lo agregué al repositorio:

git add historial_comandos.txt
git commit -m AgregoHistorial

En esta parte ya estaba más cómodo con los comandos.

Después vino la parte de GitHub, que también tuvo sus complicaciones.
Primero creé el repositorio desde la página, pero al vincularlo desde la terminal tuve errores porque no podía escribir bien la URL (por el tema del teclado) y además me faltaban partes como https:// y .git.

Tuve que borrar el remote y volver a agregarlo correctamente.

Cuando intenté hacer git push, me falló porque estaba usando mi contraseña normal. Ahí aprendí que GitHub ahora usa tokens, así que tuve que generar uno desde la configuración de la cuenta y usarlo como contraseña.

Finalmente, el push funcionó y se subieron todos los archivos correctamente.

También tuve un problema donde la máquina virtual se trabó y no me dejaba escribir. Tuve que reiniciarla desde VirtualBox para poder seguir.
