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
- **Soporte oficial para C#**: 
 `Paso 1` Abre Visual Studio Code.
 `Paso 2` Ve al menú de Extensiones o presiona *Ctrl+Shift+X* (Windows/Linux) o *Cmd+Shift+X* [(Mac).](screenshots/screenshot30.png)
 `Paso 3`En la barra de búsqueda escribe el nombre de la extensión. Por ejemplo:
         C# (la oficial de Microsoft)
 Haz clic en la extensión que aparece en los resultados y Presiona [Instalar.+](screenshots/screenshot31.png)

**Configuraciones específicas para C#:** 
[Describir las configuraciones que se aplicaron, como formateo automático, intellisense, o configuraciones del compilador]
`Formateo automático del código`
Puedes configurar VS Code para que formatee automáticamente el código al guardar o pegar:

  Archivo: .vscode/settings.json
  {
    "[csharp]": {
    "editor.formatOnSave": true,
    "editor.formatOnPaste": true,
    "editor.defaultFormatter": "ms-dotnettools.csharp"
  }
  } 
 Esto usa el formateador integrado de la extensión de C# de Microsoft.
 Si usas .editorconfig, también puedes definir reglas más específicas de estilo (indentación, espacios, llaves, etc.).

 `IntelliSense y análisis de código`
La extensión oficial de C# (basada en OmniSharp o el nuevo LSP) habilita autocompletado, sugerencias y diagnósticos de errores en tiempo real.
Puedes ajustar su comportamiento con estas opciones:

  Archivo: .vscode/settings.json

  {
    "csharp.suppressDotnetInstallWarning": true,
    "omnisharp.enableRoslynAnalyzers": true,
    "omnisharp.enableEditorConfigSupport": true,
    "omnisharp.enableImportCompletion": true,
    "omnisharp.autoStart": true
  }
Estas opciones activan análisis avanzados (Roslyn), lectura de configuraciones .editorconfig y completado automático inteligente.

 `Configuración del compilador y ejecución`

Para controlar cómo se ejecutan o compilan tus proyectos C#, VS Code usa los archivos generados por .NET:
tasks.json → Define cómo se compila el proyecto (dotnet build)
launch.json → Define cómo se ejecuta o depura (dotnet run)
Un ejemplo básico:

// .vscode/launch.json
  {
    "version": "0.2.0",
    "configurations": [
      {
        "name": "Ejecutar programa C#",
        "type": "coreclr",
        "request": "launch",
        "preLaunchTask": "build",
        "program": "${workspaceFolder}/bin/Debug/net8.0/MiProyecto.dll",
        "cwd": "${workspaceFolder}",
        "console": "integratedTerminal",
        "stopAtEntry": false
      }
    ]
  }  

**Debugging básico:**
`Establecer un punto de interrupción e iniciar el depurador`
*Introducción a los puntos de interrupción en el depurador de Visual Studio*
Los puntos de interrupción constituyen una de las técnicas de depuración más importantes en los cuadros de herramientas de los desarrolladores. Puedes establecer puntos de interrupción donde quieras pausar la ejecución del depurador. Por ejemplo, es posible que desee ver el estado de las variables de código o examinar la pila de llamadas en un determinado punto de interrupción.

*Establecimiento de puntos de interrupción en el código fuente*
Puede establecer un punto de interrupción en cualquier línea de código ejecutable. Por ejemplo, eche un vistazo a este sencillo código de C# que crea un bucle simple.

    C#
    int testInt = 3;

    for (int i = 0; i < 10; i++)
    {
      testInt += i;
    }

Puede establecer un punto de interrupción en la línea de código con la asignación de variables *(int testInt = 3)*, el bucle for o cualquier código dentro del bucle for. No se puede establecer un punto de interrupción en las firmas de método, las declaraciones de un espacio de nombres o una clase, o bien las declaraciones de variables si no hay ninguna asignación y no hay ningún captador o establecedor.

Para establecer un punto de interrupción en el código fuente:

  Haga clic en el margen izquierdo situado junto a una línea de código. También puede seleccionar la línea y presionar *F9* y seleccionar *Depurar>Alternar punto de interrupción*, o hacer clic con el botón derecho y seleccionar *Punto de interrupción>Insertar punto de interrupción*. El punto de interrupción aparece como un punto rojo en el margen izquierdo.

Para la mayoría de los lenguajes (incluido C#), Visual Studio resalta automáticamente el punto de interrupción y las líneas de ejecución actuales. Para algunos lenguajes, como C++, que no está resaltado de forma predeterminada, puede activar el resaltado del punto de interrupción y las líneas actuales.
Abra el cuadro de diálogo *Opciones de herramientas*>, expanda la sección *Depuración*> y active la casilla *Resaltar toda la línea de origen para los puntos de interrupción y la instrucción actual (solo C++)*. [Seleccione *Aceptar* para aplicar el cambio.](screenshots/screenshot32.png)

`Ejecutar y depurar`
Para depurar, presione *F5* o seleccione *Depurar>Iniciar depuración*.

Al depurar, la ejecución se detiene en el punto de interrupción, antes de que se ejecute el código de esa línea. El símbolo del punto de interrupción muestra una flecha amarilla.

En el punto de interrupción del ejemplo siguiente, el valor de testInt sigue siendo 3. Por lo tanto, el valor no ha cambiado desde que se inicializó la variable (se estableció en un valor de 3) porque la instrucción en amarillo aún no se ha [ejecutado.](screenshots/screenshot33.png)
Cuando el depurador se detiene en el punto de interrupción, se puede consultar el estado actual de la aplicación, incluidos los valores de variable y la pila de llamadas.
[Por ejemplo, en la ilustración siguiente, puede ver el valor de testInt en una sugerencia de datos y en la ventana de *variables locales.*](screenshots/screenshot34.png)
Estas son algunas instrucciones generales para trabajar con puntos de interrupción.

El punto de interrupción es un comando de alternancia. Puede hacer clic en él, presionar F9, o bien usar *Depurar>Alternar punto de interrupción para eliminarlo o volver a insertarlo.*

Para deshabilitar un punto de interrupción sin eliminarlo, mantenga el puntero sobre él o haga clic con el botón derecho y seleccione *Deshabilitar punto de interrupción*. Los puntos de interrupción deshabilitados aparecen como puntos vacíos en el margen izquierdo o en la ventana *Puntos de interrupción*. Para volver a habilitar un punto de interrupción, mantenga el puntero sobre él o haga clic con el botón derecho y seleccione *Habilitar punto de interrupción*.

Establezca condiciones y acciones, agregue y edite etiquetas o exporte un punto de interrupción; para ello, haga clic con el botón derecho en él y seleccione el comando adecuado, o mantenga el puntero sobre él y seleccione el icono Configuración.

*Tipos de puntos de interrupción*
Visual Studio admite diferentes tipos de puntos de interrupción para admitir diferentes escenarios de depuración, como puntos de interrupción condicionales que solo se activan en función de criterios especificados. Para obtener más información, consulte Utilice el tipo correcto de punto de interrupción.

*Administrar puntos de interrupción en la ventana Puntos de interrupción*

En la ventana *Puntos de interrupción* se pueden ver y administrar todos los puntos de interrupción de la solución. Esta ubicación centralizada es especialmente útil en una solución grande o para escenarios de depuración complejos en los que los puntos de interrupción son críticos.

En la ventana *Puntos de interrupción* se pueden buscar, ordenar, filtrar, habilitar/deshabilitar o eliminar puntos de interrupción. También puede establecer condiciones y acciones, o agregar una nueva función o punto de interrupción de datos.

Para abrir la ventana *Puntos de interrupción*, seleccione *Depurar>Ventanas>Puntos de interrupción*, o bien presione [*CTRL+Alt+B*.](screenshots/screenshot35.png)
Para seleccionar las columnas que se van a mostrar en la ventana Puntos de interrupción, seleccione Mostrar columnas. Seleccione un encabezado de columna para ordenar la lista de puntos de interrupción por esa columna.

*Etiquetas de puntos de Interrupción*
Puede usar etiquetas para ordenar y filtrar la lista de puntos de interrupción en la ventana de 'Puntos de interrupción' *y*.

  -Para agregar una etiqueta a un punto de interrupción, haga clic con el botón derecho en el punto de interrupción en el código fuente o en la ventana *Puntos de interrupción* y, después, seleccione *Editar etiquetas*. Agregue una etiqueta nueva o elija una existente y, después, seleccione *Aceptar*.

  -Para ordenar la lista de puntos de interrupción en la ventana *Puntos de interrupción*, seleccione *Etiquetas, Condiciones* u otros encabezados de columna. Para seleccionar las columnas que desea mostrar, seleccione *Mostrar columnas* en la barra de herramientas.

*Grupos de puntos de Interrupción*
En escenarios de depuración complejos, es posible que desee crear grupos de puntos de interrupción para organizar los puntos de interrupción. Esto le permite habilitar y deshabilitar rápidamente agrupaciones lógicas de puntos de interrupción, en función del escenario actual que está intentando depurar.

Puede crear puntos de interrupción en la ventana de *Puntos de interrupción* seleccionando *Nuevo > Grupo de puntos de interrupción* y proporcionando un nombre para el grupo. Para agregar un punto de interrupción a un grupo, haga clic con el botón derecho en el punto de interrupción y elija *Agregar al grupo de puntos de interrupción><nombre de grupo>*. O bien, arrastre y coloque los puntos de [interrupción en el grupo deseado.](screenshots/screenshot36.png)

Para establecer un grupo de puntos de interrupción predeterminado, haga clic con el botón derecho en un grupo y seleccione *Establecer como grupo de puntos de interrupción predeterminado*. Al establecer un grupo de puntos de interrupción predeterminado, los puntos de interrupción recién creados se agregan automáticamente al grupo.

*Exportar e importar puntos de Interrupción*
Para guardar o compartir el estado y la ubicación de los puntos de interrupción, puede exportarlos o importarlos.
A partir de la versión 17.12 Preview 3 de Visual Studio 2022, los grupos de puntos de interrupción también se incluyen con los puntos de interrupción exportados e importados.
  --Para exportar un solo punto de interrupción a un archivo XML, haga clic con el     botón derecho en el punto de interrupción en el código fuente o en la ventana *Puntos de interrupción* y, luego, seleccione *Exportar* o *Exportar seleccionados*. Seleccione una ubicación de exportación y, a continuación, seleccione *Guardar*. La ubicación predeterminada es la carpeta de la solución.
  --Para exportar varios puntos de interrupción, active las casillas situadas junto a los puntos de interrupción en la ventana *Puntos de interrupción* o especifique los criterios de búsqueda que quiera en el campo *Buscar*. Seleccione el icono *Exportar todos los puntos de interrupción que coinciden con el criterio de búsqueda actual* y guarde el archivo.
  --Para exportar todos los puntos de interrupción, desactive todas las casillas y deje el campo *Buscar* en blanco. Seleccione el icono *Exportar todos los puntos de interrupción que coinciden con el criterio de búsqueda actual* y guarde el archivo.
  --Para importar puntos de interrupción, seleccione el icono *Importar puntos de interrupción de un archivo* en la ventana *Puntos de interrupción*, vaya a la ubicación del archivo XML y seleccione *Abrir*.

*Establecer puntos de interrupción desde ventanas del depurador*
También se pueden establecer puntos de interrupción en las ventanas del depurador *Pila de llamadas* y *Desensamblado*.

*Establecer un punto de interrupción en la ventana Pila de llamadas*:
Para interrumpir la ejecución en la instrucción o línea a la que una función de llamada regresa, se puede establecer un punto de interrupción en la ventana *Pila de llamadas*.
*Para establecer un punto de interrupción en la ventana Pila de llamadas:*

  --Para abrir la ventana *Pila de llamadas*, la depuración debe estar en pausa. Seleccione *Depurar>Ventanas>Pila de llamadas* o presione *Ctrl+Alt+C*.

  --En la ventana *Pila de llamadas*, haga clic con el botón derecho en la función de llamada y seleccione *Punto de interrupción>Insertar punto de interrupción* o presione *F9*.

    Aparecerá un símbolo de punto de interrupción junto al nombre de la llamada de función en el margen izquierdo de la pila de llamadas.

El punto de interrupción de la pila de llamadas aparece en la ventana *Puntos de Interrupción* como una dirección, con una ubicación de memoria que corresponde a la siguiente instrucción ejecutable de la función.

El depurador interrumpe la ejecución en la instrucción.
Para obtener más información sobre la pila de llamadas, vea Cómo usar la ventana pila de llamadas.
Si quiere realizar un seguimiento visual de los puntos de interrupción durante la ejecución del código, vea Asignar métodos en la pila de llamadas durante la depuración.

Establecer un punto de interrupción en la ventana Desensamblado
Para abrir la ventana Desensamblado, la depuración debe estar en pausa. Seleccione Depurar>Windows>Desensamblaro presione Ctrl+Alt+D.

En la ventana Desensamblado, haga clic en el margen izquierdo de la instrucción que quiera interrumpir. También puede seleccionarlo y presionar F9, o bien hacer clic con el botón derecho y seleccionar Punto de interrupción>Insertar punto de interrupción.

`Inspección de variables`
*Inspección de variables y valores devueltos en el depurador de Visual Studio*
Al intentar depurar un problema, a menudo intenta averiguar si las variables almacenan los valores que espera que tengan en un estado de aplicación determinado. Algunas de las características más útiles del depurador son las que permiten inspeccionar variables.
En este artículo se muestra cómo inspeccionar variables y ver los valores devueltos mediante el depurador en Visual Studio. El depurador proporciona varias maneras cómodas de realizar estas tareas, incluidas las siguientes:

  --En el editor de código, puede ver sugerencias de datos y valores devueltos en línea.
  --En ventanas del depurador (Automáticos, Variables locales e Inspección), puede ver los valores de las variables.
  --En los visualizadores, puede ver cadenas grandes o objetos .NET complejos.
Estas características solo están disponibles durante la depuración. Para obtener información sobre cómo iniciar una sesión de depuración, consulte Iniciar la depuración y entrar en modo de interrupción.

*Visualización de variables en el editor de Código*
A menudo, al depurar, necesita una forma rápida de comprobar los valores de propiedad de los objetos en el editor de código y la información sobre datos es una buena forma de hacerlo.
Cuando el depurador está pausado, pase el ratón sobre un objeto y verá su valor o su valor de [propiedad predeterminado.](screenshots/screenshot37.png)
Si la variable tiene propiedades, puede expandir el objeto para ver todas sus propiedades.
Para obtener información detallada sobre el uso de sugerencias de datos, consulte Ver valores de datos en sugerencias de datos.

*Visualizar valores de retorno en línea de llamadas a métodos en el editor de código*
En el código de .NET y C++, puede examinar los valores devueltos al pasar o salir de una llamada de método, lo que puede ser útil cuando el valor devuelto no se almacena en una variable local. Un método se puede usar como parámetro o como valor devuelto de otro método.
A partir de la versión 17.12 de Visual Studio 2022, puede ver los valores devueltos de las llamadas de método en línea y no solo en la [ventana Autos.](screenshots/screenshot38.png)
Con Copilot habilitado, también puede obtener asistencia específica relacionada con el valor de retorno en línea mediante el botón Preguntar a Copilot que aparece en la sugerencia de datos para el [valor de retorno.](screenshots/screenshot39.png)

*Establecimiento de una inspección de variables*
Puede usar una ventana Inspección para especificar una variable (o una expresión) que quiera supervisar.
Durante la depuración, haga clic derecho sobre un objeto en el editor de código y elija Agregar Vigilancia. [Se abre una ventana de inspección.](screenshots/screenshot40.png)

En este ejemplo, se ha establecido una inspección para el objeto y puede ver cómo cambia su valor conforme avanza en el depurador. A diferencia de las otras ventanas de variables, las ventanas *Watch* siempre muestran las variables que estás observando (están atenuadas cuando están fuera del ámbito).
Para obtener más información, vea Establecimiento de una inspección con las ventanas Inspección e Inspección rápida.

*Visualización de valores devueltos de consultas LINQ*
Mientras esté en pausa en el depurador, puede mantener el puntero sobre cláusulas individuales o segmentos de la consulta LINQ para evaluar el valor devuelto de la consulta [inmediata.](screenshots/screenshot41.png)
Si tiene Copilot, puede obtener ayuda de inteligencia artificial mientras mantiene el puntero sobre la consulta LINQ. Seleccione el icono de *GitHub Copilot* al final de la información sobre datos para analizar la consulta con Copilot. A continuación, Copilot explica la sintaxis de la consulta LINQ y aclara por qué obtiene el resultado especificado.

*Obtención de ayuda para la inteligencia artificial*
Si tiene Copilot, puede obtener asistencia de inteligencia artificial mientras examina las variables en el editor de código o en las ventanas de Autos o Locales. Mientras está depurando, haga clic con el botón derecho en una variable y use el botón Preguntar a CopilotCaptura de pantalla del botón *Preguntar a Copilot*. En este escenario, Copilot ya conoce el contexto de su pregunta, por lo que no es necesario proporcionar contexto en el chat. Para obtener más información, consulte Depurar con Copilot.

*Inspección de variables en las ventanas (Automático y Variables locales)*
Las ventanas Automático y Variables locales muestran valores de variables durante la depuración. Las ventanas solo están disponibles durante una sesión de depuración. La ventana Autos muestra las variables utilizadas en torno a la declaración actual donde el depurador está pausado. La ventana Variables locales muestra las variables definidas en el ámbito local, que suele ser la función o el método actuales.

  --Para abrir la ventana *Automático*, seleccione *Depurar>Ventanas>Automático*, o bien presione *Ctrl+Alt+V>A* durante la depuración.

  --La ventana de *Autos* está disponible para los lenguajes de código C#, Visual Basic, C++, y Python, pero no para JavaScript o F#.

  --Para abrir la ventana *Variables locales*, seleccione *Depurar>Ventanas>Variables locales*, o bien presione *Alt+4* durante la depuración.

Las matrices y objetos expandibles aparecen en las ventanas de *Automáticos y Locale*s. Seleccione la flecha situada a la izquierda de un nombre de variable para expandir la vista para mostrar campos y propiedades. Este es un ejemplo de un objeto System.IO.FileStream en la ventana de [*variables locales*:](screenshots/screenshot42.png)
Un valor rojo en la ventana *Locales* o *Automático* significa que el valor ha cambiado desde la última evaluación. El cambio podría provenir de una sesión de depuración anterior, o podría ser porque usted ha cambiado el valor en la ventana.
El formato numérico predeterminado en las ventanas del depurador es decimal. Para cambiarlo a hexadecimal, haga clic con el botón derecho en la ventana *Variables locales* o *Automático*, y seleccione *Presentación hexadecimal*. El cambio afecta a todas las ventanas del depurador.

*Editar valores de variable en la ventana Autos o Variables locales*
Para editar los valores de la mayoría de las variables en las ventanas de Automático o Variables locales, haga doble clic en el valor y escriba el nuevo valor.
Puede escribir una expresión para un valor, por ejemplo, a + b. El depurador acepta la mayoría de las expresiones de lenguaje válidas.
En el código nativo de C++, es posible que tenga que calificar el contexto de un nombre de variable. Para obtener más información, vea Operador de contexto (C++).

*Búsqueda en las ventanas Automático o Variables locales*
Puede buscar palabras clave en las columnas Nombre, Valor y Tipo de la ventana *Autos* o de la ventana *Locals* mediante la barra de búsqueda situada encima de cada ventana. Presione ENTRAR o seleccione una de las flechas para ejecutar una búsqueda. Para cancelar una búsqueda en curso, seleccione el icono "x" en la barra de búsqueda.
Use las flechas izquierda y derecha (Mayús+F3 y F3, respectivamente) para desplazarse por las [coincidencias encontradas.](screenshots/screenshot43.png)
Para que la búsqueda sea más o menos exhaustiva, use la lista desplegable *Búsqueda más profunda* en la parte superior de la ventana *Automóviles* o *Locales* para seleccionar cuántos niveles de profundidad desea buscar en objetos anidados.

*Abrir un visualizador para inspeccionar variables*
Mientras depuras en Visual Studio, puedes ver cadenas grandes o objetos complejos con visualizadores integrados que hacen que los datos sean más fáciles de inspeccionar. Por ejemplo:

  --El visualizador de cadenas muestra cadenas de texto, XML, HTML y JSON que son demasiado largas para una ventana de información o depurador de datos. También puede ayudarle a identificar cadenas malformadas. Para obtener más información, vea Ver cadenas en un visualizador de cadenas.
  --Los visualizadores DataSet e IEnumerable muestran objetos de colección .NET en un visualizador tabular. Para más información, vea Visualizadores tabulares en objetos de Visual Studio.
Los visualizadores aparecen en las ventanas Automático , sugerencias de datos y otras ventanas del depurador.
Para abrir el visualizador, la depuración debe estar en pausa. Mantenga el puntero sobre una variable que tenga un valor de visualizador compatible y seleccione el icono de [lupa VisualizerIcon.](screenshots/screenshot44.png)
Abrir visualizador de cadenas

> **Enfoque práctico**: Concentra tu documentación en las funcionalidades básicas que usarás día a día.

### Flujo de Trabajo con C#

**Creación de proyectos:**

`Paso 1`Abre una terminal en la carpeta donde deseas crear el [proyecto y ejecuta:](screenshots/screenshot45.png)

    dotnet new console -n HolaMundo

  Esto crea una carpeta llamada HolaMundo con una estructura [básica de proyecto C#.](screenshots/screenshot46.png)

`Paso 2`Abrir en Visual Studio Code, En la terminal, navega a la [carpeta del proyecto:](screenshots/screenshot47.png)

cd HolaMundo
code .

**Estructura de proyecto:**
``csharp

La estructura generada por defecto es:

HolaMundo/
├── bin/
├── obj/
├── Program.cs
└── HolaMundo.csproj.

// Incluir aquí un ejemplo del código desarrollado

    using System

  namespace HolaMundo
  {
      class Program
      {
         static void Main(string[] args)
         {
             Console.WriteLine("¡Hola Mundo!");
         }
      }
  }

// Comentarios sobre las decisiones tomadas
Comentarios sobre las decisiones tomadas:

  --Se usa el espacio de nombres HolaMundo para mantener el código organizado.
  --El método Main es el punto de entrada del programa.
  //--Console.WriteLine() imprime texto en la consola.

**Compilación y ejecución:**

`Depurar código con Visual Studio Code`
Visual Studio Code ofrece un amplio soporte para la depuración de diversos tipos de aplicaciones. VS Code incluye soporte integrado para la depuración de JavaScript, TypeScript y Node.js. El Marketplace de Visual Studio ofrece una gran variedad de extensiones de depuración para añadir soporte para otros lenguajes y entornos de ejecución a VS Code.

Este artículo describe las funciones de depuración de VS Code y cómo empezar a depurar en VS Code. También aprenderá a usar Copilot en VS Code para acelerar la configuración de la depuración y el inicio de una sesión de depuración.

`Interfaz de usuario del depurador`
[El siguiente diagrama muestra los componentes principales de la interfaz de usuario del depurador](screenshots/screenshot50.png)
  *1* Vista de ejecución y depuración : muestra toda la información relacionada con la ejecución, la depuración y la gestión de la configuración de depuración.
  *2* Barra de herramientas de depuración : tiene botones para las acciones de depuración más comunes.
  *3* Consola de depuración : permite ver e interactuar con la salida del código que se ejecuta en el depurador.
  *4* Barra lateral de depuración : durante una sesión de depuración, le permite interactuar con la pila de llamadas, los puntos de interrupción, las variables y las variables de observación.
  *5* Menú Ejecutar : contiene los comandos de ejecución y depuración más comunes.

`Antes de comenzar la depuración`
  *1* Instala una extensión de depuración desde Visual Studio Marketplace para tu lenguaje o entorno de ejecución.

VS Code incluye soporte integrado para la depuración de JavaScript, TypeScript y Node.js.

*2* Define una configuración de depuración para tu proyecto.
Para aplicaciones sencillas, VS Code intenta ejecutar y depurar el archivo activo. Para aplicaciones más complejas o escenarios de depuración, es necesario crear un launch.jsonarchivo para especificar la configuración del depurador. Obtenga más información sobre cómo crear una configuración de depuración .

    Consejo
    Copilot en VS Code puede ayudarte a generar el launch.jsonarchivo. Para obtener más información, consulta Usar Copilot para generar configuraciones de depuración .

*3* Establece puntos de interrupción en tu código.
Un punto de interrupción es un marcador que puedes establecer en una línea de código para indicarle al depurador que pause la ejecución cuando llegue a esa línea. Puedes establecer puntos de interrupción haciendo clic en el margen junto al número de línea en el editor.
Para obtener más información sobre los puntos de interrupción, consulte la sección "Trabajar con puntos de interrupción".

`Iniciar una sesión de depuración`
Para iniciar una sesión de depuración en VS Code, siga los siguientes pasos:

`Paso 1` Abre el archivo que contiene el código que deseas depurar.

`Paso 2` Inicie una sesión de depuración con la tecla F5 o seleccione Ejecutar y depurar en la vista Ejecutar y [depurarworkbench.view.debug ( ).](screenshots/screenshot51.png)
Para escenarios de depuración más complejos, como la conexión a un proceso en ejecución, es necesario crear un launch.jsonarchivo para especificar la configuración del depurador. Obtenga más información sobre las configuraciones de depuración .

`Paso 3` Elija el depurador que desea utilizar de la lista de depuradores disponibles.
VS Code intenta ejecutar y depurar el archivo activo. En el caso de Node.js, VS Code busca un startscript en el package.jsonarchivo para determinar el punto de entrada de la aplicación.

`Paso 4` Cuando se inicia una sesión de depuración, se muestra el panel CONSOLA DE DEPURACIÓN y muestra la salida de depuración, y la barra de estado cambia de color [(naranja para los temas de color predeterminados).](screenshots/screenshot52.png)

`Paso 5` El estado de depuración en la barra de estado muestra la configuración de depuración activa. Seleccione el estado de depuración para cambiar la configuración de inicio activa y comenzar a depurar sin necesidad de abrir la vista [Ejecutar y depurar.](screenshots/screenshot53.png)

`Acciones de depuración`
Una vez iniciada la sesión de depuración, la barra de herramientas de depuración aparece en la parte superior de la ventana. Esta barra contiene acciones para controlar el flujo de la sesión, como recorrer el código paso a paso, pausar la [ejecución y detener la sesión.](screenshots/screenshot54.png)

Acción	Descripción
  *Continuar / Pausa*
  F5	-Continuar- : Reanuda la ejecución normal del programa/script (hasta el siguiente punto de interrupción).
      -Pausa- : Inspecciona el código que se ejecuta en la línea actual y depura línea por línea.
  *Paso superior*
  F10	Ejecuta el siguiente método como un solo comando sin inspeccionar ni seguir sus pasos componentes.
  *Entra en*
  F11	Ingrese al siguiente método para seguir su ejecución línea por línea.
  *Salir*
  Shift+F11	Cuando se encuentre dentro de un método o subrutina, regrese al contexto de ejecución anterior completando las líneas restantes del método actual como si se tratara de un solo comando.
  *Reiniciar*
  Ctrl+Shift+F5	Finalice la ejecución actual del programa y vuelva a iniciar la depuración utilizando la configuración de ejecución actual.
  *Detener*
  Shift+F5	Finalizar la ejecución del programa actual.

`Consola de depuración REPL`
Las expresiones se pueden evaluar con la función REPL ( bucle de lectura-evaluación-impresión ) de la consola de depuración . Para abrir la consola de depuración, utilice la acción Consola de depuración en la parte superior del panel de depuración o el comando Ver: Consola de depuración ( Ctrl+Mayús+Y ).
Las expresiones se evalúan después de pulsar Intro y la consola de depuración REPL muestra sugerencias mientras escribe. Si necesita introducir varias líneas, utilice Mayús+Intro entre ellas y, a continuación, envíe todas las líneas para su evaluación con Intro .
La entrada de la consola de depuración utiliza el modo del editor activo, lo que significa que admite el resaltado de sintaxis, la sangría, el cierre automático de comillas y otras [características del lenguaje.](screenshots/screenshot55.png)

``Depuración de múltiples objetivos``
Para escenarios complejos que involucran más de un proceso (por ejemplo, un cliente y un servidor), VS Code admite la depuración de múltiples objetivos. Después de iniciar una primera sesión de depuración, puede iniciar otra. Tan pronto como la segunda sesión esté en funcionamiento, la interfaz de usuario de VS Code cambia al modo de múltiples objetivos .

Las sesiones individuales ahora se muestran como elementos de nivel superior en la vista de [*PILA DE LLAMADAS*.](screenshots/screenshot56.png)
--La barra de herramientas de depuración muestra la sesión actualmente activa [(y todas las demás sesiones están disponibles en un menú desplegable).](screenshots/screenshot57.png)
--Las acciones de depuración (por ejemplo, todas las acciones de la barra de herramientas de depuración) se ejecutan en la sesión activa. La sesión activa se puede cambiar mediante el menú desplegable de la barra de herramientas de depuración o seleccionando un elemento diferente en la vista de la pila de llamadas .

**Debugging:**

``Configuración de depuración de Visual Studio Code``
Para depurar aplicaciones o en escenarios complejos, es necesario crear un launch.jsonarchivo para especificar la configuración del depurador. Por ejemplo, para especificar el punto de entrada de la aplicación, conectarse a una aplicación en ejecución o establecer variables de entorno.
Para obtener más información sobre la depuración en VS Code, consulte Depuración en Visual Studio Code .
    *Consejo*
    Copilot en VS Code te ayuda a crear una configuración de lanzamiento para tu proyecto. Obtén más información sobre cómo generar una configuración de lanzamiento con Copilot.

``Configuraciones de lanzamiento``
Para aplicaciones sencillas o escenarios de depuración, puedes ejecutar y depurar un programa sin configuraciones de depuración específicas. Usa la tecla F5 y VS Code intentará ejecutar el archivo activo.
Sin embargo, en la mayoría de los casos de depuración, es necesario crear una configuración de depuración ( configuración de inicio ). Por ejemplo, para especificar el punto de entrada de la aplicación, conectarse a una aplicación en ejecución o establecer variables de entorno. Crear un archivo de configuración de inicio también resulta útil, ya que permite configurar y guardar los detalles de la configuración de depuración con el proyecto.
VS Code almacena la información de configuración de depuración en un launch.jsonarchivo ubicado en la .vscodecarpeta de su espacio de trabajo (carpeta raíz del proyecto), o en la configuración de usuario o la configuración del espacio de trabajo .

El siguiente fragmento describe una configuración de ejemplo para depurar una aplicación Node.js:
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}\\app.js"
    }
  ]
}

VS Code también admite configuraciones de lanzamiento compuestas para iniciar varias configuraciones al mismo tiempo.
    *Nota*
    Puedes depurar una aplicación simple incluso si no tienes una carpeta abierta en VS Code, pero no es posible gestionar las configuraciones de inicio ni configurar la depuración avanzada.

``Crea un archivo de configuración de depuración``
Para crear un launch.jsonarchivo inicial:

``Paso 1`` Seleccione "Crear un archivo launch.json" en la vista ["Ejecutar y depurar".](screenshots/screenshot58.png)
``Paso 2`` VS Code intenta detectar tu entorno de depuración. Si no puede hacerlo, puedes seleccionarlo [manualmente:](screenshots/screenshot59.png)
En función del entorno de depuración seleccionado, VS Code crea una configuración inicial en el launch.jsonarchivo.
``Paso 3``En la vista Explorador ( Ctrl+Shift+E ), observe que VS Code creó una .vscodecarpeta y agregó el launch.jsonarchivo a su [espacio de trabajo.](screenshots/screenshot60.png)
Ahora puedes editar el launch.jsonarchivo para añadir más configuraciones o modificar las existentes.

``Agrega una configuración a launch.json``
Para agregar una nueva configuración a una existente launch.json, utilice una de las siguientes técnicas:
  --Pulse el botón Agregar configuración y luego seleccione un fragmento para agregar una configuración predefinida.
  --Utilice IntelliSense si su cursor se encuentra dentro de la matriz de configuraciones.
  --Seleccione la opción de menú *Ejecutar > Agregar configuración.*

``Generar una configuración de lanzamiento con IA``
Con Copilot en VS Code, puedes acelerar el proceso de creación de una configuración de lanzamiento para tu proyecto. Para generar una configuración de lanzamiento con Copilot:

``Paso 1``Abra la vista de chat con Ctrl+Alt+I o seleccione Abrir chat en el menú Copilot de la barra de título.

``Paso 2``Introduce el /startDebuggingcomando de chat para generar una configuración de depuración.
Como alternativa, también puede ingresar un mensaje personalizado, como generar una configuración de depuración para una aplicación Express #codebase .
Esto puede resultar útil si tu espacio de trabajo contiene archivos en diferentes idiomas.

      *Nota*
      La #codebasevariable de chat proporciona a Copilot el contexto de tu proyecto, lo que le ayuda a generar una respuesta más precisa.

``Paso 3``Aplique la configuración sugerida y luego comience a depurar.

``Inicie una sesión de depuración con una configuración de lanzamiento.``
Para iniciar una sesión de depuración con una configuración de lanzamiento:

``Paso 1`` Seleccione la configuración denominada "Lanzar programa" utilizando el menú desplegable "Configuración" en la vista "Ejecutar y depurar" .

La lista de configuraciones disponibles coincide con la del [launch.jsonarchivo](screenshots/screenshot61.png)
``Paso 2`` Inicie su sesión de depuración con F5 o seleccione Iniciar depuración (icono de reproducción) en la vista *Ejecutar y depurar.*
Como alternativa, puede ejecutar su configuración a través de la paleta de comandos ( Ctrl+Shift+P ) filtrando por *Depurar: Seleccionar e iniciar depuración* o escribiendo 'debug 'y seleccionando la configuración que desea depurar.

## Visual Studio - IDE Alternativo

### Instalación

**Proceso de instalación:**
  **Descarga:** 
`Paso 1` [Ir a la pagina *https://visualstudio.microsoft.com/es/downloads/?cid=learn-onpage-download-install-visual-studio-page-cta*,](screenshots/screenshot62.png).
`Paso 2` Decida qué versión y edición de Visual Studio se va a instalar. Las opciones más comunes son:
  La versión más reciente de Visual Studio 2022 hospedada en servidores de Microsoft. Para instalar esta versión, seleccione el botón siguiente y elija la edición que desee. El instalador descarga un pequeño cargador de arranque en su [carpeta Descargas.](screenshots/screenshot63.png)

  **Opciones del instalador:** 
 ``Paso 3``En la carpeta Descargas, haga doble clic en el programa de instalación denominado VisualStudioSetup.exe, o denominado algo como vs_community.exe, para iniciar la instalación.

Si ve un aviso de Control de cuentas de usuario, seleccione *Sí*. El cuadro de diálogo le pide que confirme los términos de licencia de Microsoft y la Declaración de privacidad de Microsoft . Seleccione [*Continuar.*](screenshots/screenshot64.png)
Se abre el Instalador de Visual Studio. También puede instalar cualquier producto que aparezca en la pestaña Disponible del instalador de Visual Studio.

``Paso 4``Elegir cargas de trabajo
Después de instalar el Instalador de Visual Studio, puede usarlo para personalizar la instalación seleccionando los conjuntos de características o cargas de trabajo, que desee. Así es como.

Seleccione la carga de trabajo que desee en el [instalador de Visual Studio.](screenshots/screenshot65.png)
Revise los resúmenes de carga de trabajo para decidir qué carga de trabajo admite las características que necesita. Por ejemplo, elija la carga de trabajo de ASP.NET y desarrollo web para editar páginas web de ASP.NET con Vista Previa en Vivo o crear aplicaciones web responsivas con Blazor. Puede elegir entre las cargas de trabajo de escritorio, & móvil, o para desarrollar aplicaciones multiplataforma con C#, o proyectos de C++ que tienen como destino C++20.
Después de elegir las cargas de trabajo que desee, seleccione Instalar.
A continuación, aparece una pantalla de estado que muestra el progreso de la instalación de Visual Studio.

- **Componentes necesarios:** [Componentes específicos para C#]
- 
``Paso 5`` Elegir componentes individuales (opcional)
Si no desea usar la característica Cargas de trabajo para personalizar la instalación de Visual Studio o si desea agregar más componentes que las instalaciones de una carga de trabajo, puede instalar o agregar componentes individuales desde la pestaña Componentes individuales. Elija lo que desee y, [a continuación, siga las indicaciones.](screenshots/screenshot66.png)
Carga de trabajo principal Desarrollo de escritorio con .NET
(Incluye C#, .NET Framework, .NET 6/7/8, y Windows Forms/WPF)
*Componentes opcionales recomendados*

ASP.NET y desarrollo web (si planeas crear aplicaciones web)

Desarrollo multiplataforma con .NET MAUI (si quieres apps móviles y de escritorio)
Desarrollo de Azure (si usarás servicios en la nube de Microsoft)
Herramientas de administración de datos (para trabajar con bases de datos SQL)
    *Consejo:* puedes personalizar los componentes antes de instalar; el instalador mostrará el espacio requerido.

``Paso 6`` Instalar paquetes de idioma (opcional)
De forma predeterminada, el programa de instalador intenta coincidir con el idioma del sistema operativo cuando se ejecuta por primera vez. Para instalar Visual Studio en un idioma que elija, vaya a la pestaña Paquetes de idioma del Instalador de Visual Studio y [siga las indicaciones.](screenshots/screenshot667.png)
Cambiar el idioma del instalador en un símbolo del sistema
También puede cambiar el idioma predeterminado ejecutando el instalador desde un símbolo del sistema. Por ejemplo, puede forzar que el instalador se ejecute en inglés mediante el siguiente comando:
Símbolo del sistema de Windows

vs_installer.exe --locale en-US

El instalador conserva esta configuración al volver a ejecutarla. El instalador admite estas configuraciones regionales del *idioma*:*zh-cn, zh-tw, cs-cz, en-us, es-es, fr-fr, de-de, it-it, ja-jp, ko-kr, pl-pl, pt-br, ru-ruy tr-tr.*

``Paso 7`` Seleccionar la ubicación de instalación (opcional)
Puede reducir la superficie de memoria de instalación de Visual Studio en la unidad del sistema. Para obtener más información, consulte [Selección de las ubicaciones de instalación.](screenshots/screenshot68.png)
    *Importante*
    Puede seleccionar otra unidad para Visual Studio IDE o para la caché de descargas solo al instalar Visual Studio por primera vez. Si ya la instaló y quiere cambiar las unidades, debe desinstalar Visual Studio y volver a instalarla.
    Si ya ha instalado previamente Visual Studio en el equipo, no podrá cambiar la ruta de acceso de los componentes, las herramientas y los SDK compartidos. Parece atenuado. Todas las instalaciones de Visual Studio comparten esta ubicación.

``Paso 8`` Iniciar sesión en su cuenta (opcional)
Aunque no tiene que iniciar sesión, hay muchas ventajas para hacerlo.
Puede evaluar una evaluación gratuita de Visual Studio Professional o Visual Studio Enterprise durante 30 días. Si inicia sesión, puede ampliar el período de prueba a 90 días. La extensión de prueba de 90 días solo funciona una vez. Para seguir usando Visual Studio después de que finalice un período de prueba, desbloquee con una suscripción en línea de o una clave de producto de .
Visual Studio Community no requiere que inicie sesión. Sin embargo, si la instalación le pide que inicie sesión periódicamente, inicie sesión para seguir usando Visual Studio Community sin interrupciones.

``Paso 9`` Empezar a desarrollar
Una vez completada la instalación, puede empezar a desarrollar con Visual Studio.

  --Seleccione el botón Iniciar.

  --En la ventana de inicio, seleccione Crear un nuevo proyecto.

  --En el cuadro de búsqueda de plantillas, escriba el tipo de aplicación que desea crear para ver una lista de plantillas disponibles. La lista de plantillas depende de las cargas de trabajo que haya elegido durante la instalación. Para ver diferentes plantillas, elija diferentes cargas de trabajo. También puede filtrar la búsqueda de un lenguaje de programación específico mediante la lista desplegable *Todos los lenguajes*. También puede filtrar mediante la lista *Todas las plataformas* y la lista *Todos los tipos de proyecto*.

  --Seleccione Siguiente. Proporcione información en los cuadros de diálogo siguientes y, a continuación, seleccione Crear.
Visual Studio abre el nuevo proyecto y está listo para codificar.

- **Verificación:** [Cómo confirmar instalación correcta]

Para confirmar que Visual Studio está correctamente instalado y listo para C#:
 Desde Visual Studio
*Metodo 1*
``PASO 1``Abre Visual Studio.
``PASO 2``Selecciona Crear un nuevo proyecto.
``PASO 3``Busca “Aplicación de consola C#” o “Windows Forms App (.NET)”.
``PASO 4``Crea el proyecto y espera que cargue el entorno.
``PASO 5``En la ventana del editor, escribe:
        Console.WriteLine("¡Visual Studio y C# listos para usar!");
``PASO 6``presiona F5 o el botón Iniciar para ejecutar el programa.
*Metodo 2*
``Paso 1``Desde el instalador
``PASO 2``Abre el Instalador de Visual Studio.
``PASO 3``En la pestaña Instalados, verifica que la edición esté [instalada y actualizada.](screenshots/screenshot69.png)

### Desarrollo con C#

**Creación de proyecto:**

Creación de un proyecto
Para empezar, cree un proyecto de aplicación de C#. El tipo de proyecto incluye todos los archivos de plantilla que necesita.

``Paso 1`` Abra Visual Studio y seleccione [Crear un nuevo proyecto en la ventana de inicio.](screenshots/screenshot70.png)

``Paso 2`` En la ventana Crear un nuevo proyecto, seleccione C# de la lista desplegable de lenguajes. Elija Windows en la lista de plataformas y Console en la lista de tipos de proyecto.
Después de aplicar los filtros de idioma, plataforma y tipo de proyecto, seleccione la plantilla aplicación de consola y, a continuación, seleccione Siguiente.
    NOTA
    Si no ve la plantilla Aplicación de consola, seleccione Instalar más herramientas y [características.](screenshots/screenshot71.png)
    En Instalador Visual Studio, seleccione la carga de trabajo Desarrollo de escritorio de [.NET.](screenshots/screenshot72.png)
    Seleccione Modificar en el Instalador de Visual Studio. Es posible que se le pida que guarde su trabajo. Seleccione Continuar para instalar la carga de trabajo.
Vuelva al paso 2 del procedimiento Crear un proyecto.

``Paso 3`` En la ventana Configurar el nuevo proyecto, escriba Calculator en el cuadro Nombre del proyecto y, a continuación, [seleccione Siguiente.](screenshots/screenshot73.png)

``Paso 4`` En la ventana Información adicional seleccione .NET 8.0 para el campo Plataforma de destino. A continuación, [seleccione Crear.](screenshots/screenshot74.png)

Visual Studio abre el nuevo proyecto, que incluye el código predeterminado Hello World. Para verlo en el editor, seleccione el archivo de código Program.cs en la ventana Explorador de soluciones, que normalmente se encuentra en el lado derecho de Visual Studio.
La instrucción de código único llama al método WriteLine para mostrar la cadena literal Hello, World! en la ventana de la consola. Si presiona F5, puede ejecutar el programa predeterminado en modo de depuración. Una vez que la aplicación se ejecuta en el depurador, la ventana de la consola permanece abierta. Presione cualquier tecla para cerrar la ventana de la consola.

**Flujo de trabajo básico:**
  ``Compilación y ejecución``
  *Compilación*
  Visual Studio compila automáticamente el código antes de ejecutar, pero también puedes hacerlo manualmente:

     Menú superior → Compilar > Compilar solución (o presiona Ctrl + Shift + B).

  Esto generará los archivos ejecutables en la carpeta:

    /bin/Debug/net8.0/

-*Ejecución*
  Asegúrate de que el archivo principal (por ejemplo, Program.cs) tenga un método Main.
  Haz clic en el botón Iniciar(o presiona F5) para ejecutar el programa.
  En una aplicación de consola, aparecerá una ventana con el resultado.

  ``Uso de Solution Explorer``
  El Solution Explorer (Explorador de soluciones) es el panel de Visual Studio que te permite visualizar, organizar y gestionar todos los archivos y elementos que forman parte de tu solución (solution) y sus proyectos (projects).
  Lo encontrarás normalmente en el lado derecho del entorno de Visual Studio.
  Si no está visible, puedes activarlo desde:

      Menú → Ver → Explorador de soluciones
      o con el atajo Ctrl + Alt + L.

  ``Debugging básico``
El depurador (Debugger) de Visual Studio permite analizar el comportamiento del programa paso a paso, detectar errores y examinar variables en tiempo real.

Principales herramientas:
Herramienta	Descripción	Atajo
🔴 Punto de interrupción (Breakpoint)	Detiene la ejecución en una línea específica.	F9
▶️ Iniciar depuración	Ejecuta el programa en modo debug.	F5
⏩ Paso a paso (Step Over)	Ejecuta la siguiente línea sin entrar a funciones.	F10
⏬ Paso dentro (Step Into)	Entra dentro de una función o método.	F11
⏹️ Detener depuración	Finaliza la sesión de depuración.	Shift + F5
Uso práctico:
``Paso 1`` Haz clic en el margen izquierdo del editor para colocar un breakpoint (un círculo rojo).

``Paso 2``Ejecuta el programa en modo depuración (F5).

``Paso 3``Cuando el programa llegue al breakpoint, se detendrá.

``Paso 4``En la parte inferior y lateral podrás usar:

  Ventana de Variables locales: muestra el valor de las variables actuales.

  Ventana Inspección (Watch): permite agregar variables para monitorearlas.

  Ventana Pila de llamadas (Call Stack): muestra el orden de ejecución.

``Paso 5``Usa F10 o F11 para avanzar línea por línea y observar los cambios en las variables.
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
