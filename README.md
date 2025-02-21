# Usando Git con Intersystem Iris

[D] Documentación
[V] Video
[O] OpenExange

## Pre requisitos para usar Git

- IRIS con licencia
- Git [D](https://git-scm.com/downloads/win)
- OpenSSH
  - Habilitar OpenSSH en Windows [D](https://soporte.donweb.com/hc/es/articles/19426302601364--C%C3%B3mo-habilitar-el-cliente-OpenSSH-en-Windows-10) 
  - Crear clave pública SSH [D](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- InterSystems package manager [O](https://openexchange.intersystems.com/package/InterSystems-Package-Manager-1) [V](https://www.youtube.com/watch?v=UzrG91_swLM&list=PLKb2cBVphNQRcmxt4LtYDyLJEPfF4X4-4&index=7&t=615s)


## InterSystems package manager

Para instalar Intersystems package manager debes:

1.- Descarga la última varsión de zpm desde OpenExange e importa el archivo dentro de "Clases" en el portal de gestión y compila.

2.- Entra desde el terminal de tu Namespace a zpm.
```
zpm 
```

3.- Revisa si están disponibles las librerias por instalar.
```
repo -list-modules -n registry
```


3.- Instala las librerias de ser necesario.
```
repo -n registry -r -url https://pm.community.intersystems.com
```


## Control de versiones con Git

Documentación de Git for Shared Develop Enviroment  [O](https://openexchange.intersystems.com/package/Git-for-Shared-Development-Environments)  [D](https://community.intersystems.com/post/git-shared-development-environments) [V](https://youtu.be/elVQEU9MitE?t=387) 

Instala Git Source Control
```
zpm "install git-source-control"
```

Configura el Namespace
```
do ##class(SourceControl.Git.API).Configure()
```

Desde la terminal en tu repositorio local configura con tu directorio
```
git config --global --add safe.directory C:/InterSystems/IRISHealth/mgr/repo/DEMO
```

Añade archivos en tu directorio (repositorio local) 
```
git add .
```

Genera un comit on untexto representativo
```
git commit -m "hola mundo"
```







