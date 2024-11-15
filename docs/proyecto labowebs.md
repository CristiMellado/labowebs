**Autor: Cristina Mellado**
Proyecto Labowebs.

# Ejercicio de Git - Proyecto Labowebs.

[TOC]

# Trabajo en Local

## **Cuestiones**

1. Inicializa un nuevo repositorio Git en una carpeta llamada `"labowebs"`y agrega los archivos proporcionados en el aula virtual. Renombra la rama `master` a `main` , si es necesario. Realiza el primer commit. Muestra el log del repositorio.

```bash
git init
git add .
git branch -m master main
git commit -m "primer commit"
git log 
```

<img src="./proyecto labowebs.assets/image-20241114085850996.png" alt="image-20241114085850996" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114085952081.png" alt="image-20241114085952081" style="zoom:80%;" />

2. Incluye un fichero `.gitignore` para que los ficheros `README.md` , `LICENCE.txt` y `passwords.txt` sean ignorados por el control de versiones. Realiza el commit y muestra los logs del repositorio en una línea.

   ```bash
   notepad .gitignore
   git add .gitignore
   git commit -m "añadiendo .gitignore"
   git log --oneline
   ```
   

<img src="./proyecto labowebs.assets/image-20241114091139643.png" alt="image-20241114091139643" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114091302899.png" alt="image-20241114091302899" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114091242317.png" alt="image-20241114091242317" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114091331957.png" alt="image-20241114091331957" style="zoom:80%;" />

3. En el repositorio, crea los archivos `README.md` , `LICENCE.txt` y `passwords.txt` con algún contenido. Muestra el estado del repositorio. Muestra el listado de archivos ignorados.

   ```bash
   touch README.md
   touch LICENCE.txt
   touch passwords.txt
   notepad README.md
   notepad LICENCE.txt
   notepad passwords.txt
   git status
   git status --ignored
   git ls-files --ignored --exclude-standars --others
   ```
   

<img src="./proyecto labowebs.assets/image-20241114092553740.png" alt="image-20241114092553740" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114092906953.png" alt="image-20241114092906953" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114093128394.png" alt="image-20241114093128394" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114093244318.png" alt="image-20241114093244318" style="zoom:80%;" />

4. Crea una rama `feature-estilos` . Cámbiate a ella. 

   * Modifica el archivo `estilos.css` : propiedad color del body y de h2 : #ff0 propiedad background-color de header y footer: #7acffe .
   * Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje "actualizados estilos a azules".
   
   ```bash
   git branch feature-estilos
   git checkout feature-estilos
   git status 
   git add .
   git commit -m "actualizados estilos azules"
   
   ```
   
   <img src="./proyecto labowebs.assets/image-20241114094202023.png" alt="image-20241114094202023" style="zoom:80%;" />
   
   <img src="./proyecto labowebs.assets/image-20241114094640236.png" alt="image-20241114094640236" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114094721605.png" alt="image-20241114094721605" style="zoom:80%;" />

5. Vuelve a la rama `main` . En el archivo `index.html` añade un comentario donde se indique tu nombre como autor de la página. Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje ' añadido autor en index'. Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'.

   ```bash
   git checkout main
   git status
   git add .
   git commit -m "añadido autores en index"
   git log --oneline --graph --decorate
   ```

   <img src="./proyecto labowebs.assets/image-20241114094913711.png" alt="image-20241114094913711" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114095243304.png" alt="image-20241114095243304" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114095423527.png" alt="image-20241114095423527" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114095506906.png" alt="image-20241114095506906" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114095615766.png" alt="image-20241114095615766" style="zoom:80%;" />

6. Fusiona la rama `feature-estilos` en la rama `main .` Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'

   ```bash
   git merge feauture-estilos
   git log --oneline --graph --decorate
   ```

   ![image-20241114100023002](./proyecto labowebs.assets/image-20241114100023002.png)



# Trabajo en Remoto

## **Cuestiones**

1. Continúa con el repositorio `labowebs` . Añade el repositorio a Sourcetree.

   
   
   <img src="./proyecto labowebs.assets/image-20241114100750689.png" alt="image-20241114100750689" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114100848603.png" alt="image-20241114100848603" style="zoom:80%;" />

2. Crea un repositorio remoto y sube al remoto los ficheros de tu repositorio local. Debes subir todas las ramas.

   

```bash
git remote add origin https://github.com/CristiMellado/labowebs.git
git remote -v
git push -u origin --all
```

​		El comando git remote add origin añade el remoto usando la URL del nuevo repositorio remoto, después 		se comprueba que se añade correctamente con el comando git remote -v y por último se suben los cambios y 		todas las ramas con el comando git push -u origin -all.

<img src="./proyecto labowebs.assets/image-20241114183045510.png" alt="image-20241114183045510"  />

![image-20241114183228787](./proyecto labowebs.assets/image-20241114183228787.png)

<img src="./proyecto labowebs.assets/image-20241114183528207.png" alt="image-20241114183528207" style="zoom: 80%;" />

3. Crea una rama `feature-index.` Añade el siguiente código dentro de la  <section class ="about">. Añade los cambios y crea un commit. Sube los cambios al remoto.

​	<img src="./proyecto labowebs.assets/image-20241114183838517.png" alt="image-20241114183838517" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114184551772.png" alt="image-20241114184551772" style="zoom:80%;" />



<img src="./proyecto labowebs.assets/image-20241114184338141.png" alt="image-20241114184338141" style="zoom:80%;" />



<img src="./proyecto labowebs.assets/image-20241114184421560.png" alt="image-20241114184421560" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114184817867.png" alt="image-20241114184817867" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114184930448.png" alt="image-20241114184930448" style="zoom:80%;" />

4. En el repositorio local, fusiona la rama `feature-index` en la rama `main` .

   <img src="./proyecto labowebs.assets/image-20241114185630045.png" alt="image-20241114185630045" style="zoom:80%;" />

   <img src="./proyecto labowebs.assets/image-20241114185733332.png" alt="image-20241114185733332" style="zoom:80%;" />

5. Edita el fichero `contacto.html.` Borra unas líneas. Muestra los ficheros con cambios pendientes y las diferencias. Añade los cambios y haz un commit.

   <img src="./proyecto labowebs.assets/image-20241114190210247.png" alt="image-20241114190210247"  />

<img src="./proyecto labowebs.assets/image-20241114190352146.png" alt="image-20241114190352146" style="zoom:80%;" />

6. Te das cuenta del error. Deshaz el commit anterior. Captura el estado actual del repositorio.
   * Al hacer click en "reset current branch to this commit" me permite eliminar el commit posterior al seleccionado dejando como último commit el seleccionado, los cambios del commit borrado vuelven al área de staging.

<img src="./proyecto labowebs.assets/image-20241114190801064.png" alt="image-20241114190801064" style="zoom:80%;" />

* En la siguiente imagen muestra que se eliminó correctamente el commit "Borrando líneas en contacto.html".

  y tras descartar los cambios en el documento "contacto.html" se vuelven a tener las líneas borradas. 

<img src="./proyecto labowebs.assets/image-20241114191114340.png" alt="image-20241114191114340" style="zoom:80%;" />

7. Crea una rama `feature-mapa.` Incluye este código en el archivo `contacto.html` . Añade los cambios. Realiza un commit. Sube los cambios al remoto. Muestra en el remoto los cambios del archivo `contacto.html` en la rama `feature-mapa`.

   ![image-20241114192802265](./proyecto labowebs.assets/image-20241114192802265.png)

<img src="./proyecto labowebs.assets/image-20241114193047293.png" alt="image-20241114193047293" style="zoom:80%;" />

![image-20241114193128180](./proyecto labowebs.assets/image-20241114193128180.png)

<img src="./proyecto labowebs.assets/image-20241114193223883.png" alt="image-20241114193223883" style="zoom:80%;" />

![image-20241114193452982](./proyecto labowebs.assets/image-20241114193452982.png)

8. En GitHub, en la rama `main` , fusiona la rama `feature-mapa.` Baja los cambios del remoto a local. Deja los dos repositorios sincronizados.

   

<img src="./proyecto labowebs.assets/image-20241114195000971.png" alt="image-20241114195000971" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241114195323882.png" alt="image-20241114195323882" style="zoom:80%;" />

```bash
git pull origin main
```

<img src="./proyecto labowebs.assets/image-20241114195839314.png" alt="image-20241114195839314"  />



# Conflictos

## **Cuestiones**

1. Crea una rama `hotfix-js` . Cámbiate a ella. Añade este código en el fichero `script.js.` Confirma el cambio y haz un commit. (Fíjate en los números de línea...)

   <img src="./proyecto labowebs.assets/image-20241115084204454.png" alt="image-20241115084204454" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115084359372.png" alt="image-20241115084359372" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115084457913.png" alt="image-20241115084457913" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115085040248.png" alt="image-20241115085040248" style="zoom:80%;" />

2. Vuelve a la rama `main`. En el fichero `script.js` en las mismas líneas que en la cuestión anterior, añade el código siguiente. Confirma el cambio y haz un commit.

   <img src="./proyecto labowebs.assets/image-20241115084736772.png" alt="image-20241115084736772" style="zoom:80%;" />

   <img src="./proyecto labowebs.assets/image-20241115084842342.png" alt="image-20241115084842342" style="zoom:80%;" />

   

   <img src="./proyecto labowebs.assets/image-20241115085000748.png" alt="image-20241115085000748" style="zoom:80%;" />

   

   <img src="./proyecto labowebs.assets/image-20241115085112541.png" alt="image-20241115085112541" style="zoom:80%;" />

3. Fusiona la rama `hotfix-js en main` . Debe producirse un conflicto. Resuélvelo. Cuando termines la resolución del conflicto sube los cambios al remoto. Deja los repositorios sincronizados.

   <img src="./proyecto labowebs.assets/image-20241115085732423.png" alt="image-20241115085732423" style="zoom:80%;" />

   
   
   ![image-20241115085830847](./proyecto labowebs.assets/image-20241115085830847.png)

<img src="./proyecto labowebs.assets/image-20241115090620121.png" alt="image-20241115090620121" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115090749243.png" alt="image-20241115090749243" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115090841178.png" alt="image-20241115090841178" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115091951789.png" alt="image-20241115091951789" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115092226911.png" alt="image-20241115092226911" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115092357631.png" alt="image-20241115092357631" style="zoom:80%;" />

![image-20241115092449073](./proyecto labowebs.assets/image-20241115092449073.png)

<img src="./proyecto labowebs.assets/image-20241115092716164.png" alt="image-20241115092716164" style="zoom:80%;" />



# Subida de documentación

En la carpeta del proyecto labowebs añade una carpeta `docs` . Copia en esa carpeta el fichero markdown y la carpeta con las imágenes. Incluye también el pdf . Añade todo al repositorio. Súbelo al remoto.

```bash
mdkir docs 
git add .
git commit -m "añadiendo documentación"
```

<img src="./proyecto labowebs.assets/image-20241115101746052.png" alt="image-20241115101746052" style="zoom:80%;" />

<img src="./proyecto labowebs.assets/image-20241115103411383.png" alt="image-20241115103411383" style="zoom:80%;" />

![Captura de pantalla 2024-11-15 110046](./proyecto labowebs.assets/Captura de pantalla 2024-11-15 110046.png)



![Captura de pantalla 2024-11-15 110105](./proyecto labowebs.assets/Captura de pantalla 2024-11-15 110105.png)

![Captura de pantalla 2024-11-15 110113](./proyecto labowebs.assets/Captura de pantalla 2024-11-15 110113.png)

![Captura de pantalla 2024-11-15 110119](./proyecto labowebs.assets/Captura de pantalla 2024-11-15 110119.png)
