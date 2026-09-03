# .UBA ECONÓMICAS
### Actuación Profesional del Lic. en Sistemas de Información de las Organizaciones

# Arquitectura Empresarial

---

## Qué vamos a ver hoy

1. Por qué hablamos de arquitectura
2. Arquitectura Empresarial y sus dominios
3. Arquitectura actual y arquitectura objetivo
4. Marcos de referencia y el rol del arquitecto

---

## Por qué hablamos de arquitectura

### Comparación: Mansión Winchester vs. Burj Khalifa

| | Mansión Winchester (California, EEUU) | Burj Khalifa (Dubai, EAU) |
|---|---|---|
| Años de construcción | 38 años | 6 años |
| Constructoras | 147 | 3 |
| Arquitectos | Ningún arquitecto | 1 estudio de arquitectura e ingeniería |
| Tamaño | 160 habitaciones, 40 dormitorios | 193 pisos habitables, 828 metros |
| Otros elementos | 950 puertas | 57 ascensores |

**Datos curiosos de la Mansión Winchester** (construida sin planos ni arquitecto):
- 65 puertas y 13 escaleras que no llegan a ningún lado
- 24 tragaluces en el piso
- No existen planos

> La falta de una arquitectura planificada genera resultados incoherentes, ineficientes y difíciles de mantener — a pesar de la inversión de tiempo y recursos.

### ¿Qué buscamos?

**¡Construir los planos!** — antes de construir, se necesita un diseño (existente, ampliación y remodelación).

Para que una casa funcione bien, se debe pensar en:
- Diseño de interiores
- Electricidad
- Plomería
- Estructuras
- etc.

*La misma lógica aplica a las organizaciones: sin una arquitectura definida, los sistemas y procesos crecen de forma desordenada.*

---

## Arquitectura Empresarial y sus dominios

### Dominios de la Arquitectura Empresarial

```
                    ARQUITECTURA EMPRESARIAL
   ┌───────────────┬───────────────┬───────────────┬───────────────┐
   │ Arquitectura  │ Arquitectura  │ Arquitectura  │ Arquitectura  │
   │  de NEGOCIOS  │de APLICACIONES│   de DATOS    │  TECNOLÓGICA  │
   └───────────────┴───────────────┴───────────────┴───────────────┘
                    Oportunidades y Soluciones
                    Portafolio de programas
                    Proyectos
```

### Qué es la Arquitectura Empresarial

- Es una disciplina que **describe de manera integrada** cómo la organización cumple su estrategia y visión.
- Es un **puente entre la estrategia y los proyectos**, y una herramienta de decisión para la dirección.
- **No es** un diagrama de red ni el diseño interno de un sistema.
- **No es** un asunto exclusivo del área de sistemas ni un documento creado para archivar y no tocar más.

### Fundamentos de la Arquitectura Empresarial

- Informar a la dirección en lenguaje accesible cuál es la infraestructura actual y el modelo de infraestructura deseado.
- Brindar una visión integrada y única para los tomadores de decisiones.
- Disponer de instrumentos metodológicos que unifiquen criterios, vocabularios y formas de describir una situación presente y/o futura.
- Medir la relación de inversión en TI con respecto a los resultados esperados del negocio, impactados con dicha inversión.

---

## Arquitectura actual y arquitectura objetivo

### Arquitectura Empresarial Actual

| Dominio | Pregunta clave |
|---|---|
| Arquitectura de Negocios | ¿Cómo se refleja la estrategia en los procesos del negocio? |
| Arquitectura de Aplicaciones | ¿Cuáles son los sistemas, apps e interfaces que soportan al negocio? |
| Arquitectura de Datos | ¿Cuál es la información necesaria para que opere el negocio? |
| Arquitectura Tecnológica | ¿En qué plataforma tecnológica se apoyan las necesidades del negocio? |

### Arquitectura Empresarial Futura

*Destino / To-Be — Visión + Objetivos Estratégicos*

| Dominio | Pregunta clave |
|---|---|
| Arquitectura de Negocios | ¿Cómo deberían ser sus procesos? |
| Arquitectura de Aplicaciones | ¿Qué sistemas, apps e interfaces soportarán al negocio? |
| Arquitectura de Datos | ¿Cuál será la información necesaria para que opere el negocio? |
| Arquitectura Tecnológica | ¿En qué plataforma tecnológica se apoyarán las necesidades del negocio? |

### Mapa de procesos ISO 9001

**Procesos Estratégicos:**
- Dirección y Planificación Estratégica
- Gestión del Sistema de Calidad
- Revisión de Dirección

**Procesos Operativos:**
Marketing y Ventas → Diseño y Desarrollo → Compras → Producción → Entrega y Posventa

**Procesos de Apoyo:**
- Recursos Humanos
- Infraestructura y TI
- Gestión Documental
- Mejora Continua

*Flujo: Requisitos del cliente → Procesos → Satisfacción del cliente*

Este mapa de procesos se puede vincular directamente con el modelo de Arquitectura Empresarial (Negocios, Aplicaciones, Datos, Tecnología).

### Diagrama resumen de Arquitectura Empresarial (ejemplo)

**Arquitectura empresarial actual** — ejemplo de una empresa con ERP central:

| Capa | Contenido |
|---|---|
| Procesos | Gestión de Compras, Gestión de Depósito, Gestión Comercial, Gestión Servicio Post-venta, Gestión Contable |
| Aplicaciones | CALIPSO (ERP) - núcleo transversal; Google Workspace; WhatsApp; Zendesk (RMA); uso puntual de IA (ChatGPT, Cursor AI, sin integración formal) |
| Datos | Datos transaccionales (ERP): clientes, ventas, pedidos, stock, proveedores, facturación; datos de postventa (tickets); documentación operativa; backups e históricos |
| Infraestructura | 25 endpoints (15 PC + 10 laptops), 1 servidor on-prem (Windows Server 2022), doble enlace ISP, firewall Ubiquiti, Windows Defender, Dropbox (backup) |

*Marco de referencia: TOGAF - The Open Group (Método de Desarrollo de Arquitectura)*

**Otro ejemplo — Arquitectura Actual (Estado Presente) de una empresa menos madura:**

| Capa | Contenido |
|---|---|
| Procesos | Búsqueda terrenos, Análisis mercado, Negociación compra, Creación proyecto, Aprobaciones municipal., Contratos proveedores, Comercializ. + Obra |
| Aplicaciones | WhatsApp (coordinación), Google Drive, Excel (finanzas), Email |
| Datos | Clientes (Excel), Proveedores (Excel), Ventas (Excel), Gastos (Excel), Proyectos (carpetas), Contratos (físico) |
| Tecnología | MacBook Pro Sonoma 14.1, Notebooks personales |

> Madurez actual (modelo CMM): 2/5 · Sin digitalización · Procesos informales

### Transición de arquitectura: Origen (as-is) → Destino (to-be)

**Arquitectura de Negocio:**
- Origen (as-is): Flujos de Valor, Capacidades de Negocio, Activos de Información, Estructura Organizacional
- Destino (to-be): mismos elementos, evolucionados según la visión objetivo

**Arquitectura de TI:**
- Origen (as-is): Artefactos de Arquitectura de Aplicaciones, de Datos, Tecnológica, y de "Shadow IT"
- Destino (to-be): Dominios de Arquitectura de Aplicaciones, de Datos, Tecnológica, y de "Shadow IT"

**Proceso de transformación:**
- **Transformación de Negocio**: de Arq. de Negocio Origen → Arq. de Negocio Destino
- **Transformación de TI**: de Arquitectura de TI Origen → Arquitectura de TI Destino
- **Sincronización** de ambas transformaciones (Negocio y TI deben avanzar de forma coordinada)
- **Mapeo de arquitecturas** (origen y destino) conecta el nivel de negocio con el nivel de TI en cada momento

---

## Marcos de referencia y el rol del arquitecto

### Marco metodológico de Arquitectura Empresarial: TOGAF

El ciclo TOGAF (ADM - Architecture Development Method) se organiza en fases (A a H), agrupadas en:

**Estrategia & Motivación:**
- A. Visión de Arquitectura
- H. Gestión de los Cambios de Arquitectura

**Capas clave** (Negocio, Aplicaciones y Datos, Tecnología):
- B. Arquitectura de Negocio
- C. Arquitectura de Sistemas de la Información
- D. Arquitectura Tecnológica

**Implementación & Migración:**
- E. Oportunidades y Soluciones
- F. Plan de Migración
- G. Implementación y Gobernanza

En el centro del ciclo: **Gestión de Requerimientos**, que conecta todas las fases.

### El rol del Arquitecto Empresarial

| Aspecto | Detalle |
|---|---|
| **Qué hace** | Releva la arquitectura actual, define la arquitectura objetivo y explicita el porqué de cada decisión. |
| **Con quién trabaja** | Dirección, dueños de procesos, líderes de proyecto, proveedores y equipos técnicos. |
| **Qué entrega** | Diagramas y catálogos, principios de decisión y recomendaciones de inversión priorizadas. |
| **Qué se le pide** | Visión amplia antes que profundidad técnica, y saber explicar en lenguaje de negocio. |

> **No decide solo:** su herramienta es la argumentación y el acuerdo entre el negocio y la tecnología.
