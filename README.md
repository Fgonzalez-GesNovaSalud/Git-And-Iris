# Usando Git con Intersystem Iris

## Pre requisitos para usar Git

- IRIS con licencia
- Git [1](https://git-scm.com/downloads/win)
- OpenSSH
  - Habilitar OpenSSH en Windows [2](https://soporte.donweb.com/hc/es/articles/19426302601364--C%C3%B3mo-habilitar-el-cliente-OpenSSH-en-Windows-10) 
  - Crear clave pública SSH [3](https://git-scm.com/book/es/v2/Git-en-el-Servidor-Generando-tu-clave-p%C3%BAblica-SSH)
- InterSystems package manager [4](https://openexchange.intersystems.com/package/InterSystems-Package-Manager-1) [5](https://www.youtube.com/watch?v=UzrG91_swLM&list=PLKb2cBVphNQRcmxt4LtYDyLJEPfF4X4-4&index=7&t=615s)


## InterSystems package manager

Para instalar Intersystems package manager debes:

1.- Descargar la última varsión de zpm e importar el archivo dentro de "Clases" en el portal de gestión y compilar.

2.- Entrar desde el terminal de tu Namespace y entrar a zpm.
```
zpm 
```

3.- instalar librerias en zpm.
```
repo -n registry -r -url https://pm.community.intersystems.com
```


## Control de versiones con Git

Documentación de Git for Shared Develop Enviroment en Open Exange [6](https://openexchange.intersystems.com/package/Git-for-Shared-Development-Environments) y en página de Intersystem Iris [7](https://community.intersystems.com/post/git-shared-development-environments) y video de referencia [8](https://youtu.be/elVQEU9MitE?t=387) 

Instalar Git Source Control
```
zpm "install git-source-control"
```

Configurar el Namespace
```
d ##class(SourceControl.Git.API).Configure()
```


