# Relevamiento organizacional — Iberpark / IBER (Uruguay)

> **Nota de origen:** este es un apunte propio (no material oficial de la cátedra), consolidado a partir de:
> 1. `Fuente_Transcripciones_Iberpark.md` — transcripción automática (Whisper) de audios 001 a 037 + mensajes de texto de la entrevista con el cliente, con contacto directo de Macarena Ignacio.
> 2. Aclaraciones de chat entre el equipo (Juan Torres / Macarena Ignacio).
> 3. Material oficial del repo de la cátedra: `01__Caso_de_Negocio/Relevamiento_Inicial_Cliente.md` y `01__Caso_de_Negocio/Estructura_organizacional_IBER.md`.
>
> Donde hay dato confirmado por (3) se prioriza sobre lo dicho en los audios, según lo indicado en CLAUDE.md. Donde algo es una inferencia o sigue sin confirmar, se marca explícitamente como tal.

---

## 1. Datos generales de la empresa

- **Nombre:** Iberpark / IBER (dominio de correo institucional confirmado: `@iber.uy`, ver `Relevamiento_Inicial_Cliente.md`).
- **Empresa hermana en Argentina:** llamada literalmente **"Culpable"** — no es un error de transcripción de Whisper, es el nombre real de la empresa (confirmado por Macarena Ignacio en el chat del equipo, 8/9/2026).
- **Rubro (confirmado, no es inferencia):** tienda de retail con foco en bebidas alcohólicas y productos gourmet, con fuerte posicionamiento como importadora de vinos.
- **Antigüedad:** 30 años en el mercado.
- **Personal:** ~100 personas en promedio (dato oficial del cliente; distinto del cálculo de "30 a 40 computadoras/celulares" mencionado en el audio 015, que solo cubre parte del personal con equipo asignado — no son cifras contradictorias, solo miden cosas distintas).
- **Presencia geográfica:** Montevideo, Las Piedras, Ciudad de la Costa, Salto, Paysandú, Mercedes, Colonia, Minas, Punta del Este y canal web.
  - *Pendiente:* el audio 015 menciona "20 tiendas" de forma incidental (al estimar computadoras), pero no coincide en granularidad con esta lista de 9 localidades — probablemente hay varias tiendas por ciudad (sobre todo en Montevideo). No hay un número total de tiendas confirmado explícitamente todavía.
- **Estructura:** empresa de tipo familiar, con fuerte involucramiento de la gerencia en tareas operativas además de las estratégicas (audio 014).
- **Misión:** orientada a satisfacción de clientes y consumidores mediante calidad de producto y excelencia de servicio.
- **Visión:** ser la tienda líder, joven, sólida e innovadora en comercialización de vinos, espirituosas, gourmet y otras especialidades.
- **Valores declarados:** pasión y compromiso.
- **Cadena de valor:** proveedores locales y del exterior de mercadería y de servicios, más cada área interna de la empresa.

---

## 2. Estructura organizacional

### 2.1 Organigrama oficial (fuente: `Estructura_organizacional_IBER.md`)

```
Dirección
└── Gerente General
    ├── Jefatura de Gestión Humana
    ├── Jefatura de Operaciones y Ventas
    │   └── Encargados de Tiendas
    │       └── Colaboradores de Tiendas
    ├── Gerente Comercial
    │   ├── Jefatura de Compras
    │   │   └── Asistente de Compras
    │   └── Encargado del Centro Logístico
    │       └── Auxiliares de Depósito
    ├── Jefatura de Marketing
    │   └── Asistentes de Marketing
    ├── Brand Ambassador
    │   └── Asistentes del Brand Ambassador
    └── Gerencia de Administración
        └── Asistentes de Administración
```

> *Brand Ambassador y Gerencia de Administración* no aparecen mencionados en los audios de la entrevista; se incorporan acá porque están confirmados en el organigrama oficial del repo.

### 2.2 Cómo se relaciona esto con lo dicho en los audios

- **Importación / comercio exterior (audio 002):** el cliente describe una persona operativa de comercio exterior bajo el Gerente Comercial (logística internacional, documentación, fletes, liberación aduanera INAVI/INV, costeo). **Pendiente:** este rol no aparece como nodo propio en el organigrama oficial — habría que confirmar si está contenido dentro de "Jefatura de Compras" o si el organigrama está incompleto en ese punto.
- **Compra nacional (audio 003):** el audio habla de "auxiliar de compras"; el organigrama oficial lo llama **"Asistente de Compras"**. Se usa el término oficial como referencia primaria.
- **Centro logístico (audio 021):** el cliente menciona "un encargado más dos peones"; el organigrama oficial llama a ese rol **"Auxiliares de Depósito"** bajo el "Encargado del Centro Logístico".
- **Marketing (audio 004):** confirmado que depende de Gerencia General, no de Comercial — coincide con el organigrama oficial.
- **RRHH:** existe como **"Jefatura de Gestión Humana"**, reportando a Gerente General (confirmado por el organigrama oficial; no había detalle de esto en los audios de esta tanda).
- **Legales (audio 016):** tercerizado (arquitecto, abogada/escribana, contador externo asesor) — no depende de un área interna.
- **Mantenimiento (audios 017/018, contenido idéntico):** tercerizado.
- **IT (audio 023):** no hay personal de IT propio.
  - El sistema (programa, desarrollos, día a día) lo maneja una consultora externa llamada **"Montevideo COMM"** (confirmado — el audio la transcribe como "Montevideo.com"; contacto: Paula y su equipo).
  - Un equipo de IT tercerizado aparte atiende infraestructura interna (hardware, impresoras, instalaciones, respaldo/nube).

### 2.3 Ventas (audio 005)

- **Canal tiendas:** Jefatura de Operaciones y Ventas → Encargados de Tiendas → Colaboradores de Tiendas (cajeros, vendedores, reponedores).
- **E-commerce:** depende de Marketing (web, Mercado Libre).
- **Canal HORECA (interior del país):** un vendedor en Montevideo y un vendedor en Punta del Este/Maldonado (ver aclaración de nombre en sección 6).
- **Venta corporativa:** supervisada por Jefatura de Operaciones y Ventas.
- **Clientes VIP / preferenciales:** atención diferenciada.
- **Regalos corporativos (canastas de fin de año):** proceso estacional; empresas encargan grandes volúmenes (ej. 500 regalos), a entregar en un único punto o distribuidos a múltiples direcciones.

---

## 3. Sistemas y arquitectura de datos

- **ERP base:** **Odoo**, con un desarrollo a medida sobre Odoo.
  - **Pendiente de confirmar (punto explícitamente marcado como "a confirmar" por el equipo):** si Odoo está efectivamente **compartido/integrado** entre Iberpark (Uruguay) y "Culpable" (la empresa hermana en Argentina), o si son instancias independientes del mismo software. Se espera confirmación de Macarena sobre a qué se refería puntualmente el audio 007 en ese punto.
  - **Evidencia externa (análisis de los sitios públicos `iber.uy` y `culpable.com.ar`, 2026-09-13):** ambos corren Odoo, pero con versiones y huellas de servidor claramente distintas — `iber.uy` responde `Werkzeug/0.11.15 Python/3.6.12` (versión vieja, ~Odoo 10/11), mientras que `culpable.com.ar` responde `Werkzeug/3.0.1 Python/3.12.0` y expone `websocket_worker_version: "18.0-5"` (Odoo 18, actual). Ambos sitios están alojados por el mismo proveedor uruguayo (`mvdsimple.uy`, visible en el header `Via`), pero como sitios distintos (`sitio103078.p10...` vs `sitio153455.p18...`). Esto sugiere fuertemente que **son dos instancias de Odoo separadas**, no una base compartida — aunque no es 100% concluyente (una empresa podría tener dos instancias vinculadas por integración externa). **Confirmar igual con Montevideo COMM en la entrevista.**
- **Módulo de pronóstico de compras:** en base a stock actual e histórico de ventas, determina diariamente qué falta por proveedor y por local, generando una orden de compra sugerida que luego confirma el área de compras según calendario de entrega.
- **Excel de apoyo:** vistas y reportes automatizados sobre ventas del último período, usado como complemento para la reposición.
- **E-commerce:** integrado con generación automática de etiqueta de envío y número de envío al confirmar un pedido.
- **Proveedor externo del sistema:** Montevideo COMM (desarrollo y mantenimiento del ERP/sistema).
- **Comunicación por correo:** existe una casilla mencionada como "Rova Iber" (audio 013) para recepción de pedidos/comprobantes — **pendiente confirmar** nombre y uso exacto (no verificado aún contra el repo).

---

## 4. Infraestructura tecnológica

- **Computadoras:** estimado entre 30 y 40 equipos (≈20 asignadas a tiendas, 2 en depósitos, ≈15 en administración) — dato del audio 015, referido solo al personal con equipo asignado (no a la totalidad de ~100 personas de la empresa).
- **Celulares:** cantidad similar a la de computadoras.
- **Sistemas operativos:** mayoría Windows; una minoría con Mac. En celulares, proporción similar.
- **Modalidad de trabajo:** principalmente notebooks y celulares (no computadoras fijas).

---

## 5. Logística — situación actual y diagnóstico

Área de mayor foco del relevamiento ("un tema que se supone que tenemos que solucionar"). Confirmado además como objetivo estratégico explícito en `Relevamiento_Inicial_Cliente.md`: automatizar, programar y controlar todos los canales de envío desde el ERP (armado de rutas, selección de proveedor/modalidad, trazabilidad, cobros, costos, autorizaciones).

### 5.1 Logística internacional (importación desde Argentina/Chile)
- El comercial genera pedidos a distintas bodegas, mayoritariamente en Mendoza (rara vez Salta).
- El asistente de comercio exterior arma los camiones (completos o compartidos entre varias bodegas) según pallets, peso, fechas de pedido listo y urgencias comerciales — hoy todo gestionado en Excel.
- **Problema identificado:** falta que el sistema (no solo Excel) registre desde el inicio del pedido cantidades, pesos y pallets, y sobre todo falta trazabilidad: qué camión llevó qué bodegas, fecha comprometida de salida vs. real, fecha de llegada, y responsable de cualquier demora (fletero, bodega, o la propia empresa). Hoy la coordinación es informal ("boca a boca", mensajes sueltos) y no queda registro histórico.

### 5.2 Centro logístico → distribución a tiendas
- Distribución mensual por transferencia interna cargada en el sistema (entre 1 y 4 pallets según el tamaño del local).
- El proceso completo de reparto a todos los locales demora unas 2 semanas, sin visibilidad clara de fechas por local.
- **Mejora deseada por el cliente:** que el encargado informe con anticipación qué día sale cada local, con qué proveedor de flete tercerizado y a qué costo; y que luego se confirme la entrega real — para tener una vista global de todos los envíos (locales, internacionales y e-commerce).

### 5.3 Depósitos secundarios — canal HORECA
- El audio transcribe este canal como "ORECA"/"OREKA"; el nombre correcto es casi seguro **HORECA** (Hoteles, Restaurantes, Cafés), confirmado por `Relevamiento_Inicial_Cliente.md` ("canal HORECA Montevideo", "canal HORECA Punta del Este").
- **Depósito 2 (Montevideo):** mismo depósito de backup, al lado de la oficina — abastece HORECA Montevideo.
- **Depósito 3:** el audio lo ubica en "Maldonado"; el documento oficial lo especifica como **Punta del Este** (ciudad dentro del departamento de Maldonado) — abastece HORECA Punta del Este. No se trata de una contradicción, sino de distinto nivel de precisión geográfica.
- Operativa: el vendedor carga el pedido ("SEO"), el encargado del depósito lo prepara y despacha.
- **Falta:** registro de la fecha real de envío y del medio utilizado (camioneta propia o flete tercerizado, con su costo). Hoy la coordinación es informal (WhatsApp / mail). Mismo problema en ambos depósitos: no hay trazabilidad de cantidad de envíos, medio utilizado, ni tiempos reales de entrega.

### 5.4 Transferencias entre tiendas propias
- Cuando una tienda no tiene stock de un producto pero otra cercana sí, se transfiere directamente entre locales para no perder la venta ante la urgencia del cliente.
- **Falta control de:** costo del envío, con quién se realizó, quién lo autorizó, y si la operación se justificaba económicamente.

### 5.5 Clientes VIP y venta corporativa
- Se gestionan también mediante órdenes ("SEO"), pero sin trazabilidad, de forma similar al canal HORECA.

### 5.6 Fletes y proveedores de transporte
- Casi todos los fletes están **tercerizados**, salvo una camioneta propia con chofer que opera desde el depósito de backup (Montevideo).
- Existe un sistema donde se cargan los pedidos, pero **no hay seguimiento del flete en sí**: no queda registrado qué modalidad se usó por proveedor (por pallet, por hora, camión completo), ni si se cumplió la fecha de entrega comprometida.
- La asignación de qué flete usar depende del **conocimiento informal de cada persona** (ej.: "para tal zona se llama a tal proveedor", "con Pedidos Ya se carga en su plataforma", otros fleteros se contratan por hora llamando directamente). Este conocimiento no está sistematizado ni es igual entre todos los encargados (ej.: un encargado nuevo puede no saber cómo enviar una caja a Montevideo).
- El sistema exige indicar la "cadetería" al hacer un envío entre locales, pero no todos los fleteros están dados de alta como opción, y cualquier usuario puede elegir libremente cuál usar, sin restricciones ni autorización.
- Tienen habilitado el servicio de **"Pedidos Ya"**, pero sin control de la empresa sobre cuándo se autoriza su uso: al estar simplemente habilitado, el personal lo usa libremente.
- La información de proveedores de flete está fragmentada: cada persona conoce una parte (tarifas, contactos), no existe una nómina centralizada y accesible para todos. Los Excel individuales se pierden o quedan desactualizados cuando cambian las personas.
- Las facturas de flete llegan y se pagan correctamente (se sabe de quién son), pero esa información no está disponible para todos los involucrados en el proceso.

### 5.7 E-commerce (el proceso más automatizado, aunque incompleto)
- Al llegar un pedido desde la web se genera automáticamente la etiqueta de envío del courier, se asigna un número de envío y se notifica al proveedor.
- Existen grupos de WhatsApp entre el equipo de e-commerce y los fleteros para seguimiento informal.
- **Falta:** integración con el courier — no hay actualización automática de estado (en preparación → despachado → entregado); hoy cada cambio de estado lo carga manualmente una persona en el sistema, sin conexión directa con la plataforma del proveedor de envíos.

### 5.8 Diagnóstico del cliente (síntesis, en sus propias palabras)
- Falta un lugar único en el sistema donde figuren todos los proveedores de flete, su tipo de servicio (por hora, camión, pallet, bulto, kilómetro) y su tarifa, para poder elegir automáticamente la mejor opción según el tipo de envío.
- Falta un esquema de **autorización por monto**: envíos por encima de cierto valor deberían requerir aprobación del gerente general; envíos menores entre locales deberían requerir la del jefe de operaciones. Hoy no existe control cruzado — cualquiera decide cómo y con quién enviar.
- Conclusión textual del cliente: *"funcionar, funcionamos, pero falta tecnología y proceso"* — el proceso formal de logística debe generarse desde cero.

---

## 6. Notas sobre la fuente (correcciones y aclaraciones de transcripción)

- Las transcripciones fueron generadas automáticamente (Whisper) a partir de los audios, por lo que contienen imprecisiones fonéticas, especialmente en nombres propios.
- **"Culpable"** → **no es un error de transcripción**: es el nombre real de la empresa hermana en Argentina (confirmado por el equipo vía chat, 8/9/2026). Se corrige la versión anterior de este documento, que asumía erróneamente que era una mala transcripción de "Iberpark".
- **"DUDU"** → **Odoo** (ERP).
- **"ORECA" / "OREKA"** → casi seguro **HORECA** (canal Hoteles, Restaurantes, Cafés), confirmado por `Relevamiento_Inicial_Cliente.md`.
- **"Rova Iber"** → posible casilla de correo genérica, mencionada por el relevador en el audio 013 — pendiente de confirmar nombre y uso exacto.
- **"Montevideo.com"** → nombre real: **Montevideo COMM**, consultora de tecnología externa (confirmado).
- **"Inavi / INV"** → correctamente transcripto: Instituto Nacional de Vitivinicultura de Uruguay (INAVI) y de Argentina (INV).
- Se identificó un posible desfasaje entre la numeración de archivos y el orden real de algunas menciones puntuales (ej. entorno a los audios 015/019/023), que el equipo decidió no forzar a encajar por no contar con la referencia exacta del audio citado.
- El contenido del audio 022 ("logística internacional") quedó cortado / sin desarrollo audible más allá de la introducción del tema.

---

## 7. Pendientes de relevamiento / confirmación

- Detalle final y cierre del tema "logística internacional" (audio 022 incompleto).
- Confirmar el uso exacto de la casilla de correo mencionada como "Rova Iber" (qué tipo de documentos/pedidos recibe).
- Nómina completa y centralizada de proveedores de flete (tarifas, tipo de servicio, contacto) — actualmente inexistente de forma unificada.
- Confirmar si existen otros procesos de apoyo no relevados aún, más allá de Jefatura de Gestión Humana (RRHH), Legales, Mantenimiento e IT.
- **Confirmar si Odoo está efectivamente compartido/integrado con "Culpable" (Argentina)** o si son instancias separadas del mismo software — a la espera de que Macarena confirme a qué se refería puntualmente el audio 007. *Actualización:* el análisis externo de ambos sitios (ver sección 3) sugiere que son instancias separadas (versiones de Odoo y de servidor distintas), pero se mantiene como pendiente de confirmación directa con el proveedor.
- **Confirmar la cantidad total de tiendas** — el audio 015 menciona "20" de forma incidental, pero no coincide en granularidad con la lista de 9 localidades del `Relevamiento_Inicial_Cliente.md`.
- Confirmar si el rol de "comercio exterior" descrito en el audio 002 corresponde a un puesto dentro de "Jefatura de Compras" en el organigrama oficial, o si el organigrama está incompleto en ese punto.
