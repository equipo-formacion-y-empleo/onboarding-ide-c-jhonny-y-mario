# Guía de Evaluación - Requisitos y Errores Comunes

## ⚠️ REQUISITO

**IDE_ONBOARDING_GUIDE.md debe tener:**
- Entre 2,000 y 5,000 **Palabras:**
- Al menos 25 **Imágenes:**   (usa la sintaxis `![alt text][image-ref]`))

**CONCLUSIONES_EVALUACION.md debe tener:**
- Entre 750 y 1,500 **Palabras:**

---

## ❌ ERRORES COMUNES A EVITAR

1. **Narración en primera persona:** "Nosotros instalamos...", "habrá que hacer..." → Usa segunda persona (tú) o impersonal si conviene: "Abre VS Code", "Se debe hacer clic en...".
2. **Uso de comandos de consola en vez de capacidades del IDE:** Ejemplo: `dotnet build` en terminal en lugar de F5 (Run) o Ctrl+Shift+B (Build). Prioriza acciones desde el IDE.
3. **Falta de evidencia visual y descripción insuficiente:** Cada paso relevante debe estar probado con imágenes y ser descriptivo en cuanto a dónde hacer clic, qué escribir o seleccionar.
4. **Texto guía o plantilla sin eliminar:** No debe quedar ningún texto que indique cómo rellenar el archivo, como `[Nombre]`, `[Fecha]`, `TODO`, `COMPLETAR`, ni instrucciones de la plantilla.
5. **Flujo de trabajo en otros lenguajes sin prueba de ejecución:** Documentar solo instalación de Python/Java sin mostrar crear archivo, ejecutar y capturar salida desde el IDE. Demuestra el flujo completo create→run→output.
6. **Imágenes no validadas en GitHub:** Las rutas de imágenes deben ser relativas (`![alt text](screenshots/nombre.png)`), no absolutas. Valida que todas las imágenes carguen en el previsualizador Markdown del IDE y también en GitHub tras hacer push.
