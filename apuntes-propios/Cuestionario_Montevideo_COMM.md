# Cuestionario para entrevista técnica — Montevideo COMM (proveedor de sistema de IBER)

> Apunte propio (no material oficial de la cátedra). Objetivo: completar los campos "Pendiente" de `02__Arquitectura_empresarial/02-Arquitectura-Empresarial-Actual-Desarrollo-Parcial.md` (Arquitectura de Datos, Aplicaciones y Tecnológica) con información real, ya que el cliente (IBER) no tiene personal de IT propio y no conoce estos detalles.
>
> Lo que se puede inferir por fuera (stack visible del sitio público https://iber.uy/) no se pregunta acá — solo lo que no es observable externamente: backend, base de datos, hosting, integraciones internas, seguridad y el desarrollo a medida sobre Odoo.

---

## 0. Contexto de la entrevista

- Rol de la persona entrevistada dentro de Montevideo COMM (para calibrar el nivel de detalle esperado: ¿es quien toma decisiones de arquitectura, o es soporte/funcional?).
- Hace cuánto tiempo trabajan con IBER y qué alcance tiene el contrato (desarrollo a medida, mantenimiento, ambos).
- ¿Hay documentación técnica existente (diagramas, manual de arquitectura, API docs) que puedan compartir en vez de/además de responder verbalmente?

---

## 1. Arquitectura de datos

- ¿Qué motor de base de datos usa el ERP (Odoo)? ¿Postgres (el nativo de Odoo), u otro?
- ¿La base de datos está alojada en la nube o on-premise (servidor propio de IBER)? Si es nube, ¿qué proveedor (AWS, GCP, Azure, hosting local)?
- ¿Es una única base de datos o hay varias (por ejemplo, una para el ERP, otra para e-commerce, otra para el "Excel automatizado" que mencionó el cliente)?
- **Pregunta puntual de nuestro relevamiento con el cliente:** ¿la base de Odoo de IBER (Uruguay) está compartida/integrada con la de "Culpable" (la empresa hermana en Argentina), o son instancias separadas del mismo software?
- Entidades/módulos principales que administra el sistema (productos, stock, órdenes de compra, clientes, envíos, etc.) — para completar la columna "Entidades principales".
- Seguridad y accesos: ¿cómo se gestionan los permisos por rol/usuario? ¿Hay logs de auditoría?
- Medidas de seguridad: cifrado, backups (frecuencia, dónde se guardan), plan de recuperación ante desastres.

## 2. Arquitectura de aplicaciones

- Catálogo completo de aplicaciones que corren sobre o junto al ERP: ¿solo Odoo + desarrollo a medida, o hay módulos/sistemas satélite (por ejemplo, el "pronosticador de compra" que mencionó el cliente, el sistema de e-commerce, la integración con Mercado Libre)?
- E-commerce: ¿es un módulo de Odoo o una plataforma aparte integrada por API?
- **Sistema de cobros a clientes** (tu pregunta original): ¿cómo se procesan los pagos? ¿Integran alguna pasarela de pago (ej. dLocal, Mercado Pago, procesadora de tarjetas local uruguaya)? ¿Es todo dentro del ERP o hay un sistema de facturación/cobranza separado?
- Integración con el courier del e-commerce: el cliente mencionó que hoy la actualización de estado de envío (en preparación → despachado → entregado) es manual. ¿Existe alguna integración vía API con el courier que no se esté usando, o directamente no existe?
- ¿Qué gestiona la casilla de correo que el cliente mencionó como "Rova Iber" (posiblemente mal transcripta)? ¿Es un buzón genérico conectado a algún flujo automático (por ejemplo, ingreso de pedidos por mail) o solo un mailbox compartido?
- ¿Hay app móvil (para clientes, para vendedores/depósito) o todo es vía navegador/web?

## 3. Arquitectura tecnológica

- Lenguaje(s) de programación del desarrollo a medida sobre Odoo (Python es el nativo de Odoo — ¿hay algo adicional, por ejemplo un frontend separado en otro lenguaje?).
- Framework de frontend, si aplica (para el e-commerce o algún portal aparte del ERP).
- Infraestructura: ¿servidores propios (on-premise) o en la nube? Si es nube, ¿qué proveedor?
- Sistema operativo de los servidores.
- ¿Cómo se resuelven las integraciones entre sistemas (APIs propias, webhooks, procesos batch/nocturnos)?
- Redes y seguridad perimetral: ¿manejan ellos el firewall/VPN de acceso al sistema, o eso es responsabilidad del otro proveedor de IT tercerizado de IBER (el que atiende impresoras, notebooks, etc.)? Esto es importante para no mezclar responsabilidades entre los dos proveedores tercerizados que mencionó el cliente.
- ¿Cómo es el esquema de ambientes (desarrollo/testing/producción)? ¿Hay control de versiones y despliegues, o los cambios se aplican directo en producción?

## 4. Soporte, mantenimiento y relación contractual

- ¿Cómo funciona el soporte ante incidentes (SLA, tiempos de respuesta, canal de contacto)?
- ¿Quién define y prioriza el backlog de mejoras — IBER pide funcionalidades puntuales, o Montevideo COMM también propone cambios proactivamente?
- Dado el diagnóstico del cliente sobre logística (falta de trazabilidad, autorizaciones, nómina de fletes centralizada): ¿qué tan viable ven, desde el lado técnico, construir esas mejoras sobre el Odoo actual (nuevos módulos/campos) versus necesitar un sistema o integración externa?

---

## Notas de uso

- Las preguntas de la sección 1 y 2 relacionadas con "Culpable" y "Rova Iber" dependen de que Macarena confirme antes el detalle exacto — revisar antes de la entrevista si ya hay respuesta.
- Priorizar las preguntas de la sección 3 (lenguaje, hosting, seguridad) si el tiempo de entrevista es acotado — son las que menos se pueden inferir por otro medio.
- Si la persona entrevistada no puede responder algo de arquitectura profunda (por ser perfil funcional/soporte), pedir que derive la pregunta a alguien del equipo técnico o que comparta documentación.
