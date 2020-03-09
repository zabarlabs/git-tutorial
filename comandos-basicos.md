# Comandos Básicos

En este capítulo vamos a adentrarnos en los comandos básicos de Git y con los que podremos realizar la gran mayoria de tareas relacionadas con este control de versiones.

## ¿Cómo obtener un repositorio Git?

Básicamente tenemos dos opciones para poder tener un repositorio Git

### 👉🏻 Inicializarlo en un directorio existente

Aquí tenemos que tener en cuenta si el directorio está vacio o ya contiene archivos y carpetas:

- Si el directorio esta vacio basta con utilizar el comando:  
   **`git init`**
- Si el directorio ya cuenta con contenido y queremos rastrear el mismo:

```java
$ git add .
$ git commit -m"Primer commit"
```

### 👉🏻 Clonar un repositorio existente

Existen varios tipo de repositorios en la nube (_GitHub, GitLab, GitBucket_) tanto con proyectos públicos como privados. Desde los repositorios públicos se nos permite descargar a local una copia para poder trabajar en ellos, mediante el comando:

- **`git clone <URL> <miDirectorio>`** : Se clona a un directorio con el nombre que le he indicado.

  {% hint style='tip' %}
  la diferencia entre clonar un proyecto o descargarlo en formato ZIP, es que clonado te traes todos los commits que se han realizado desde el comienzo.
  {% endhint %}

## 🔁 Ciclo de vida de los archivos en Git

Dentro de este ciclo de vida podemos encontrarnos con tres estados en los que se pueden encontrar los archivos:

- **Working Area**: es el espacio donde se guardan los archivos y las carpetas sin rastrear.
- **Staged Area**: es la zona intermedia, un area de preparación donde están los archivos que han sido editados.
- **Repositorio**: es la zona donde se guardan todas las modificaciones y cambios realizados. Es el contenido de la carpeta oculta **`.git`**

![Estados Git](_book/assets/3-stages-git.PNG)

- **`$ git status`**: permite conocer el estado de los archivos.
- **`$ git status -s`**: muestra el estado pero de una manera más reducida.
- **`$ git add <archivo1><archivo2><...>`**: comando que se utiliza para empezar a rastrear nuevos archivos.
- **`$ git add .`**: utilizando el punto añade todos los archivos a la vez.
- **`$ git commit -m"Mensaje del commit"`**: manda al repositorio los archivos preparadados en el Staged Area.
