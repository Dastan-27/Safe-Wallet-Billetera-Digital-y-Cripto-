# Safe-Wallet (Billetera Digital y Cripto)

---

## Fase 1: Auditoría Forense y Diagnóstico

### 1. Dinámica de Trabajo
[🔗 Ver Matriz de Hallazgos en Figma](https://www.figma.com/design/Zm7zxZaIRwTYgi4E4CbZY4/Matriz-de-Hallazgos--Safe-Wallet?node-id=0-1&t=Gb6c4jlcMoxH12o2-1)

### 2. Tareas por Rol (Entregables Individuales)

#### Rol A: Auditor de Ecosistema
**Misión:** [Escribe aquí la misión principal del rol]
- **Errores encontrados:**
  - [Describe el error 1]
  - [Describe el error 2]
- **Soluciones propuestas:**
  - [Describe la solución 1]
  - [Describe la solución 2]

#### Rol B: Analista de Psicología UX
**Misión:** [Escribe aquí la misión principal del rol]
- **Errores encontrados:**
  - [Describe el error 1]
  - [Describe el error 2]
- **Soluciones propuestas:**
  - [Describe la solución 1]
  - [Describe la solución 2]

#### Rol C: Especialista en UI y Jerarquía
**Misión:** [Escribe aquí la misión principal del rol]
- **Errores encontrados:**
  - [Describe el error 1]
  - [Describe el error 2]
- **Soluciones propuestas:**
  - [Describe la solución 1]
  - [Describe la solución 2]

#### Rol D: Oficial de Ética y Fricción
**Misión:** Cazar *Dark Patterns* y Fricción Negativa. 

**Errores de cada pantalla:**

- **Costos Ocultos (Pantalla 3: Confirmación de Compra)**
  - **El Problema:** En la pantalla de confirmación, observamos un claro caso de *Drip Pricing* (Precios por Goteo) y Costos Ocultos.
  - **La trampa matemática:** El usuario está comprando 0.05 BTC a un precio de $28,500. El costo base del activo es de $1,425 (0.05 x 28,500). Sin embargo, el "Total a Pagar" exige $1,567.25.
  - **La falta de transparencia:** Hay un sobrecosto de $142.25 (casi un 10% del valor de la transacción) que se agrupa bajo una línea de texto gris, pequeña y sin desglosar que dice: + Tasa de Red y Comisión de Servicio.
  - **Impacto ético:** El usuario se entera del costo real justo en el último segundo, aprovechando la fatiga de la decisión para forzar una transacción desproporcionadamente cara. Esto es inaceptable para una plataforma financiera formal.

- **Confirmshaming y Fricción Negativa (Pantalla 5: Notificación Alarmista)**
  - **El Problema:** Esta pantalla es un compendio de manipulación emocional diseñado para forzar operaciones (y por ende, cobrar comisiones).
  - **Alarmismo (Fear-mongering):** El título en rojo "¡EL MERCADO SE DESPLOMA!" y el subtítulo "Vende ahora o piérdelo todo" generan pánico irracional. En el mundo de las inversiones, las caídas son normales; inducir al pánico provoca que el usuario tome decisiones financieras perjudiciales basadas en el miedo.
  - **Confirmshaming:** Al intentar descartar la acción, la única opción para no vender es un botón que obliga al usuario a aceptar una premisa humillante y aterradora: "No, prefiero perder mis ahorros".
  - **Impacto ético:** Se está castigando psicológicamente al usuario por no realizar la acción que la empresa desea. Esta práctica destruye la percepción de Safe-Wallet como una herramienta "profesional" y la acerca al terreno de las estafas.

**Soluciones para cada pantalla:**

- **A. En la Confirmación de Compra (Solución a Pantalla 3):**
  - **Desglose Obligatorio:** Antes de habilitar el botón de compra, el usuario debe ver un recibo detallado: Monto en BTC + Comisión de Safe-Wallet + Tasa de Red (Minero).
  - **Fricción Positiva:** Reemplazar el botón de un solo toque ("Confirmar Compra") por un mecanismo de confirmación activa, como un "Deslizar para Comprar" (*Swipe to Buy*) o requerir el PIN/Biometría después de mostrar el recibo transparente. Esto asegura que el usuario no compre por accidente y esté 100% consciente del costo final.

- **B. En Situaciones de Alta Volatilidad (Solución a Pantalla 5):**
  - **Alertas Neutrales:** Cambiar el UX Writing por un lenguaje informativo: "El valor de BTC ha bajado un X% en la última hora. Revisa el mercado".
  - **Fricción Positiva en Ventas de Pánico:** Si el usuario decide vender durante una caída abrupta, implementar un modal de advertencia neutro (*Cooling-off prompt*): "Estás a punto de liquidar tus activos durante un periodo de alta volatilidad. ¿Deseas proceder con la venta de 0.05 BTC?".

---

## Fase 2: Re-Arquitectura y User Flow en Lucidchart

### 1. El Reto de Simplificación: "Finanzas con Claridad"
[🔗 Ver flujo general en Lucidchart](https://lucid.app/lucidchart/f4541a30-d4fc-468b-8268-a6b27c53f342/edit?viewport_loc=-884%2C-662%2C4988%2C2288%2C0_0&invitationId=inv_cffc7c59-fd8e-4ea0-8f9b-8b8da9f439f7)

### 2. Tareas por Rol en esta Fase

- **Estudiante 1 (Ecosistema):** [🔗 Ver esquema en Lucidchart](https://lucid.app/lucidchart/da588949-1c3d-4186-a9bd-8210c2cc15de/edit?viewport_loc=185%2C339%2C3365%2C1544%2C0_0&invitationId=inv_22fbdec7-51fd-4de8-898b-f2f654a693df)
- **Estudiante 2 (Arquitecto de Información):** [🔗 Pegar enlace aquí](#)
- **Estudiante 3 (UX Writer):** [🔗 Pegar enlace aquí](#)
- **Estudiante 4 (Validador de Usabilidad):** [🔗 Pegar enlace aquí](#)

---

## Fase 3: Prototipado de Media Fidelidad (Wireframes)
[🔗 Ver prototipos en Figma (Ecocanje)]([https://www.figma.com/design/2cDx3ToZ6Pl12HhILkbTQU/Ecocanje?node-id=0-1&t=77TC2K6Nf5RZq3pt-1](https://www.figma.com/design/ZheGFEoDzcdFFYaY0L9L6C/Sin-t%C3%ADtulo?node-id=6-78&t=2fHv8oyUqIzmoyq1-1))
