⚠ **ADVERTENCIA**

El objetivo de este template no es construir una solución productiva completa. Es diseñar, experimentar y obtener evidencia suficiente para hacer una recomendación profesional fundamentada. Una demo convincente no equivale a una solución viable: la diferencia está en haber probado los límites, involucrado a usuarios reales y analizado los riesgos.

Diseño y validación de la solución de IA Generativa - [NOMBRE EMPRESA]

# HIPÓTESIS DE LA EXPERIMENTACIÓN

Retome la hipótesis formulada en T-09 y refínela para guiar el trabajo de este sprint.

💡 **SUGERENCIA**

Una buena hipótesis es verificable: define quién hace qué, con qué resultado, y establece un criterio observable que permita saber si funcionó o no. Pueden tener más de una hipótesis si necesitan validar cosas distintas. Por ejemplo:

* **Hipótesis de valor:** ¿la solución resuelve el problema que identificaron?
* **Hipótesis funcional:** ¿produce el resultado esperado en los casos normales?
* **Hipótesis de riesgo:** ¿puede fallar de formas inaceptables para la organización?

Formule la hipótesis o hipótesis que guiarán la experimentación:

Creemos que [capacidad o solución] permitirá a [usuario] realizar [tarea], logrando [resultado esperado].  
Consideraremos validada la hipótesis cuando [criterio observable].

Indique también qué incertidumbres clave busca resolver esta experimentación:

# DISEÑO FUNCIONAL

Describa cómo funcionaría la solución desde la perspectiva del usuario. No es necesario explicar la tecnología en detalle: explique la experiencia.

💡 **SUGERENCIA**

Recorra el flujo completo prestando atención a cada paso:

1. ¿Quién inicia la interacción y en qué contexto?
2. ¿Qué información aporta el usuario?
3. ¿Qué hace la solución con esa información?
4. ¿Qué respuesta o acción produce?
5. ¿Quién valida el resultado antes de que tenga consecuencias?
6. ¿Qué ocurre después?
7. ¿Cuándo debe la solución detenerse y derivar a una persona?

Incluya al menos un flujo normal y un caso de excepción o error.

# COMPORTAMIENTO ESPERADO

Defina con precisión qué puede y qué no puede hacer la solución. Esta especificación es la base del diseño y de las pruebas.

💡 **SUGERENCIA**

Para un profesional LSI, definir lo que una solución *no debe hacer* es tan importante como definir lo que sí hace. Una solución de IA sin límites claros no puede gobernarse. Esta tabla es el equivalente a las restricciones de un RFP: establece el contrato de comportamiento antes de construir nada.

|  | Definición |
| --- | --- |
| **Puede hacer** |  |
| **No puede hacer** |  |
| **Información que puede consultar** |  |
| **Información que no debe utilizar** |  |
| **Decisiones que puede recomendar** |  |
| **Decisiones que no puede tomar por sí sola** |  |
| **Cuándo debe escalar a una persona** |  |
| **Cuándo debe indicar que no sabe o no puede responder** |  |

# DISEÑO DE LA SOLUCIÓN

## Patrón de solución

Identifique qué tipo de solución de IA Generativa corresponde a este caso y justifique la elección.

💡 **SUGERENCIA**

Algunos patrones frecuentes:

* **Prompt estructurado:** se envía una instrucción al modelo con contexto fijo y se obtiene una respuesta generada
* **Asistente con conocimiento organizacional (RAG):** el modelo responde basándose en documentos o bases de conocimiento de la organización
* **Copiloto integrado:** la IA asiste dentro de una aplicación existente (redactar, revisar, sugerir)
* **Generación de documentos:** produce borradores, resúmenes o reportes a partir de datos o plantillas
* **Extracción y clasificación:** interpreta texto no estructurado y lo convierte en información utilizable
* **Agente con herramientas:** la IA puede consultar sistemas externos o disparar acciones

No asuma que todos los casos requieren el patrón más complejo. Elija el más simple que resuelva el problema.

Patrón seleccionado y justificación:

## Arquitectura conceptual

Presente un diagrama que muestre los componentes principales de la solución y cómo se relacionan: usuarios, canales, modelo de IA, fuentes de información, sistemas de la organización, controles e intervención humana.

💡 **SUGERENCIA**

No hace falta que sea un diagrama técnico detallado. Debe ser comprensible para alguien del negocio. Relacione esta arquitectura con la Arquitectura Empresarial Actual (T-02) y con la solución tecnológica ya recomendada (T-07): ¿cómo convive o se integra con lo que ya existe?

## Herramientas y modelos

Documente qué herramientas y modelos utilizó o utilizaría la solución.

💡 **SUGERENCIA**

La elección no puede basarse únicamente en lo que el equipo ya conocía o en popularidad. Justifiquen por qué esta herramienta es adecuada para el caso e indiquen al menos una alternativa que evaluaron.

| Componente | Herramienta / Modelo | Motivo de la elección | Licencia | Privacidad de datos | Costo estimado |
| --- | --- | --- | --- | --- | --- |
| Modelo generativo |  |  |  |  |  |
| Plataforma o entorno |  |  |  |  |  |
| Fuente de conocimiento |  |  |  |  |  |
| Integración con otros sistemas |  |  |  |  |  |

## Instrucciones y prompts

Si la solución utiliza instrucciones configurables para el modelo, documente el diseño de las principales.

💡 **SUGERENCIA**

Incluya al menos: el rol asignado al modelo, el contexto que recibe, el objetivo de la interacción, las restricciones de respuesta y el formato esperado de salida. No es necesario revelar credenciales ni datos confidenciales de la organización.

# INFORMACIÓN Y FUENTES DE CONOCIMIENTO

Detalle qué información utiliza la solución, cómo se obtiene y qué cuidados requiere.

| Fuente | Propietario | Formato | ¿Se envía al modelo externo? | Sensibilidad | Estado |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

Describa brevemente cómo se mantiene actualizada esta información y quién sería responsable de su gestión en la operación normal:

# PROTOTIPO O PRUEBA DE CONCEPTO

Describa qué construyó el equipo y cómo puede accederse o verificarse.

💡 **SUGERENCIA**

Un prototipo válido para este trabajo no necesita estar listo para producción, pero sí debe ser funcional. Las herramientas disponibles hoy permiten construir algo real en el tiempo de un sprint. Algunas opciones concretas:

* Configurar un asistente o agente personalizado con instrucciones específicas para el caso (Claude Projects, ChatGPT Custom GPTs, Gemini Gems)
* Armar un flujo de automatización conectando una fuente de información con un modelo de IA (n8n, Make, Zapier)
* Integrar capacidades de IA en una herramienta que la organización ya usa (Notion AI, Copilot, Google Workspace AI)
* Construir un prototipo de interfaz funcional conectado a una API de un modelo

Si los datos reales son sensibles, trabaje con datos sintéticos o anonimizados que representen fielmente la estructura del caso. Lo que importa es que el flujo sea real y que pueda probarse con usuarios.

| Elemento | Descripción |
| --- | --- |
| ¿Qué se construyó? |  |
| ¿Dónde puede verse o accederse? |  |
| ¿Qué partes son funcionales y cuáles fueron simuladas? |  |
| ¿Qué iteraciones realizó el equipo durante la construcción? |  |

# PLAN DE PRUEBAS Y RESULTADOS

## Casos de prueba

Defina los casos de prueba antes de ejecutarlos. Registre los resultados en la misma tabla.

⚠ **ADVERTENCIA**

Probar únicamente los casos en que la solución funciona bien no es una validación profesional. Una solución confiable debe haber sido probada también ante entradas ambiguas, información incorrecta o incompleta, preguntas fuera de alcance e intentos de obtener respuestas que no debería dar. Si el equipo no encontró ningún caso en el que la solución falle, probablemente no probó suficiente.

| ID | Tipo de caso | Entrada o situación | Resultado esperado | Resultado obtenido | ¿Aprobó? |
| --- | --- | --- | --- | --- | --- |
|  | Caso normal |  |  |  |  |
|  | Información incompleta |  |  |  |  |
|  | Pregunta fuera del alcance |  |  |  |  |
|  | Solicitud de datos sensibles |  |  |  |  |
|  | Caso crítico o de alto impacto |  |  |  |  |

## Síntesis de la experimentación

Describa en prosa qué aprendió el equipo: qué funcionó, qué no funcionó, qué ajustes realizaron durante el proceso y qué incertidumbres permanecen sin resolver.

# VALIDACIÓN CON USUARIOS

Describa si el equipo pudo probar la solución con algún referente o usuario de la organización.

💡 **SUGERENCIA**

La validación con usuarios no requiere una sesión formal. Puede ser una demo de 20 minutos con el sponsor o con alguien que trabaje en el proceso afectado. Lo importante es registrar qué se mostró, qué reaccionaron y si lo consideraron útil y confiable. Una recomendación basada exclusivamente en la evaluación del propio equipo tiene mucho menos peso que una que incluye al menos una validación externa.

| Elemento | Descripción |
| --- | --- |
| ¿Con quién se validó? |  |
| ¿Qué se mostró o probó? |  |
| ¿Qué feedback recibió el equipo? |  |
| ¿Qué cambios surgieron de esa conversación? |  |
| ¿Qué nivel de confianza expresaron en la solución? |  |

# RESPONSABILIDAD Y GOBIERNO

## Supervisión humana

Defina concretamente cómo interviene una persona en el funcionamiento de esta solución.

💡 **SUGERENCIA**

La supervisión humana no es un detalle de implementación: es una condición para que una solución de IA pueda recomendarse responsablemente. No alcanza con escribir "habrá revisión humana". Debe quedar claro quién interviene, cuándo y ante qué situaciones. Una solución en la que nadie sabe quién es responsable cuando algo falla no tiene gobernanza.

| Etapa del proceso | Actividad de la IA | Intervención humana requerida | Responsable |
| --- | --- | --- | --- |
|  |  |  |  |

## Seguridad, privacidad y ética

Describa los controles necesarios para operar esta solución de forma responsable e identifique cualquier riesgo que no haya podido mitigarse en el alcance de este trabajo.

💡 **SUGERENCIA**

Algunos aspectos que suelen requerir atención: protección de datos personales, control de acceso, registro de interacciones para auditoría, manejo de sesgos en las respuestas, transparencia con los usuarios (¿saben que interactúan con una IA?), propiedad intelectual del contenido generado, y qué ocurre si el modelo da una respuesta incorrecta con consecuencias para la organización o sus clientes.

# RECOMENDACIÓN FINAL

Con base en todo lo trabajado, el equipo debe tomar una posición profesional sobre esta solución.

💡 **SUGERENCIA**

Una recomendación fundamentada puede concluir que la solución es viable e implementable, que requiere un piloto más amplio antes de decidir, que el caso de uso debe reformularse, que hay dependencias previas que resolver, o que no es el momento adecuado. Cualquiera de estas conclusiones es válida si está respaldada por la evidencia. Lo que no es válido es recomendar implementar basándose en el entusiasmo, ni descartar basándose en el miedo a la tecnología.

Seleccione la recomendación del equipo:

* ☐ Implementar
* ☐ Realizar un piloto más amplio antes de decidir
* ☐ Reformular el caso de uso
* ☐ Resolver dependencias previas antes de avanzar
* ☐ Postergar
* ☐ Descartar

**Justificación** (basada en la evidencia de este trabajo):

**Próximos pasos recomendados para la organización:**
