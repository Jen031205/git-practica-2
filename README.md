# git practica 2
Taller GIT. Práctica 2.
Guarda los comandos realizados, así como los resultados(capturas), integrarlo dentro del mismo repositorio

## Trabajar con un proyecto HTML y un repositorio local.
- Crea una carpeta practica-taller-git en tu pc.
- Inicializa el repositorio. 
 ```bash
 git init
 ```
- Crea el fichero index.html con un html simple.
- Comprueba que el repositorio a detectado el cambio. 
```bash
git status
```
- Añade el fichero al stage. 
```bash
git add index.html.
```
<img width="921" height="509" alt="image" src="https://github.com/user-attachments/assets/57885f35-9023-4184-b2d4-86d6447536cf" />


- Confirma los cambios. 
```bash
git commit -m “added index file”
```
- Añade un fichero description.html y edita index.html.
- Comprueba que ha detectado el nuevo fichero y la modificación de index.
```bash
git status
git diff
```
- Crea un fichero TODO.txt de tareas pendientes.
- Comprueba que git ha detectado el nuevo fichero. 
```bash
git status
```
- Ignora el fichero TODO.txt ya que es donde anotaremos nuestras tareas personales y no debe formar parte del proyecto. Para ello crea un fichero .gitignore con la linea TODO.txt.
- Comprueba que ya no detecta el nuevo fichero TODO.txt (si que detectara el .gitignore claro). 
```bash
git status
```
- Añade y confirma el .gitignore.
- Puedes continuar añadiendo ficheros html, css e imágenes para probar el repositorio.

  <img width="921" height="458" alt="image" src="https://github.com/user-attachments/assets/a51ef434-ffab-49a6-b231-acd23b35c1c5" />



## Haz un fork del repositorio creado para la práctica del taller:
- Entra en https://github.com/
- Accede a tu cuenta.
- Accede al repositorio del profesor https://github.com/lalobarri/git-practica-2.git
- Pulsa el botón fork (parte superior derecha) para crearte una copia del mismo en tu cuenta.
- Clona el repositorio en tu equipo *en otra carpeta diferente que la llamaremos 'git-practica-2'*. Quedará algo parecido a lo siguiente:
```bash
git clone https://github.com/[tu-nombre-de-usuario]/git-practica-2.git
```
<img width="921" height="451" alt="image" src="https://github.com/user-attachments/assets/bda72877-114f-4d45-911f-e757157aec6b" />

- Crea un nuevo fichero en el proyecto que se llame [tu-nombre-de-usuario].html
- Edita el fichero añadiendo como título tu nombre, algún texto y lo que desees en el.
- Añade el fichero al repositorio.
  <img width="921" height="631" alt="image" src="https://github.com/user-attachments/assets/8cd33ef5-06be-4dc5-9e37-d0d32299521d" />

- Súbelo al repositorio remoto (github). 
```bash
git push
```
- Crea una rama develop y cámbiate a ella.
```bash
git checkout -b develop
```
- Realiza cambios en el proyecto, confírmalos y súbelos al repositorio remoto.
```bash
git status
git add *
git commit -m "Mensaje del commit..."
git push origin
```
- Desde github crea un pull request de la rama develop a main.
- Fusiona la rama develop con en main. No deberías de tener ningún conflicto.
- Haz nuevos cambios en el proyecto siguiendo el flujo de trabajo git flow.


# Preguntas y Respuestas

## 1. ¿Qué sucede cuando hacemos un git add?

**Respuesta:**
El comando `git add` agrega los cambios realizados en uno o varios archivos al área de preparación (staging area). Esto indica a Git qué cambios se incluirán en el próximo commit.

---

## 2. ¿Qué sucede cuando hacemos un git commit? ¿Dónde está ese commit?

**Respuesta:**
El comando `git commit` crea un registro permanente de los cambios que se encuentran en el área de preparación. Ese commit se almacena en el repositorio local dentro de la carpeta `.git`.

---

## 3. ¿Por qué al hacer git commit todavía no está disponible ese commit en el repositorio remoto?

**Respuesta:**
Porque el commit se guarda únicamente en el repositorio local. Git no envía automáticamente los cambios al repositorio remoto después de realizar un commit.

---

## 4. ¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de GitHub?

**Respuesta:**
Debemos utilizar el comando `git push` para enviar los commits del repositorio local al repositorio remoto en GitHub.

---

## 5. ¿Qué diferencia hay entre hacer un fork o crear una nueva rama?

**Respuesta:**
Un fork crea una copia completa de un repositorio en otra cuenta de GitHub, permitiendo trabajar de forma independiente. Una rama crea una línea de desarrollo separada dentro del mismo repositorio para realizar cambios sin afectar la rama principal.

---

## 6. ¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?

**Respuesta:**

```bash
git branch nombre-rama
```

Este comando crea la rama, pero mantiene al usuario en la rama actual.

---

## 7. ¿Cuál es la diferencia entre los comandos git switch y git checkout al trabajar con ramas?

**Respuesta:**
`git switch` fue creado específicamente para cambiar entre ramas y resulta más sencillo de usar. `git checkout` es un comando más antiguo que además de cambiar ramas puede restaurar archivos y realizar otras tareas.

---

## 8. ¿Qué es una rama por defecto (como main o master) y por qué es importante?

**Respuesta:**
Es la rama principal del repositorio donde normalmente se almacena la versión estable y oficial del proyecto. Es importante porque sirve como referencia para el desarrollo y la integración de cambios.

---

## 9. ¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?

**Respuesta:**

```bash
git branch
```

Este comando muestra todas las ramas locales y marca con un asterisco la rama actual.

---

## 10. En el contexto de Git, explica con tus propias palabras qué es una rama (branch) y cuál es su beneficio principal al trabajar en un proyecto de software.

**Respuesta:**
Una rama es una línea independiente de desarrollo dentro de un repositorio. Permite trabajar en nuevas funciones, correcciones o pruebas sin modificar directamente la versión principal del proyecto. Su principal beneficio es facilitar el trabajo paralelo y evitar conflictos durante el desarrollo.

---

## 11. ¿Qué ha pasado con el contenido de la carpeta practica-taller-git? ¿Por qué no la podemos ver en nuestro repositorio remoto de GitHub?

**Respuesta:**
La carpeta `practica-taller-git` corresponde a un repositorio local diferente al repositorio clonado desde GitHub. Como nunca se vinculó a un repositorio remoto ni se realizó un `git push`, su contenido permanece únicamente en la computadora local y no aparece en GitHub.

*Utilice un formato que permita distinguir entre sus preguntas y respuestas*
