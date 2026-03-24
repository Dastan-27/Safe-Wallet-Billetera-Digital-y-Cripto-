# Safe-Wallet (Billetera Digital y Cripto)

---

## Fase 1: Auditoría Forense y Diagnóstico

### 1. Dinámica de Trabajo
[🔗 Ver Matriz de Hallazgos en Figma](https://www.figma.com/design/Zm7zxZaIRwTYgi4E4CbZY4/Matriz-de-Hallazgos--Safe-Wallet?node-id=0-1&t=Gb6c4jlcMoxH12o2-1)

### 2. Tareas por Rol (Entregables Individuales)

#### Rol A: Auditor de Ecosistema
**Misión:** Analizar la factibilidad y el hardware.

**¿Por qué es una falla de ecosistema?**  
Es una falla de ecosistema porque el sistema depende de varios elementos externos que no siempre funcionan correctamente, tales como:

1. **Hardware del dispositivo:** la cámara frontal puede estar sucia o dañada.  
2. **Condiciones del entorno:** puede haber poca iluminación o movimiento del usuario.  
3. **Sensores biométricos del teléfono:** algunos celulares tienen sensores menos precisos.  
4. **Conexión con servidores de autenticación:** pueden presentarse retrasos o fallos en la comunicación.  

Cuando esto ocurre, el sistema asume que el usuario intenta acceder de forma fraudulenta, cuando en realidad el problema puede ser técnico. Por eso, bloquear la cuenta automáticamente por 24 horas genera frustración y pérdida de confianza.

- **Impacto en el usuario:**
  - El usuario queda sin acceso a su dinero.
  - No recibe una explicación clara del error.
  - No tiene métodos alternativos para ingresar.
  - Puede pensar que la aplicación no es confiable.

- **Propuesta de mejora:**
  - **Autenticación multifactor (MFA):** si el Face ID falla 3 veces, ofrecer una alternativa segura.
  - Enviar un código al correo registrado para que el usuario pueda ingresar a la aplicación.
  - Esto mantiene la seguridad y evita bloquear al usuario de manera inmediata.

#### Rol B: Analista de Psicología UX
**Misión:** Detectar la carga cognitiva y el impacto emocional en los usuarios de la app Safe-Wallet.

- **Análisis de errores por pantalla:**
  - **Pantalla 2: Trading Saturado**
  
La pantalla de trading de Safe-Wallet presenta demasiada información al mismo tiempo, lo que genera sobrecarga cognitiva en el usuario. Esto dificulta que pueda concentrarse en la decisión principal: comprar o vender una criptomoneda.

En esta pantalla aparecen:
- Gráficos en tiempo real.
- Una lista de aproximadamente 50 criptomonedas.
- Noticias que cambian constantemente.
- Un chat de usuarios activo.

- **Problemas identificados:**
  - **Falta de jerarquía visual:** no existe una organización clara de la información. Todos los elementos parecen tener la misma importancia, por lo que el usuario no sabe en qué debe fijarse primero.
  - **Riesgo de cometer errores:** los botones de “Comprar” y “Vender” tienen el mismo color gris, lo que puede provocar que el usuario realice una acción equivocada al operar.
  - **Estrés en la toma de decisiones:** el exceso de información visual y dinámica genera ansiedad y aumenta la posibilidad de errores.

#### Rol C: Especialista en UI y Jerarquía
**Misión:** Evaluar la jerarquía visual y el affordance.

En la aplicación Safe-Wallet se identifica un problema importante en la pantalla de operaciones, ya que los botones **“Comprar”** y **“Vender”** generan confusión. Ambos presentan un diseño muy similar, especialmente en color y tamaño, lo que dificulta que el usuario los diferencie rápidamente. Esto puede provocar errores en una acción crítica, como comprar cuando en realidad quería vender, afectando la confianza y la experiencia de uso.

Además, la opción de **retirar fondos** se encuentra oculta dentro de varios menús, lo que hace que una función esencial no sea visible ni fácil de encontrar. Esto da la sensación de que la aplicación pone barreras para acceder al dinero del usuario, generando desconfianza.

- **Soluciones propuestas:**
  - Usar colores diferentes y universalmente reconocibles para los botones:
    - **Verde** para comprar.
    - **Rojo** para vender.
  - Agregar íconos y mejorar la ubicación visual de los botones.
  - Ubicar la opción de **retirar fondos** de manera directa en el panel principal.
  - Colocar esta opción junto a acciones como **depositar** o **transferir**, para que sea clara, accesible y transparente para el usuario.

#### Rol D: Oficial de Ética y Fricción
**Misión:** Identificar dark patterns y fricción negativa dentro de la aplicación Safe-Wallet.

En la **pantalla 3**, el problema principal son los **costos ocultos**, ya que el usuario no ve claramente desde el inicio cuánto pagará en total. El valor final incluye comisiones y tasas que aparecen casi al final del proceso y en un texto poco visible, lo que afecta la transparencia y genera desconfianza en una aplicación financiera.

En la **pantalla 5**, se evidencia una estrategia de **manipulación emocional**, porque se utilizan mensajes alarmistas como si el usuario estuviera a punto de perder todo su dinero. Además, se presenta **confirmshaming**, ya que la opción para no continuar hace sentir culpable al usuario. Esto presiona de manera negativa la toma de decisiones y afecta la ética de la plataforma.

En la **pantalla 6**, el dashboard resulta confuso y poco intuitivo, debido a que tiene demasiada información, funciones repetidas, colores mal utilizados, textos poco claros e íconos que no ayudan a entender bien las acciones disponibles. Esto dificulta la navegación y hace que el usuario no identifique rápidamente lo más importante.

- **Soluciones propuestas:**
  - Mostrar un desglose claro de los costos antes de confirmar cualquier compra.
  - Utilizar mensajes neutrales e informativos en lugar de alarmistas.
  - Rediseñar el dashboard con una mejor jerarquía visual.
  - Reducir la saturación de elementos.
  - Usar colores consistentes.
  - Hacer más visibles las opciones principales.

### 3. Entregable de Fase 1

#### Tabla de diagnóstico

| Aspecto | Diagnóstico | Oportunidad de mejora |
|---|---|---|
| Costos ocultos y retiro de fondos oculto | El problema más grave en Safe-Wallet es la presencia de costos ocultos y la dificultad para retirar fondos. Esto genera mucha desconfianza en el usuario, ya que percibe que su dinero no está seguro, por lo tanto no seguirá utilizando la app. | Para evitar esa desconfianza y hacer el proceso más transparente, se debe mejorar el flujo para que sea lógico y accesible, mostrando desde el inicio el desglose completo de costos y ubicando la opción de retirar fondos de forma visible y directa. |

---

## Fase 2: Re-Arquitectura y User Flow en Lucidchart

### 1. El reto de simplificación: “Finanzas con claridad”
[🔗 Ver flujo general en Lucidchart](https://lucid.app/lucidchart/f4541a30-d4fc-468b-8268-a6b27c53f342/edit?viewport_loc=-884%2C-662%2C4988%2C2288%2C0_0&invitationId=inv_cffc7c59-fd8e-4ea0-8f9b-8b8da9f439f7)

### 2. Tareas por Rol en esta Fase

- **Estudiante 1 (Ecosistema):** [🔗 Ver esquema en Lucidchart](https://lucid.app/lucidchart/da588949-1c3d-4186-a9bd-8210c2cc15de/edit?viewport_loc=185%2C339%2C3365%2C1544%2C0_0&invitationId=inv_22fbdec7-51fd-4de8-898b-f2f654a693df)

- **Estudiante 2 (Arquitecto de Información):** [🔗 Ver esquema en Lucidspark](https://lucid.app/lucidspark/6fe8af27-5430-4b27-afa2-3e7909924895/edit?invitationId=inv_4de863c7-cbb4-4901-bb19-78fe46d7b8f3&page=0_0)

- **Estudiante 3 (UX Writer):** [🔗 Ver documento en Lucidchart](https://lucid.app/lucidchart/1662a9b9-232a-42b5-9f1b-b2abcac9e33a/edit?invitationId=inv_94d9f117-8443-4248-906a-9fb3101d1ffc&page=0_0)

- **Estudiante 4 (Validador de Usabilidad):** [🔗 Ver documento en Lucidchart](https://lucid.app/lucidchart/407baf6f-ec61-43fa-b211-7569cd841190/edit?viewport_loc=-183%2C-229%2C3573%2C1974%2C0_0&invitationId=inv_953876ba-2816-4626-a0cb-f8a402e93494)

### 3. Entregable de Fase 2

En el siguiente enlace se encuentra el diagrama de flujo que representa el funcionamiento actual de la app:  
[🔗 Ver flujo actual](https://lucid.app/lucidchart/70081b15-95bf-4732-9a32-ffb2bc03de56/edit?invitationId=inv_7ec24e62-7142-41ac-90ff-3d8103c5f8f3&page=0_0#)

En el siguiente enlace se encuentra el diagrama de flujo que representa el funcionamiento correcto de la app, creado con el fin de solucionar los errores que actualmente presenta:  
[🔗 Ver flujo propuesto](https://lucid.app/lucidchart/79c4772a-cb36-4e22-a9ea-4399ed4ffd98/edit?invitationId=inv_50c590bd-d33b-4a1f-8aa3-5b81689be37c&page=0_0#)

---

## Fase 3: Prototipado de Media Fidelidad (Wireframes)

[🔗 Ver prototipo en Figma](https://www.figma.com/design/2cDx3ToZ6Pl12HhILkbTQU/Ecocanje?node-id=0-1&t=77TC2K6Nf5RZq3pt-1)
