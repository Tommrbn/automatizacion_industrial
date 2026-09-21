# Portabilidad del diagnóstico del parcial 1

## Objetivo y alcance autorizado

Conservar el avance del diagnóstico de las unidades 1 y 2 y permitir continuarlo en otra computadora sin reiniciarlo.
El usuario autorizó preparar y subir el registro a `Tommrbn/automatizacion_industrial`, usando su sesión local de GitHub y cambiando previamente el repositorio a privado.
No se subirán ni modificarán los 27 PDF ni el archivo PPTX originales. No se publicarán credenciales ni registros internos de herramientas.

## Plan de trabajo

- [ ] T1: Crear y verificar un registro portable, instrucciones de reanudación y exclusión de materiales originales; registrar la unidad de trabajo con un commit convencional.

Ruta T1: delegada directa. Motivo: redacción no mecánica de documentos relacionados y lectura preparatoria. El padre conserva la verificación remota, Git y la entrega.
Archivos previstos: `README.md`, `AVANCE_PROBE.md` y `.gitignore`.
Estimación: 250–350 líneas redactadas, incluido este seguimiento. Estrategia: `ask-on-risk`; no se prevé crear PR.
Rama local prevista: `docs/probe-portability`. El repositorio remoto está vacío; se publicará su primera rama `main` sin sobrescribir historial.

## Criterios de aceptación y comprobaciones

- Registro fiel de respuestas, correcciones y temas no evaluados; una respuesta posterior a la explicación no demuestra dominio independiente.
- Pregunta pendiente exacta: «¿El cambio de 001 a 011 cumple la regla de Gray? Explica qué posición cambia».
- Diagnóstico pausado, no terminado; la propuesta de diez preguntas adicionales no fue aceptada.
- Instrucciones para continuar desde otra computadora y advertencia de que los materiales originales no viajan en este respaldo.
- Lectura estructural de documentos; comprobación de enlaces locales, ausencia de secretos y rutas personales, `git diff --cached --check`, lista explícita de archivos y comparación SHA-256 de los 28 originales.
- Tras la subida: comprobar privacidad, SHA remoto y archivos realmente publicados.

## Configuración de comprobaciones

TDD: no aplicable; solo documentación de estudio y exclusiones de Git, sin software ni ejecutable de pruebas en la carpeta original.
Prueba funcional: lectura del punto de reanudación y comprobaciones de Git indicadas arriba.
Runtime: no aplicable; no hay aplicación que ejecutar. No se ha evaluado el uso práctico de CADeSIMU.
Reversión: retirar únicamente los nuevos documentos y exclusiones; no tocar materiales originales.
RDD: desactivado por defecto, comprobado con `gentle-ai review mode status`; no se activó.
La evaluación nativa clasificó el cambio como `medium` por `.gitignore`, con `review_due=false` y `under_budget` (303 líneas iniciales). Se aplicaron comprobaciones del redactor y lectura estructural independiente del padre; no se ejecutó revisión RDD.

## Evidencia y estado

- Cuenta verificada: Tommrbn.
- Cambio de visibilidad autorizado y comprobado: `isPrivate=true`, `isEmpty=true`.
- Se calcularon hashes SHA-256 de los 28 materiales antes de cualquier modificación local.
- Redacción delegada completada y leída por el padre: `README.md`, `AVANCE_PROBE.md` y `.gitignore`.
- `git diff --cached --check`: correcto. Lista preparada: solo los tres archivos anteriores y este seguimiento.
- `git check-ignore` con nombres explícitos: 28/28 originales excluidos; los documentos del respaldo no están ignorados.
- Comparación SHA-256 posterior: los 28 originales conservan exactamente su contenido.
- UTF-8, enlace README al registro y ausencia de espacios finales: comprobados por el redactor; el padre repitió la lectura y la comprobación de exclusiones.
- Espejo Engram pendiente: el servicio rechaza el proyecto con `unknown_project`; no existe un identificador de sesión autorizado disponible.
- Commit y entrega: pendientes.

## Próximo paso

Registrar la unidad de trabajo y comprobar su publicación privada con la lista exacta de archivos.
