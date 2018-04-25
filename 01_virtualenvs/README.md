### Introducción a los ambientes virtuales en python
Universidad ICESI  
Curso: Sistemas Operativos  
Docente: Daniel Barragán C.  
Tema: Introducción a los ambientes virtuales en python  
Correo: daniel.barragan at correo.icesi.edu.co

### Objetivos
* Crear ambientes virtuales con python

### Introducción
Por medio de los ambientes virtuales de python es posible ejecutar múltiples proyectos con versiones de librerías distintas.
Virtualenvwrapper es un wrapper para virtualenv el cual permite la activación de ambientes virtuales desde cualquier lugar del path del sistema operativo

### Requerimientos
Maquina Virtual de CentOS7

### Instalación
Ingrese los comandos que se describen a continuación

```
# adduser microservices
# passwd microservices
# yum install -y wget
# wget https://bootstrap.pypa.io/get-pip.py -P /tmp
# python /tmp/get-pip.py
# pip install virtualenv
# su microservices
$ pip install --user virtualenvwrapper
```
Para iniciar virtualenvwrapper al autenticarse como el usuario microservices editamos el archivo **.bashrc**
```
$ vi ~/.bashrc
export WORKON_HOME=~/.virtualenvs
source /home/microservices/.local/bin/virtualenvwrapper.sh
```
Para activar los cambios sin necesidad de cerrar la sesión del usuario python_user se debe ejecutar el siguiente comando
```
$ source ~/.bashrc
```

### Desarrollo

Practique los comandos que se muestran en la tabla a continuación

| Comando | Descripción |
|---	|---	|
| mkvirtualenv test	| Crea el ambiente virtual llamado test	|
| deactivate	| Si un ambiente virtual esta activo, lo desactiva	|
| workon test	| Activa el ambiente virtual llamado test	|
| pip install Flask	| Si el ambiente esta activo, instala la libreria Flask en el ambiente	|
| rmvirtualenv test	| Elimina el ambiente virtual llamado test	|
| lsvirtualenv | Lista los ambientes virtuales |

### FAQ

* Si tiene problemas con la iniciación de virtualenvwrapper debido a que este busca el interprete de python en /usr/bin/python
cree la siguiente variable de ambiente antes de ejecutar el comando source ~/.local/bin/virtualenvwrapper.sh
```
VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3.4
```

### Actividades

* Cree al menos tres ambientes que tengan la misma librería de python pero en versiones distintas
