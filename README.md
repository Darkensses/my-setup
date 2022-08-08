# Setup Darkensses

## Lenguajes 💻

### NodeJS

Pendiente

### Python

1. Ir a [Download Python | Python.org](https://www.python.org/downloads/)

2. Descargar la última version estable

3. Ejecutar el instalador

4. Seleccionar **Install launcher for all users (recommended)**

5. Seleccionar **Add Python to PATH**

6. Dar click en **Customize Installation**

7. Dejar todo seleccionado

8. Dar click en **Next**

9. Seleccionar **Install for all users**

10. Desmarcar **Associates file with Python**

11. Modificar la ruta de instalación por **C:\Python**

12. Dar click en **Install**

13. Dar click en **Disable path lenght limit**

14. Dar click en **Close**

15. Abrir un **CMD**

16. Ejecutar `python --version`

17. Verificar que la respuesta sea la versión instalada

### Java

De acuerdo a este [articulo](https://devexperts.com/blog/oracle-jdk-vs-openjdk-builds-comparison/), la opción adecuado para instalar Java es **AdoptOpenJDK** ya que es de código abierto y se puede usar en producción de forma gratuita.

1. Ir a https://adoptium.net/es/

2. Dar click en **Otras plataformas y versiones**

3. Seleccionar:
   
   1. Sistema Operativo: Windows
   
   2. Arquitectura: x64
   
   3. Tipo de paquete: JDK
   
   4. Version: 17 (o la más actual LTS)

4. Descargar el **.zip**

5. Descomprimir en **C:\Java**

6. Añadir Java a las variables de sistema:
   
   1. Abrir el menu de inicio y escribir *variables de entorno*
   
   2. Dar click en **Editar las variables de entorno del sistema**
   
   3. Dar click en el botón de **Variables de entorno...**
   
   4. Debajo de la categoría de **Variables de sistema**, dar click al botón **Nueva...**
   
   5. Nombrar la variable como `JAVA_HOME`
   
   6. En el campo de valor escribir `C:\Java\jdk-<version>`
   
   7. Dar click en Aceptar
   
   8. Seleccionar la varaible `Path` en la categoría de **Variables de sistema**
   
   9. Dar click en **Editar...**
   
   10. Dar click en **Nuevo**
   
   11. Escribir `%JAVA_HOME%\bin`
   
   12. Dar click en **Aceptar**



## IDEs 👨‍💻

### Visual Studio Code

1. Ir a https://code.visualstudio.com/#alt-downloads

2. Dar click en la opcion de **64 bit** de **System Installer**

3. Ejecutar el instalador

4. Aceptar el acuerdo de usuario

5. Dar click en **Siguiente >**

6. Asegurarse de que la ruta de instalación sea `C:\Program Files\Microsoft VS Code`

7. Dar click en **Siguiente >**

8. (Opcional: Crear carpeta del Menú Inicio) Dar click en **Siguiente >**

9. Seleccionar unicamente:
   
   1. Crear un acceso directo en el escritrio
   
   2. Agregar a PATH (disponible después de reiniciar)

10. Dar click en **Siguiente >**

11. Dar click en **Instalar**



### PyCharm

### IntelliJ



## Fuentes ✒

### Fira Code

### Meslo



## Tools 🧰

### Git

1. ir

2. click descargar

3. seleccionar x64

4. ejecutar

5. next

6. asegurar ruta c\program files\Git

7. next

8. solo seleccionat git lfs y (New!) Add a Git Bash Profile to Windows Terminal

9. next

10. (Opcional: Crear carpeta del Menú Inicio) Dar click en **Next**

11. Seleccionar Use Vim the ubiquitous text editor) as Git's default editor > next

12. Seleccionar Let Git decide > next

13. Seleccionar Git from the command line and also from 3rd-party software > next

14. Seleccionar Use bundled OpenSSH > next

15. Seleccionar Use the OpenSSl library > next

16. Seleccionar Checkout Windows-style, commit Unix-style line ending > next

17. Seleccionar Use MinTTY (the default terminal of MYSYS2) > next

18. Seleccionar Default (fast-forward or merge) > next

19. Seleccionar Git Credential Manager > next

20. Solo seleccionar Enable file system caching > next

21. no seleccionar nada

22. Dar click en Install

23. comprobar git -v



#### Configuracion ⚙

1. git config --global user.name “[firstname lastname]”

2. git config --global user.email “[valid-email]”

3. git config --global color.ui auto





### 7-Zip

### Windows Terminal

1. Abrir **Microsoft Store**

2. Buscar *Windows Terminal*

3. Dar click en **Obtener**



### Personalización 💅

#### Oh-my-posh

Se pueden seguir los pasos del tutorial

1. Abrir **Windows terminal**

2. Ejecutar el comando `winget install JanDeDobbeleer.OhMyPosh -s winget`

3. Cerrar y volver a abrir **Windows Terminal**

4. Abrir la configuración

5. Dar click en **Abrir archivo JSON** (se encuentra abajo a la izquierda)

6. Abrir `settings.json`en Visual Stuido Code

7. Agregar el atributo `font.face` y `font.size` debajo del atributo `defaults` en `profiles`: 
   
   ```json
   {
       "profiles":
       {
           "defaults":
           {
               "font":
               {
                   "face": "MesloLGM NF",
                   "size": 10,
               }
           }
       }
   }
   ```

8. Guardar los cambios

9. Dar click en **Guardar**

10. Cerrar la configuración

11. Ejecutar `notepad $PROFILE`

12. En caso de error, ejecutar `New-Item -Path $PROFILE -Type File -Force` y volver a ejecutar `notepad $PROFILE`

13. Agregar `oh-my-posh init pwsh | Invoke-Expression` en el bloc de notas que se abrió

14. Guardar cambios y cerrar

15. Recargar el perfil para que los cambios tomen efecto `. $PROFILE`. En caso de error, ejecutar primero `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser`



##### Tema 🎨

1. Ir a https://ohmyposh.dev/docs/themes

2. Dar click en el enlace del tema Atomic

3. En el repo, dar click en **Raw**

4. Click derecho > **Guardar Como** > **Guardar**

5. Copiar el archivo en `C:\Users\<YOUR_USER>\oh-my-posh\themes`

6. Abrir el perfil de Powershell, localizado en `C:\Users<YOUR_USER>\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1`

7. Editar el script, agregando el tema:
   
   ```shell
   oh-my-posh init pwsh --config "$env:USERPROFILE/oh-my-posh/themes/atomic.omp.json" | Invoke-Expression
   ```

8. Recargar el perfil para que los cambios tomen efecto `. $PROFILE`



#### Terminal-Icons

Este paquete sirve para poner iconos a las carpetas que se muestran en PowerShell

1. Ejecutar `Install-Module -Name Terminal-Icons -Repository PSGallery`

2. Abrir el perfil de Powershell, localizado en `C:\Users<YOUR_USER>\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1`

3. Editar el script, agregando al final `Import-Module -Name Terminal-Icons`

4. Recargar el perfil para que los cambios tomen efecto `. $PROFILE`
