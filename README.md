# Instalacion-de-git
procedimiento
¡Perfecto! Vamos a ver **cómo instalar y configurar Git** paso a paso en una computadora con **Windows** (aunque también te incluyo breve nota para Linux/Mac al final). Este procedimiento es **para principiantes**.

---

## 🔹 1. Verificar si ya tienes Git instalado

1. Abre la consola de Windows:

   * Presiona `Win + R`, escribe `cmd` y presiona **Enter**.
2. Escribe el siguiente comando:

   ```bash
   git --version
   ```
3. Si Git ya está instalado, verás algo como:

   ```
   git version 2.44.0.windows.1
   ```

   Si dice que **no se reconoce el comando**, continúa con la instalación.

---

## 🔹 2. Descargar Git

1. Abre tu navegador y entra a la página oficial:
   🔗 [https://git-scm.com](https://git-scm.com)
2. Da clic en **Download for Windows**.
3. Se descargará un archivo ejecutable (ejemplo: `Git-2.xx.x-64-bit.exe`).

---

## 🔹 3. Instalar Git en Windows

1. Haz doble clic en el instalador.
2. Acepta la licencia (**Next**).
3. Elige la carpeta de instalación (deja la predeterminada).
4. **Seleccionar componentes**: deja las opciones por defecto.
5. **Editor por defecto**: puedes dejar "Vim" o elegir **Notepad++/VS Code**.
6. **PATH environment**: selecciona "Git from the command line and also from 3rd-party software".
7. **Línea de final de archivo**: deja la opción recomendada.
8. Finaliza la instalación presionando **Install** y luego **Finish**.

> ✅ Ahora Git estará disponible desde la terminal `cmd`, `PowerShell` y también desde **Git Bash** (que se instala automáticamente).

---

## 🔹 4. Configurar Git por primera vez

Abre la terminal (cmd, PowerShell o Git Bash) y escribe:

1. **Configurar nombre de usuario:**

   ```bash
   git config --global user.name "Tu Nombre"
   ```

2. **Configurar correo electrónico:**

   ```bash
   git config --global user.email "tuemail@example.com"
   ```

3. **Verificar configuración:**

   ```bash
   git config --list
   ```

---

## 🔹 5. Generar y agregar una clave SSH (opcional, recomendado)

Esto sirve para conectarte a **GitHub/GitLab/Bitbucket** sin poner tu usuario y contraseña cada vez.

1. Generar clave SSH:

   ```bash
   ssh-keygen -t rsa -b 4096 -C "tuemail@example.com"
   ```

   Presiona **Enter** en cada paso (sin contraseña si no quieres).

2. Copiar tu clave pública:

   ```bash
   type %userprofile%\.ssh\id_rsa.pub
   ```

3. Ve a tu cuenta de GitHub → **Settings → SSH and GPG keys → New SSH key** → Pega tu clave.

---

## 🔹 6. Probar que todo funciona

1. Crea una carpeta de prueba:

   ```bash
   mkdir prueba_git
   cd prueba_git
   ```
2. Inicia un repositorio:

   ```bash
   git init
   ```
3. Crea un archivo:

   ```bash
   echo "Hola Git" > hola.txt
   ```
4. Agrega y haz commit:

   ```bash
   git add .
   git commit -m "Primer commit"
   ```
5. Si no hubo errores, ¡Git ya está listo! 🎉

---

## 🔹 Notas rápidas para Linux y Mac

* En Linux:

  ```bash
  sudo apt install git   # Debian/Ubuntu
  sudo dnf install git   # Fedora
  ```
* En Mac:

  ```bash
  brew install git
  ```

---

### 📌 Resumen rápido de comandos iniciales

```bash
git --version                 # Ver versión
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"
git config --list             # Ver configuración
git init                      # Iniciar repositorio
git add .                     # Agregar cambios
git commit -m "Mensaje"       # Guardar cambios
```

---

¿Quieres que también te haga **una guía en Word o PDF** con capturas de pantalla para que tus estudiantes la sigan fácil?
