MOdificado por Cano de la Cuadra....

git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/sir-seawolf/Apuntes-Git.git
git push -u origin master

# Flujo de trabajo básico

## git status, git add, git commit, git push

#### Ver en qué ficheros hemos introducido cambios

Podemos ver el status de los cambios en nuestros ficheros de la siguiente forma:

```
$ git status
```

### stage

Uno de los conceptos más esenciales en git es el de el staging area. Un simil podría ser un ***muelle de carga*** donde se ve qué archivos   archivos con cambios son susceptibles de ser enviados siguiente paso, el commit.



#### Añadir fichero con cambios al stage

Para añadir cambios de un fichero al stage podemos hacerlo de la siguiente forma:

```
$ git add archivo
```
o 
```
$ git add archivo, archivo2
```

También podemos añadir todos los archivos que tienen cambios al stage en una misma operación con el comando:

```
$ git add .
```
```
$ git add --all
```

### commit


EL commit es el siguiente paso, con el commit estamos confirmando y grabando nuestros cambios en nuestro repositorio local.

```
$ git commit -m "Mensaje del commit"
```
Los mensajes del commit son muy importantes, leyendolos se debería entender qué se está haciendo y la cronología de los cambios. Es una buena práctica hacer commits pequeños, bien descritos, para la integración continua y la regresión es fundamental unos commits bien acotados y definidos.

Aunque podríamos resumirlo en algo muy sencillo

```
$ git commit -m "describe de una manera sencilla tus cambios"
```
#### git commit -am
git commit -am es un atajo de git add y git commit
git commit -a -m es una versión del anterior atajo

#### Reescribir un commit mal escrito

Podemos editar un commit mal escrito (antes de empujarlo a un sitio remoto) con el siguiente comando:

```
$ git commit --amend
```

## push

### Empujando nuestors cambios a otro repositorio remoto

Hasta ahora con el commit hemos grabado nuestros cambios en nuestro repositorio en local, vamos ahora a empujar nuestros cambios hacia cualquier repositorio que tengamos enlazado.
Para enlazarlo
```bash 
git add origin repositorio.git
``` 

```bash     
 git push repositorioAlQueEmpujar ramaALaQueEmpujar
git push origin dev
```
    
En este ejemplo origin es el repositorio origen que tengamos enlazado, en el caso de haber enlazado nuestro repositorio local con un git clone, origin es el repositorio de donde hemos clonado nuestra copia en local. Como vemos, podemos seleccionar la rama del repositorio a la que empujar nuestros cambios, en el ejemplo dev, nuestra rama de desarrollo.



  
