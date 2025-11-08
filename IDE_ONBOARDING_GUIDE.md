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
```csharp

La estructura generada por defecto es:

/HolaMundo/
/├── bin/
/├── obj/
/├── Program.cs
/└── HolaMundo.csproj.

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
