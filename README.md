# Usando Git con Intersystem Iris

## Pre requisitos para usar Git

- IRIS con licencia
- Git [1](https://git-scm.com/downloads/win)
- OpenSSH
  - Habilitar OpenSSH en Windows [2](https://soporte.donweb.com/hc/es/articles/19426302601364--C%C3%B3mo-habilitar-el-cliente-OpenSSH-en-Windows-10)
  - Crear clave pública SSH [3](https://git-scm.com/book/es/v2/Git-en-el-Servidor-Generando-tu-clave-p%C3%BAblica-SSH)
- InterSystems package manager [4](https://openexchange.intersystems.com/package/InterSystems-Package-Manager-1)


## Source Control

Documentación de Git for Shared Develop Enviroment en Open Exange [5](https://openexchange.intersystems.com/package/Git-for-Shared-Development-Environments) y en página de Intersystem Iris [6](https://community.intersystems.com/post/git-shared-development-environments) 

Instalar Git Source Control
```
zpm "install git-source-control"
```

Configurar el Namespace
```
d ##class(SourceControl.Git.API).Configure()
```
