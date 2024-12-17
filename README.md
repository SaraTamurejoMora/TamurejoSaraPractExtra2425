---

## **Actividad: `git add` y Patrones**

---

### **Estructura Inicial del Proyecto**
1. Crea la siguiente estructura de archivos y directorios:
   ```bash
   mkdir -p proyecto-patrones/{docs,scripts,images,temp}
   touch proyecto-patrones/{docs/{manual.txt,guia.md,readme.txt},scripts/{app.js,utils.py,config.js},images/{logo.png,icon.jpg,banner.gif},temp/{pruebas.log,debug.txt,draft.md}}
   ```

![estructura](https://github.com/user-attachments/assets/f91784b9-d6da-432c-b92a-24127b8d4692)

2. Verifica que la estructura es la siguiente:

   ```
   proyecto-patrones/
   ├── docs/
   │   ├── manual.txt
   │   ├── guia.md
   │   ├── readme.txt
   ├── scripts/
   │   ├── app.js
   │   ├── utils.py
   │   ├── config.js
   ├── images/
   │   ├── logo.png
   │   ├── icon.jpg
   │   ├── banner.gif
   ├── temp/
       ├── pruebas.log
       ├── debug.txt
       ├── draft.md
   ```
   - Con _tree proyecto-patrones_ miro si la estructura es correcta y tiene todos los archivos creados.
     ![Tree](https://github.com/user-attachments/assets/c3032a52-1766-4a31-8b10-a688d44dcc1f)


3. Inicializa el repositorio y haz un commit inicial.
 - Con _git init ._ inicio el repositorio.
   ![iniciar repo](https://github.com/user-attachments/assets/f67487a1-3351-4107-8124-a10c1fce3cb7)

   
 - Hago _git add ._ para añadir todos los archivos, ya que si no, no puedo hacer el commit.
   ![Add todo](https://github.com/user-attachments/assets/d7270467-4f07-4d27-a64e-ca11eb6272f8)
 - _git commit -m "Estructura base"_ (Hago el primer commit)
 - _git log_ para ver el historial de commits
   
  ![primer commit](https://github.com/user-attachments/assets/131a4e52-96cd-4590-80eb-b7a0e5491cd7)

---

### **COMENZAMOS**

#### **1. Prepara archivos con patrones simples**

1. Añade  **solo** los archivos `.txt` que están en la carpeta `docs/` y muestra el estado.

- Uso _nano_ para editar todos los archivos .txt.
![Editar txt](https://github.com/user-attachments/assets/00d0a6a8-7d6b-4410-8afe-3648797d5ad0)
![edit debug](https://github.com/user-attachments/assets/fd2a053a-c552-474e-8bdd-9f479ef9d567)


- Hago _git status_ para ver el status de los archivos .txt que he editado sin añadirlos.
![Status txt](https://github.com/user-attachments/assets/01690dec-773b-4992-ba1a-45f1f33dbb92)

- _git add docs/*.txt_ para añadir solo los .txt de la carpeta /docs. Se puede ver que los demás no se han añadido.
![add txt](https://github.com/user-attachments/assets/61a46b69-6112-4ac1-97be-47393ae569fe)


2. Haz un commit.

-_git commit -m "Archivos txt de doc"_
![commit txt](https://github.com/user-attachments/assets/6250595e-f366-4506-843d-b8340ec91260)

---

#### **2. Trabaja con subdirectorios y extensiones**

1. Añade **todos los archivos `.js`** del directorio `scripts/` pero **excluye `config.js`** y muestra el estado.

- _nano_ para editar el contenido de los .js, así están modificados y puedo añadirlos luego.
  ![modificar js](https://github.com/user-attachments/assets/9ffb35c1-bf70-43f6-a370-f0a4e41d0ac4)

- _git add scripts/*.js -- ':!scripts/config.js'_ para añadir todos los archivos excepto config.js
  
![add  js](https://github.com/user-attachments/assets/583e489e-14bb-4417-b6fe-6b3d2c646e7e)

2. Haz un commit con los cambios.
   
-_git commit -m "Archivos js excepto config"_
![comit js](https://github.com/user-attachments/assets/146bf758-2a3c-452d-b289-0482983679c1)

---

#### **3. Máscaras en niveles**

1. Añade **todas las imágenes excepto las que terminan en `.gif`**

- _nano_ edito todas las imagenes para luego poder añadir solo las que pide el ejercicio.
- _git status_ para ver que están modificadas pero sin añadir.
  ![modificar imagenes](https://github.com/user-attachments/assets/b9fabda6-2af6-43a9-a42b-3402c932fbd3)

- _git add * ':!*.gif'_ para añadir todas las imagenes menos las que tienen extensión .gif.
![excepto gif](https://github.com/user-attachments/assets/732138f8-a40a-44f9-9fbb-e301f6fbd318)

2. Confirma que los archivos `.png` y `.jpg` están en el área de preparación y muestra el estado.
- _git status_ para ver que se han subido todas las imagenes menos los .gif.
  ![Imagenes añadidas](https://github.com/user-attachments/assets/73eac040-4b19-418a-b01e-bbbf7e67dc1d)

3. Haz un commit.
-_git commit -m "Imagenes menos gif"_
   ![commit imagenes](https://github.com/user-attachments/assets/bfde8c12-a5ff-4b08-978e-327092d9f31e)

---

#### **4. Sube el repositorio Git Local al Remoto**

1. Ya sabes como hacerlo, si no te acuerdas tienes aquí la [guía de comandos](https://github.com/VelezBeatriz/ITB-M08-DAW1/blob/main/README.md)
  - _git remote add proyecto-patrones https://github.com/SaraTamurejoMora/TamurejoSaraPractExtra2425.git_ para enlazar el repositorio local con el remoto.
  - _git branch_ para revisar en que rama estoy actualmente
  - _git push proyecto-patrones master_ para subir al remoto los archivos del local
    ![enlazar repo](https://github.com/user-attachments/assets/9d203d77-d4dc-4087-a434-86bc29222076)


   
