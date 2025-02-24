# Usando Git con Intersystem Iris

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







