# Guía de Configuración de Entornos de Desarrollo

> 📋 **Guía Técnica**: Esta documentación establece los procedimientos para configurar un entorno de desarrollo en C# y otros lenguajes. Incluye las configuraciones necesarias para mantener consistencia en el desarrollo de software.

> **Nota importante**: Este documento se enfoca en aspectos técnicos y procedimientos. Para análisis comparativos, reflexiones personales y conclusiones, utiliza el archivo `CONCLUSIONES_EVALUACION.md`.

**Autores**: Jhonny y Mario
**Fecha V0**: [Fecha de entrega inicial]
**Fecha V1**: [Fecha de entrega final]

---

## Visual Studio Code - Entorno Principal

### Instalación y Verificación

**Método de instalación:** [Desde la pagina oficial del Visual Studio Code: https://code.visualstudio.com/](screenshots/screenshot1.png)

> **💡 Sobre las imágenes**: Incluye capturas de pantalla para mostrar los diferentes pasos o resultados. Ejemplo: ![Descripción clara del contenido](screenshots/placeholder.png)`

**Proceso de instalación:**
- **Descarga:**
 `Paso 1` [Ir a la pagina *http://code.visualstudio.com/*,](screenshots/screenshot1.png).
 `Paso 2` hacer click en el boton *download for windows* o el sistema de su preferencia, se descargara un archivo insatalador como [VSCodeUserSETUP-X64](screenshots/screenshot3.png)
- **Opciones del instalador:** 
  `Paso 3` Buscaremos la direccion donde se guardo el archivo, ejecutamos el archivo, [aceptar terminos y licencias!](screenshots/screenshot4.png), dar click en next,
  `Paso 4` elegiremos la [ubicacion donde instalar o lo mantenemos con la configuracion predeterminada.](screenshots/screenshot5.png)
  `Paso 5` Elige si deseas cambiar el nombre de la carpeta de accesos directos en el menú Inicio o si no deseas instalar accesos directos en absoluto. [Haz clic en     Next.](screenshots/screenshot6.png)
  `Paso 6` Selecciona las tareas adicionales, por ejemplo: crear un icono en el escritorio o añadir opciones al menú contextual de Windows Explorer. [Haz clic en Next.](screenshots/screenshot7.png)
  `Paso 7` Haz clic en [Install para iniciar la instalación.](screenshots/screenshot8.png)
  `Paso 8` El programa está instalado y listo para usar. [Haz clic en Finish para finalizar la instalación y lanzar el programa.](screenshots/screenshot9.png)
- **Verificación:** Desde la interfaz, abrimos Visual Studio Code, si ves en la ventana principal con opciones como "Open Folder", "New File", etc., [la instalación fue exitosa.](screenshots/screenshot10.png)

*Es posible documentar múltiples métodos.*

### Uso Básico de VS Code

**Navegación y funcionalidades básicas:**

*La interfaz de VSCode se organiza en cinco áreas principales:*

`la barra de actividades` se sitúa en el extremo izquierdo y proporciona acceso directo a las vistas principales como Explorer, Search, Source Control, Run and Debug, y Extensions.

`La barra lateral` ocupa el espacio adyacente de la barra de actividades y muestra el contenido de la vista seleccionada. Cuando seleccionas el Explorer, por ejemplo, la barra lateral muestra la estructura de archivos y carpetas de tu proyecto actual.

`El grupo de edicion` constituye el área central donde se abren y editan los archivos. 

`EL Panel` se encuentra en la parte inferior y tiene la terminal integrada, los problemas detectados, la salida de depuración y los resultados de búsqueda.

`La Barra de Estados` en la parte inferior proporciona información contextual sobre el archivo actual, incluyendo el lenguaje de programación, la codificación, la posición del cursor y el estado del control de versiones.
[aqui veremos las áreas ya mencionadas](screenshots/screenshot13.png)

*Edición de código*
 en el grupo de edicion es donde se ejecuta esta funcion,practicamente donde se escribe el codigo.

  *Uso de la paleta de comandos*
-  representa una de las características más potentes. Accesible mediante *Ctrl+Shift+P (Windows/Linux)* o *Cmd+Shift+P (macOS)*, proporciona acceso instantáneo a prácticamente cualquier comando disponible en el editor.Desde allí puedes ejecutar cualquier acción, como:

  ºCambiar el tema [(Preferences: Color Theme)](screenshots/screenshot14.png)

  ºInstalar extensiones [(Extensions: Install Extensions)](screenshots/screenshot15.png)

  *Gestión de archivos y carpetas* 
  Los espacios de trabajo en VSCode permiten organizar proyectos complejos que involucran múltiples carpetas o repositorios. Un espacio de trabajo puede incluir configuraciones específicas, extensiones recomendadas y ajustes de depuración particulares como:

  ºAbrir una carpeta: [Archivo → Abrir carpeta](screenshots/screenshot11.png)

  ºCrear archivos: clic derecho en el Explorador → [Nuevo archivo.](screenshots/screenshot12.png)

  ºGuardar: Ctrl + S

### Personalización del Entorno

**Configuraciones aplicadas:** [Describir las personalizaciones que se realizaron]

*Ejemplos de configuraciones útiles (elegir las que se consideren relevantes):*

**Temas e iconos:**
Ejemplos:
- Se instalo una extension llamada *Palenight Theme* para Un tema elegante y atractivo, inspirado en Material Design, para Visual [Studio Code.](screenshots/screenshot16.png)
  
**Configuración de fuentes:**

Ejemplos:
- -Se instalo *Better Comments*
La extensión Comentarios mejorados te ayudará a crear comentarios más fáciles de entender en tu [código.](screenshots/screenshot17.png)

**Atajos de teclado útiles:**
Ejecutar archivo	Ctrl + F5
Abrir paleta de comandos	Ctrl + Shift + [P](screenshots/screenshot14.png)
Abrir configuración	[Ctrl + ,](screenshots/screenshot18.png)
Mover línea	Alt + ↑ o Alt + ↓
Ir a definición	[F12](screenshots/screenshot19.png)
Formatear documento	[Shift + Alt + F](screenshots/screenshot20.png)

**Configuración del editor:**

- Formateo automático al guardar
   *editor.formatOnSave": false*, lo cambiaremos a :
   *editor.formatOnSave": true,*
   Cada vez que guardas (Ctrl + S), el código se formatea automáticamente según las reglas del lenguaje o el formateador [configurado.](screenshots/screenshot22.png)

- Word wrap para líneas largas
-  *"editor.wordWrap": "off",*, lo cambiaremos a :
   *"editor.wordWrap": "on"*
Evita el scroll horizontal en líneas muy largas.
El texto se ajusta automáticamente al ancho de la ventana del [editor.](screenshots/screenshot22.png)

**Terminal integrada:**
- PowerShell como terminal predeterminado
  Esto Define que cada vez que abras la terminal integrada (Ctrl + ñ o Ctrl + ` ), se inicie una sesión de PowerShell en lugar de CMD u [otro shell.](screenshots/screenshot23.png)

  `Configuración de perfil personalizado`
 esta es una Estructura básica de configuración, en el archivo settings.json de VS Code escribimos:
{
  "terminal.integrated.profiles.windows": {
    "NombreDelPerfil": {
      "path": "ruta/al/ejecutable",
      "args": [],
      "env": {},
      "icon": "nombre-del-icono",
      "color": "terminal.ansiColor"
    }
  },
  "terminal.integrated.defaultProfile.windows": "NombreDelPerfil"}

  La ubicación del archivo de configuración la encontraras en:
  -Windows: %APPDATA%\Code\User\settings.json
  -Linux/macOS: ~/.config/Code/User/settings.json

  `Perfil de desarrollo PowerShell personalizado`
{
  "terminal.integrated.profiles.windows": {
    "PowerShell Dev": {
      "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
      "args": ["-NoLogo"],
      "env": {
        "DOTNET_ENVIRONMENT": "Development",
        "PATH": "${env:PATH};C:\\HerramientasInternas\\Scripts"
      },
      "icon": "terminal-powershell",
      "color": "terminal.ansiBlue"
    }
  },
  "terminal.integrated.defaultProfile.windows": "PowerShell Dev"
}
  Puedes definir perfiles adicionales
> **Personaliza según tus necesidades**: Estas son sugerencias basadas en prácticas comunes. Experimenta y documenta las configuraciones que encuentres más útiles para tu flujo de trabajo.> 💼 **Manual de Incorporación**: Esta guía establece los estándares del equipo para configurar entornos de desarrollo en C#. Cualquier nuevo desarrollador debe poder seguir estas instrucciones para configurar su entorno de trabajo de manera consistente con el resto del equipo.

### SDK .NET

**Proceso de instalación:**
Qué es?

El .NET SDK (Software Development Kit) contiene el compilador, las herramientas y las bibliotecas necesarias para crear, compilar y ejecutar aplicaciones en C#. 

1. **Descarga e instalación:** 

**DESCARGA**
  `Paso 1`Ir a la pagina oficial: [https://dotnet.microsoft.com/download](screenshots/screenshot24.png), selecciona la versión .NET 8.0 (LTS) o superior.

  `Paso 2` hacer click en el boton *descargar SDK X64 de .NET* o superior, se descargara un archivo insatalador [como:](screenshots/screenshot25.png) 

**Opciones del instalador:**
  `Paso 1` Buscaremos la direccion donde se guardo el archivo, ejecutamos el [archivo.exe](screenshots/screenshot25.png)
  
  `Paso 2` Ejecuta el instalador y sigue las instrucciones [predeterminadas.](screenshots/screenshot26.png)
  `Paso 3` al dar en *instalar* nos pedira permiso para instalacion le damos en *SI* y comenzara la [instalacion](screenshots/screenshot27.png)
  `Paso 4` esperamos que termine de instalar y por ultimo le damos en [cerrar](screenshots/screenshot28.png)
   
 **Verificación:** [Cómo comprobar que funciona]
`Paso 1` Despues de instalar podemos abrir la terminal integrada VS Code o una ventana de PowerShell y ejecutamos:

  dotnet [--version](screenshots/screenshot29.png)

`Paso 2` Luego verifica la información completa del entorno:

  dotnet [--info](screenshots/screenshot29.png)

### Configuración para C#

**Extensiones esenciales:**
- **Soporte oficial para C#**: Extensión que proporciona IntelliSense, debugging y compilación


**Configuraciones específicas para C#:** 
[Describir las configuraciones que se aplicaron, como formateo automático, intellisense, o configuraciones del compilador]

**Debugging básico:**
- Configuración de puntos de interrupción (breakpoints)
- Ejecutar y depurar
- Inspección de variables

> **Enfoque práctico**: Concentra tu documentación en las funcionalidades básicas que usarás día a día.

### Flujo de Trabajo con C#

**Creación de proyectos:**
[Documentar el proceso para crear proyectos C#]

**Estructura de proyecto:**
```csharp
// Incluir aquí un ejemplo del código desarrollado
// Comentarios sobre las decisiones tomadas
```

**Compilación y ejecución:**
[Proceso para compilar y ejecutar proyectos]

**Debugging:**
[Configuración y uso de debugging]

---

## Visual Studio - IDE Alternativo

### Instalación

**Proceso de instalación:**
- **Descarga:** [Versión recomendada - Community/Professional]
- **Componentes necesarios:** [Componentes específicos para C#]
- **Verificación:** [Cómo confirmar instalación correcta]

### Desarrollo con C#

**Creación de proyecto:**
[Describir el proceso para crear un proyecto C# en Visual Studio]

**Flujo de trabajo básico:**
- Compilación y ejecución
- Uso de Solution Explorer
- Debugging básico

---

## Configuración de Lenguaje Adicional

**Lenguaje seleccionado:** [Java/Python/Otro] - **Justificación:** [Por qué se eligió este lenguaje]

### Instalación del Entorno

**Runtime/SDK:**
- **Descarga e instalación:** [Proceso paso a paso]
- **Verificación:** [Cómo confirmar que funciona]

### Configuración en VS Code

**Extensiones por lenguaje:**

*Para Java:*
- **Paquete completo de Java**: Incluye compilación, debugging y gestión de proyectos

*Para Python:*
- **Soporte oficial de Python**: Extensión completa con intérprete y debugging

*Para otros lenguajes:*
- Busca la extensión oficial del lenguaje que proporcione soporte completo

**Configuraciones específicas aplicadas:**
[Documentar los ajustes que se realizaron, como configuración del intérprete, formateo automático, linting, etc.]

### Proyecto de Ejemplo

**Código desarrollado:**
```[lenguaje]
// Código de ejemplo aquí
// Comentarios explicativos
```

**Proceso de ejecución:**
[Describir cómo ejecutar el código]

---

## Configuraciones Recomendadas

**Configuraciones generales:**
[Documentar configuraciones que se consideran útiles para cualquier desarrollador]

**Herramientas adicionales:**
[Extensions, herramientas CLI, o utilidades que se consideran beneficiosas]

**Solución de problemas comunes:**
[Problemas frecuentes durante la configuración y sus soluciones]

**Recursos útiles:**
- Enlace [Enlace]: [Descripción]
- Documentación [Documentación]: [Descripción]

---
