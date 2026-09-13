# Cuestionario técnico — Sistema de Iber

**Organización:** IBER
**Consultora:** Next Step — Consultoría en Tecnología
**Asignatura:** Actuación Profesional del Licenciado en Sistemas de Información (APLSI) — FCE-UBA

> Apunte propio (no material oficial de la cátedra). Pensado para ser leído y usado directamente por quien haga la entrevista (aunque no tenga formación técnica), y potencialmente compartido con la persona entrevistada de Montevideo COMM.

Este cuestionario tiene como objetivo relevar información sobre el sistema que Montevideo COMM desarrolla y mantiene para Iber, en el marco de un trabajo académico de arquitectura empresarial. No se requiere un nivel de detalle técnico exhaustivo — alcanza con una descripción general de cada punto.

---

## 1. Preguntas cruciales

1. ¿El sistema corre en servidores propios de la empresa, o está alojado en la nube (por ejemplo, en un proveedor externo como Amazon u otro)?
2. Actualmente, el estado de un pedido online (en preparación / despachado / entregado) se actualiza de forma manual. ¿Es posible conectar el sistema con la empresa de envíos para que esa actualización sea automática?
3. ¿La base de datos de Iber (Uruguay) es la misma que la de Culpable (Argentina), o son dos sistemas independientes entre sí?
4. ¿Con qué frecuencia se realizan copias de seguridad de la información? Ante una falla grave, ¿qué volumen de información se podría llegar a perder y cuánto tiempo tomaría restablecer el sistema?
5. ¿El sistema (Odoo) está en una versión actualizada, o corresponde a una versión anterior? Si es una versión anterior, ¿actualizarla sería un ajuste menor o un proyecto grande? ¿Está prevista alguna actualización?

## 2. Preguntas secundarias (a tratar si el tiempo lo permite)

6. Ante un incidente o falla, ¿cómo funciona el soporte? ¿A quién se contacta y en qué plazo suelen responder?
7. Las mejoras o cambios al sistema, ¿los solicita Iber puntualmente, o Montevideo COMM también las propone?
8. Si Iber quisiera avanzar con una propuesta de mejora concreta (por ejemplo, sobre la logística), ¿cómo sería el proceso desde el lado de Montevideo COMM: cómo la evaluarían y, a grandes rasgos, en qué plazos podrían encararla?

## 3. Información ya relevada (para revisar y confirmar o corregir)

Antes de la entrevista, revisamos la información pública de los sitios web de Iber y Culpable para no hacer preguntas innecesarias. A continuación detallamos qué encontramos y cómo, para que puedan marcar qué está bien y corregir lo que no.

| Punto | Cómo lo inferimos | ¿Es correcto? |
|---|---|---|
| El sistema usado es **Odoo** (un ERP conocido, usado por muchas empresas) | Se ve en información pública del código de la página de `iber.uy`, visible para cualquiera que entra al sitio | ☐ Sí &nbsp;&nbsp; ☐ No, es: _______ |
| La **tienda online es parte del mismo sistema**, no una plataforma aparte | La tienda usa los mismos archivos internos que el resto del sitio | ☐ Sí &nbsp;&nbsp; ☐ No, es: _______ |
| Los **pagos se procesan a través de PlaceToPay** (una pasarela de pagos), que redirige a cada banco o tarjeta para autorizar el pago | Se hizo una compra de prueba hasta la pantalla de pago (sin completarla); ahí aparecen las opciones de bancos/tarjetas, y al elegir un banco (BROU) redirige a la plataforma real de ese banco | ☐ Sí &nbsp;&nbsp; ☐ No, es: _______ |
| **Iber y Culpable parecen tener sistemas separados**, no uno compartido | Ambos sitios usan Odoo, pero muestran versiones del sistema notoriamente distintas entre sí (una parece bastante más nueva) — señal fuerte, aunque no 100% confirmada desde afuera | ☐ Sí &nbsp;&nbsp; ☐ No, es: _______ |
