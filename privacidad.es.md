# Política de privacidad de Zprium

**Última actualización:** 22 de noviembre de 2026

## 1. Quién es el responsable

Zprium es un bot de Discord operado por **Isaac Dereck Lizana Correa (Dereck Lizana)**, con domicilio en **Italia** ("nosotros").
- Contacto sobre privacidad: **zprium.support@gmail.com**.
- Servidor de soporte: **https://discord.gg/HcfkxN7TcH**.

Zprium funciona en hardware propio del responsable ubicado en **Italia**. La base de datos, la caché y los modelos de inteligencia artificial se ejecutan en ese equipo. No usamos proveedores de IA en la nube.

## 2. A quién se aplica

Se aplica a:
- los miembros de los servidores de Discord donde está Zprium;
- los administradores que lo configuran, en Discord o en su consola web.

Zprium trata datos solo en los servidores donde un administrador lo añadió. Cada servidor decide qué módulos activa: **fuera del núcleo, todos vienen desactivados**.

## 3. Qué datos tratamos, para qué y durante cuánto tiempo

**No leemos el contenido de tus mensajes.** Zprium no pide a Discord el permiso de contenido de mensajes. Solo ve el texto cuando:
- mencionas al bot;
- usas un comando;
- respondes a un formulario de Zprium, como un reto de verificación o una apelación;
- aplicas sobre un mensaje la acción "Resumir".

No guardamos ese texto, salvo en tres casos que explicamos abajo: la conversación con `/ai ask` (30 minutos), las preguntas que la base de conocimiento no supo responder (sin quién las hizo) y lo que tú decides guardar en tu memoria con la IA.

| Datos | Para qué | Base jurídica | Cuánto tiempo |
| :--- | :--- | :--- | :--- |
| Identificador, nombre e idioma del servidor | Saber dónde está Zprium y en qué idioma responder | Prestación del servicio | Hasta 30 días después de que el bot salga del servidor |
| Qué módulos activó el servidor y su configuración, con el identificador del administrador que la cambió | Aplicar la configuración que eligió el servidor | Prestación del servicio | Igual que el anterior |
| Registro de seguridad (identificadores de quien hace y de quien recibe una acción, la acción y sus detalles; en una cuarentena, los roles retirados para poder devolverlos) | Detectar y registrar ataques (borrados masivos, raids) y las acciones de administración, en un registro a prueba de manipulación | Interés legítimo (seguridad) | **Hoy sin borrado automático.** Desde la versión 8.0.6, los registros nuevos guardan un seudónimo en lugar de tu identificador, y el olvido se hace destruyendo la llave de ese seudónimo (ver §6). El archivo de los registros de más de 12 meses llegará más adelante. Hasta entonces atendemos las solicitudes a mano |
| Casos de moderación, si el servidor activa el módulo de moderación. Cada caso guarda: la acción (aviso, nota, aislamiento, expulsión o baneo), un **seudónimo** de la persona afectada y otro del moderador (nunca el identificador de Discord de ninguno de los dos), el motivo que escribe el moderador, la duración, la fecha y si el caso se anuló. También se registran como casos los aislamientos, las expulsiones y los baneos que el staff hace desde Discord, los aislamientos que pone el AutoMod de Discord, y las cuarentenas y expulsiones que hace Aegis, la protección de Zprium contra ataques. Los casos de Aegis llevan un motivo fijo (el tipo de ataque y cuántas acciones hubo) y no se pueden apelar: los revisa el staff del servidor | Que el staff del servidor lleve un historial de moderación y que cada acción quede registrada y se pueda comprobar | Interés legítimo (seguridad y convivencia del servidor) | **24 meses** desde el caso; después se borra solo. También se borra si el bot sale del servidor (30 días) |
| Apelaciones de casos de moderación, si el servidor las activa. Cada apelación guarda: su estado (pendiente, aceptada o rechazada), las fechas, un **seudónimo** tuyo y otro de quien la decidió (nunca el identificador de Discord de ninguno de los dos) y la respuesta del staff, si escribe una. **El texto de tu apelación no lo guardamos:** se publica en el canal de apelaciones del servidor | Que puedas pedir al staff que revise un caso, y que su decisión quede registrada | Interés legítimo (seguridad y convivencia del servidor, y que puedas defenderte de una sanción) | Lo mismo que su caso: **24 meses** desde el caso, y se borra con él. También se borra si el bot sale del servidor (30 días). Lo publicado en el canal queda allí mientras su staff lo conserve |
| Strikes de AutoMod, si el servidor activa el módulo. Cada strike guarda: un **seudónimo** tuyo (nunca tu identificador de Discord), si viene de AutoMod de Discord o de una regla de Zprium, el tipo de regla, la hora y, si viene de Discord, el número de su entrada en el registro de auditoría del servidor. **Nunca el texto del mensaje** (Zprium no lo recibe), ni el canal, ni el nombre de la regla | Aislar de forma automática a quien incumple repetidamente las reglas del servidor | Interés legítimo (seguridad y convivencia del servidor) | **30 días**. También se borran si el bot sale del servidor (30 días) |
| Verificación, si el servidor la activa. Mientras respondes un reto, Zprium guarda el servidor, tu identificador, el tipo de reto y una huella de las respuestas válidas (**nunca lo que escribes**), y cuántas veces fallaste. Cuando te verificas, guarda la fecha y una fila en el registro de seguridad con un **seudónimo** tuyo, el rol que recibiste y el tipo de reto. Si agotas los intentos, otra fila igual, con los intentos y la espera. Si el servidor pone una edad mínima, la edad de tu cuenta se calcula desde tu identificador, sin guardar nada. Si activa la expulsión de quien no se verifica, Zprium guarda un trabajo programado con tu identificador y la fecha en que entraste y, si te expulsa, otra fila con tu **seudónimo** y el plazo. Durante un ataque de altas masivas, guarda solo que el servidor está bajo ataque, sin ningún dato tuyo | Que el servidor deje entrar solo a personas, sin salir de Discord | Interés legítimo (seguridad del servidor) | El reto, **10 minutos**, y se borra al responderlo. Los fallos, la espera que elige el staff tras el último (**24 horas** como mucho). La fecha, como el estado de cada miembro: hasta 30 días después de salir del servidor. Las filas del registro de seguridad, como ese registro (§6). El trabajo de la expulsión, hasta que vence el plazo y 30 días más. El aviso del ataque, lo que dura (**24 horas** como mucho) |
| Roles automáticos, si el servidor activa el módulo. Si hay un retraso o hay que reintentar, un trabajo programado con tu identificador y la fecha en que entraste. Por cada rol, filas del registro de seguridad con un **seudónimo** tuyo, la fecha en que entraste y el rol: que Zprium iba a dártelo, que Discord lo aceptó o que ya lo tenías sin poder confirmar quién lo puso | Darte los roles que eligió el servidor y poder comprobar después qué hizo Zprium | Prestación del servicio (el trabajo programado). Interés legítimo (seguridad y funcionamiento del servidor) para las filas del registro | El trabajo: 30 días después de terminar. Las filas: como el resto del registro de seguridad (§6) |
| Bienvenidas, si el servidor activa el módulo. Durante 24 horas como mucho, y solo en la memoria del proceso, tu identificador y la hora en que entraste, para no darte la bienvenida dos veces | Darte la bienvenida una sola vez y, si el servidor lo elige, despedirte o enviarte un mensaje directo | Interés legítimo (acoger a quien entra y el funcionamiento del servidor) | 24 horas, o hasta que Zprium se reinicie. Los mensajes publicados los guarda Discord |
| Economía, si el servidor activa el módulo: tu saldo de monedas virtuales, la fecha de tu última recompensa diaria, el historial de tus movimientos (recompensas, envíos, compras, premios de juegos y recompensas de nivel, con el otro miembro cuando lo hay) y tus artículos de la tienda | Que puedas ganar, enviar y gastar monedas en ese servidor sin que nada se pierda ni se cobre dos veces | Prestación del servicio | Mientras el servidor use Zprium; se borra con tu solicitud de supresión o al purgar el servidor |
| Niveles, si el servidor activa el módulo: tu XP y tu nivel en ese servidor, cuántos de tus mensajes dieron XP, la hora del último y el XP de ese día | Que veas tu progreso con `/profile` y la clasificación con `/levels leaderboard` | Prestación del servicio | Mientras el servidor use Zprium, aunque desactive el módulo; se borra con tu solicitud de supresión o al purgar el servidor |
| Sorteos, si el servidor activa el módulo: si participas en un sorteo y cuándo; si ganas, que ganaste; si lo organizas, que lo empezaste | Que puedas participar y retirarte, y que el resultado se pueda reproducir | Prestación del servicio | Mientras el servidor use Zprium; se borra con tu solicitud de supresión o al purgar el servidor (ver los límites en el §6) |
| Tickets de soporte, si el servidor activa el módulo: que abriste un ticket, su número, su tema (soporte, reporte u otro), su hilo, su estado y quién del staff lo tomó o lo cerró. **Nunca el asunto, la descripción ni los mensajes** | Que el staff del servidor pueda atenderte en privado y saber qué tickets siguen abiertos | Prestación del servicio | Mientras el servidor use Zprium; se borra con tu solicitud de supresión o al purgar el servidor |
| Registros del servidor, si el servidor activa el módulo de registros. Zprium publica en los canales que elige el staff: entradas y salidas de miembros (con la fecha de creación de la cuenta), cuándo un miembro se verifica o agota los intentos de verificación (con el tipo de reto, **nunca la respuesta**), cuándo la verificación expulsa a quien no se verificó a tiempo (con el plazo, **nunca un motivo**), mensajes borrados o editados (autor, canal y hora; **nunca el texto**), entradas y salidas de los canales de voz, canales y roles creados, cambiados o borrados (y quién lo hizo), reglas de AutoMod creadas, cambiadas o borradas (su nombre y quién lo hizo, nunca sus palabras), los casos de moderación y, si el servidor activa AutoMod, sus strikes | Que el staff del servidor vea lo que pasa en él y pueda moderarlo | Interés legítimo (seguridad y convivencia del servidor) | **Zprium no los guarda:** cada evento espera en memoria como mucho 15 minutos hasta que se publica, y se pierde si el bot se reinicia. Lo publicado queda en el canal del servidor mientras su staff lo conserve |
| Registro de eventos (identificadores en los eventos del servidor, sin texto de mensajes) | Recuperación ante fallos y análisis de seguridad | Interés legítimo | 30 días |
| Automatizaciones del servidor (Z-Flow): definiciones, ejecuciones (solo metadatos, nunca el texto) y fallos | Ejecutar las automatizaciones que crea el servidor | Prestación del servicio | Ejecuciones: 90 días. Fallos resueltos: 30 días. Definiciones: hasta la purga del servidor |
| Equipos, alineaciones y resultados de scrims (esports) | Organizar partidas del servidor | Prestación del servicio | Hasta la purga del servidor |
| Base de conocimiento del servidor: textos que el responsable o el staff revisan y añaden, con su fuente, sus fechas y sus vectores | Responder preguntas con IA local, citando de dónde sale cada respuesta | Prestación del servicio | Hasta que se sustituyen o se borran, o se purga el servidor |
| Tu conversación con `/ai ask`: tus preguntas y las respuestas (como mucho 20 mensajes) | Que la IA tenga en cuenta lo que acabas de preguntar | Prestación del servicio | **30 minutos** desde tu última pregunta; después desaparece sola |
| Preguntas que la base de conocimiento no supo responder: el texto de la pregunta **sin quién la hizo**, quitando identificadores, correos, teléfonos y otros datos; si toca salud, religión u otros datos especiales, solo de qué tipo era | Saber qué falta en la base de conocimiento | Interés legítimo (mejorar el servicio) | **180 días** desde la última vez que alguien la hizo |
| Notas del staff de `/ai memory`: el texto de la nota y quién la guardó | Dar a la IA contexto del servidor | Interés legítimo (funcionamiento del servidor) | Hasta que el staff la borra o se purga el servidor |
| **Tu memoria con la IA, solo si la activas** con `/ai mydata`: lo que pides guardar (preferencias, contexto, notas para más adelante), con su tipo y versión, y tu consentimiento | Recordar lo que tú le pides | **Tu consentimiento**, que puedes retirar cuando quieras | Hasta que la borres o retires el consentimiento; si no la vuelves a guardar, **365 días** (180 los resúmenes). Un consentimiento retirado se borra a los **30 días** |
| Propuestas, avisos y trabajos del motor autónomo | Operaciones automáticas que el servidor activó | Interés legítimo | 90 días desde que terminan; las pendientes se conservan hasta que se deciden o caducan |
| Estado de cada miembro en el servidor (identificador y datos de los módulos que lo usan) | Moderación y funciones del servidor | Interés legítimo | Mientras sea miembro; se borra 30 días después de salir del servidor (si vuelve antes, se conserva) |
| Trabajos programados (por ejemplo, recordatorios); pueden incluir el identificador del miembro afectado | Hacer más tarde lo que el servidor pidió | Prestación del servicio | 30 días después de terminar |
| Sesión en la consola web (identificador y nombre de Discord, lista de servidores) | Iniciar sesión en la consola | Prestación del servicio | 8 horas, o hasta cerrar sesión |
| Respuestas de IA en caché | Evitar repetir cálculos | Prestación del servicio | 30 minutos |

**Avisos de moderación.** Si un moderador te avisa, te aísla o te expulsa con Zprium, el servidor puede enviarte un mensaje privado con la acción, el motivo y la duración. El mensaje **nunca dice quién lo hizo**. Las notas internas del staff no se te envían. Estos avisos están activados por defecto y cada servidor puede desactivarlos.

**Apelaciones.** Si el servidor tiene activadas las apelaciones, el mensaje privado que te avisa de un aviso, un aislamiento o una expulsión incluye un botón para apelar durante **14 días**.
- Escribes por qué crees que el caso debe revisarse.
- Zprium lo publica en un canal privado del staff del servidor, junto a tu nombre de Discord y el caso. No guarda ese texto: tú conservas una copia en el mensaje privado.
- El staff decide. Te lo comunicamos por mensaje privado, **sin decir quién lo decidió**, y con el mismo botón puedes consultar el estado cuando quieras.
- Puedes apelar cada caso **una vez**, y como mucho **3 casos cada 30 días** en cada servidor.
- Las notas internas del staff no se pueden apelar, porque nunca se te envían.

**AutoMod.** Si el servidor activa el módulo AutoMod de Zprium:
- Cuando AutoMod de Discord bloquea un mensaje tuyo, Zprium lo sabe por el registro de auditoría del servidor: quién, cuándo y qué tipo de regla. **Nunca qué decía el mensaje.**
- Zprium también cuenta, sin leerlos, cuántos mensajes envías en pocos segundos y cuántas personas o roles mencionas en un mensaje. Esos recuentos duran menos de un minuto y no se guardan.
- Cada uno de esos hechos es un **strike**. Si acumulas varios en poco tiempo, Zprium te **aísla** un rato de forma automática. Por defecto: 3 en una hora, 10 minutos; 5 en un día, una hora; 8 en una semana, un día. Cada servidor puede cambiar estos valores.
- El aislamiento abre un caso de moderación. Como con cualquier aislamiento, te lo avisamos por mensaje privado y **puedes apelarlo**, si el servidor tiene activados los avisos y las apelaciones.
- Si el servidor tiene registros de moderación, cada strike aparece en su canal de registros: quién, el canal y el tipo de regla, nunca el texto. También aparecen los mensajes que AutoMod de Discord marca para el staff y los perfiles que pone en cuarentena, con el nombre de la regla.
- Si el servidor lo activa, Zprium también crea y mantiene reglas de AutoMod de Discord por encargo de su staff (invitaciones, enlaces, palabras y otras). Las palabras de esas reglas se guardan en Discord, no en Zprium: Zprium solo guarda qué regla es suya, una huella para saber si alguien la cambió y la fecha.
- El AutoMod de Zprium nunca expulsa ni banea a nadie.
- Los strikes y los aislamientos automáticos de Zprium no se aplican al staff del servidor.

**Aegis.**
- Si el servidor tiene un canal de registros, cuando Aegis detecta un ataque publica en él qué hizo y menciona a la persona a la que lo atribuye. En modo vigilar no hace nada: publica lo que habría hecho en modo aplicar, salvo que el staff desactive esos informes.
- Durante un ataque de altas masivas, si el staff lo activa, Aegis puede subir el nivel de verificación del servidor y activar una regla de AutoMod de Discord que compara tu nombre y tu apodo con palabras que elige el staff. La comparación la hace Discord: Zprium no lee ni guarda tu perfil. El nivel y la regla vuelven a su estado pasado el tiempo que elige el staff; si la regla te bloqueó, vuelves a poder interactuar cambiando tu nombre o tu apodo.

**Verificación.** Si el servidor activa la verificación de Zprium:
- Para ver el resto del servidor, pulsas «Verificarme» y respondes un reto corto: un botón, elegir un emoji, una operación o una pregunta del staff. Todo pasa dentro de Discord: **sin páginas web, sin captchas de terceros y sin registrar tu dirección IP**.
- Al pulsar, Zprium mira lo que Discord le envía con tu pulsación (tus roles, si aceptaste las reglas del servidor, si estás aislado y si AutoMod bloqueó tu nombre), y no lo guarda.
- Si respondes bien, Zprium te da el rol que elige el staff. Si fallas varias veces, esperas el tiempo que elige el staff antes de volver a intentarlo.
- Si el servidor pone una edad mínima, una cuenta más nueva no puede verificarse hasta cumplirla, y Zprium te dice desde qué día podrás. La edad sale de tu identificador de Discord: Zprium no guarda nada nuevo.
- Durante un ataque de altas masivas que detecte Aegis, el reto es más difícil hasta que pasa el tiempo que elige el staff: una operación (o la pregunta del staff), **un solo intento** y cuentas de **7 días** como poco.
- Si el servidor lo activa, Zprium expulsa a quien no se verifica en el plazo que elige el staff (**24 horas** por defecto). Antes te lo dice por mensaje privado, si los tienes abiertos. **No es una sanción ni un caso de moderación**: puedes volver a entrar cuando quieras. Nunca expulsa al staff, a quien ya se verificó ni a quien el staff retiene (en cuarentena o aislado), y si Zprium estuvo caído, el plazo cuenta desde que volvió. Discord guarda en el registro de auditoría del servidor que Zprium te expulsó.
- Tu respuesta se compara con las válidas y se descarta: Zprium nunca la guarda ni la publica.
- Discord guarda en el registro de auditoría del servidor que Zprium te dio el rol.

**Roles automáticos.** Si el servidor activa el módulo, Zprium te da los roles que eligió el staff cuando entras (como mucho 10).
- Solo **añade** roles: nunca te quita ninguno, tampoco los que ya tenías.
- Espera a que termines el screening de Discord y, si el servidor tiene la verificación de Zprium, a que la pases (salvo que el staff elija darlos al entrar).
- Durante un ataque de altas masivas que detecte Aegis, espera a que termine.
- Nunca da un rol con permisos de staff ni da roles a quien ya estaba en el servidor cuando se activó.
- Si el staff te quita un rol que Zprium te dio, Zprium no vuelve a dártelo mientras sigas en el servidor; si sales y vuelves, es una entrada nueva.
- Discord guarda en su registro de auditoría que Zprium te dio el rol, con el motivo «Zprium: roles automáticos».

**Bienvenidas.** Si el servidor activa el módulo, Zprium publica un mensaje de bienvenida cuando entras, en el canal que eligió el staff.
- El texto lo redacta el staff de cada servidor; Zprium solo sustituye las variables y limita las menciones. El contenido es responsabilidad del servidor.
- El mensaje solo te menciona a ti: nunca a @everyone, a @here ni a un rol, diga lo que diga el texto del staff. Tu nombre aparece como texto, sin formato.
- Espera a que termines el screening de Discord y, si el servidor tiene la verificación de Zprium, a que la pases (salvo que el staff elija darla al entrar).
- Durante un ataque de altas masivas que detecte Aegis no publica bienvenidas, y fuera de él publica como mucho 5 por minuto en cada servidor.
- Si el servidor lo activa, te envía también un mensaje directo con un enlace al canal de guía y otro a esta política. El servidor decide si se envía el MD; el staff puede desactivarlo en cualquier momento. Es un único mensaje y no se reintenta: si tienes los MD cerrados, no se envía nada más.
- Si el servidor activa la despedida, al irte publica tu nombre, sin mencionarte y sin decir por qué te fuiste. Solo lo hace si ya habías terminado la entrada (screening o verificación); si Zprium no puede saberlo, no publica nada. El servidor puede desactivar la despedida, y recomendamos a su staff anunciarla en las normas del servidor.

**Economía.** Las monedas son virtuales: no valen dinero real ni se pueden cambiar por él. Cada servidor tiene las suyas y nada se mezcla entre servidores. El servidor puede ver la clasificación de saldos con `/economy leaderboard`, que muestra tu nombre y tu saldo.

**Niveles.** Si el servidor activa el módulo de niveles:
- Cada vez que envías un mensaje, Discord se lo comunica a Zprium. Para el XP, Zprium solo usa **quién** lo envió, **en qué servidor** y **cuándo**: no analiza ni guarda su texto. Los mensajes de bots, de webhooks y del sistema no cuentan.
- Un mensaje da entre 15 y 25 XP, como mucho uno por minuto y hasta 500 XP al día (hora UTC). El staff del servidor puede cambiar esos valores con `/config` y apagar el módulo cuando quiera.
- Solo cuentan los mensajes enviados después de activar el módulo.
- Cualquier miembro del servidor puede ver tu nivel, tu XP y tu puesto con `/profile` o en `/levels leaderboard` (los 10 primeros). Si el servidor usa la economía, `/profile` muestra también tus monedas e insignias. Esas respuestas solo las ve quien pregunta y no notifican a nadie.
- Cada servidor tiene sus propios niveles: nada se mezcla entre servidores.
- Apagar el módulo deja de sumar XP, pero no borra el que ya tenías: si se vuelve a activar, sigue ahí. Se borra con tu solicitud de supresión o al purgar el servidor.
- Si el staff configura recompensas, al alcanzar un nivel puedes recibir un rol (nunca uno con permisos de staff) o monedas de la economía del servidor, **una sola vez por nivel**. El rol queda en el registro de auditoría de Discord con el motivo «Zprium: level N reward» y en nuestro registro de seguridad; las monedas, en el historial de movimientos de la economía.
- Si el staff elige un canal de anuncios, Zprium publica allí «🎉 [tu nombre] llegó al nivel N», **sin notificarte**. Sin canal elegido (lo normal), no se anuncia nada.

**Sorteos.** Si el servidor activa el módulo de sorteos:
- Participas pulsando «Participar» y puedes retirarte mientras siga abierto. Zprium guarda que participaste y cuándo; no guarda ningún mensaje tuyo. Solo cuenta una participación por persona.
- **Lo que se publica.** El resultado se publica en el canal del sorteo, que puede ser público: los ganadores aparecen **mencionados** (solo a ellos se les notifica), con el número de participantes, la semilla del sorteo y un resumen SHA-256 de la lista de identificadores de Discord de quienes seguían en el servidor al cerrar. La lista en sí no se publica.
- **El resumen no es anónimo.** Es un SHA-256 sin sal de identificadores de Discord, que no son secretos. Quien conozca a los posibles participantes (por ejemplo, en un servidor pequeño) puede probar listas hasta dar con la que coincide y saber así quién participó. No prometemos que ese resumen no pueda relacionarse contigo.
- **Qué se puede comprobar y qué no.** Al empezar se publica el SHA-256 de una semilla secreta. Al cerrar, cualquiera puede comprobar que la semilla revelada es la comprometida y, **si conoce la lista exacta de participantes elegibles**, recalcular los ganadores con el algoritmo publicado (HMAC-SHA256 de la semilla con cada identificador). Esto no demuestra que la lista incluyera a todos los participantes elegibles, ni que Zprium no conociera su propia semilla: la genera el bot.
- Los sorteos no admiten pagos ni apuestas. El premio lo describe y lo entrega el staff del servidor, no Zprium.

**Tickets.** Si el servidor activa el módulo de tickets:
- Abres un ticket desde el panel del servidor rellenando un formulario. Zprium crea un **hilo privado**, te añade y publica allí tu asunto y tu descripción una sola vez. En un canal privado del staff publica un aviso con el número del ticket, su tema y tu nombre, sin lo que escribiste. **Zprium no guarda lo que escribiste**: queda solo como mensaje en el hilo de Discord, y no desaparece de Discord porque Zprium no lo guarde.
- Ven el hilo tú, las personas del staff que se unen a él, la persona dueña del servidor y quien tenga en ese canal el permiso de Discord «Gestionar hilos» o de administrador, aunque no atienda tickets, **incluidos otros bots** que el servidor haya instalado con ese permiso. Eso lo decide Discord con los permisos del servidor. Zprium no menciona a nadie dentro del hilo y anula las menciones que escribas, para que no se pueda añadir a otras personas por ese camino.
- Zprium guarda solo los datos del ticket: número, tema, hilo, estado, quién lo abrió y quién lo tomó o lo cerró. Puedes tener **un ticket abierto por servidor**.
- Al cerrarlo, el hilo se bloquea y se archiva; sus mensajes siguen en Discord. El staff puede reabrirlo.
- Zprium **no transcribe ni archiva** las conversaciones de los tickets y no las usa con la IA.

**Música.** Mientras suena música en un canal de voz, Zprium guarda en memoria el canal y quién pidió cada canción, para la cola y sus controles. Se borra al vaciarse el canal, con `/music leave` o al reiniciarse el bot. Las canciones descargadas se guardan en el servidor de Zprium como copia local, sin ningún dato tuyo, y se borran a los 30 días sin reproducirse.

**Registros del servidor.** Si el servidor activa el módulo de registros, Zprium publica en un canal del staff cuándo entras o sales del servidor, cuándo te verificas o agotas los intentos de verificación, cuándo la verificación te expulsa por no verificarte a tiempo, cuándo entras o sales de un canal de voz y cuándo se borra o se edita un mensaje tuyo. De un mensaje solo indica el autor, el canal y la hora: **nunca su texto**, que Zprium no lee. Si el mensaje no estaba en la memoria del bot, ni siquiera el autor. Zprium no informa de nada que pase en un canal que Discord le oculta, y sus publicaciones no notifican a nadie. Esos registros los lee el staff del servidor, que los guarda o los borra como cualquier otro mensaje de su servidor. Zprium no conserva copia.

**Lista completa, generada desde el código:** [datos por módulo](https://izkron.github.io/zprium-legal/privacidad-datos-por-modulo.html).

**Inteligencia artificial:**
- La IA de Zprium (resúmenes, preguntas a la base de conocimiento) funciona **solo en nuestro equipo**, con modelos locales.
- Ningún texto sale hacia servicios de IA de terceros.
- No usamos tus datos para entrenar modelos.
- Las respuestas generadas por IA se identifican como tales.
- **Tu memoria con la IA** está desactivada hasta que la activas tú con `/ai mydata`. Antes de guardar algo, Zprium comprueba el texto y rechaza lo que parece un secreto o un identificador, datos de salud, religión, opiniones políticas, orientación sexual, origen étnico, afiliación sindical, datos genéticos o biométricos, o dificultades económicas. La comprobación es automática y puede no detectarlo todo: no escribas datos de ese tipo.
- La IA solo usa tu memoria en respuestas que **ves solo tú**. Nunca en un mensaje de un canal.
- No deducimos nada de ti: la IA solo guarda lo que tú le pides guardar.

**No hacemos:**
- publicidad ni venta de datos;
- perfiles entre servidores;
- registro de direcciones IP de los miembros;
- lectura del estado de presencia.

## 4. Con quién compartimos datos

- **Discord Inc.:** Zprium funciona dentro de Discord, y lo que el bot publica lo trata Discord según su propia política de privacidad.
- **Cloudflare, Inc.**, cuando la consola web se publique en Internet: el tráfico de la consola pasa por su red (túnel y protección frente a ataques). Cloudflare actúa como encargado del tratamiento.
- **Copias de seguridad fuera del equipo principal:** se cifran en nuestro equipo **antes** de salir de él, con una clave que solo tiene el responsable. Nadie más puede leerlas, tampoco los proveedores que las guardan. Se guardan en:
  - otro equipo del responsable, en Italia;
  - **Google Drive (Google Ireland Limited)**, como simple almacenamiento;
  - **Cloudflare R2**, en la Unión Europea, hasta que lo retiremos.

  Ninguna copia se conserva más de **35 días**.
- **Nadie más.** No hay otros destinatarios, salvo obligación legal.

**Transferencias internacionales:**
- Discord y Cloudflare pueden tratar datos fuera del Espacio Económico Europeo, con las garantías que ofrecen (cláusulas contractuales tipo). Google puede guardar las copias cifradas fuera del EEE, con esas mismas garantías.
- Nosotros almacenamos los datos en **Italia**. Las copias de seguridad cifradas también están en los proveedores indicados arriba.

## 5. Seguridad

Aplicamos estas medidas:
- sin puertos de base de datos expuestos;
- secretos fuera del código;
- sesiones de la consola en el servidor, que caducan;
- permisos de la consola calculados en el servidor para cada petición;
- registro de seguridad inmutable, protegido con una cadena de hashes;
- purga automática de los datos de un servidor 30 días después de que el bot salga de él;
- copias de seguridad cifradas con `age`, conservadas 35 días como máximo, con una restauración de prueba automática cada semana.

## 6. Tus derechos

**Qué puedes pedir:**
- acceso a tus datos;
- rectificación;
- supresión;
- limitación del tratamiento;
- oposición;
- portabilidad.

**Cómo pedirlo:** escribe a **zprium.support@gmail.com** o abre un ticket en **el servidor de soporte (https://discord.gg/HcfkxN7TcH)**, indicando tu identificador de usuario de Discord. Te pediremos que confirmes que la cuenta es tuya desde Discord.

**Plazos y alcance:**
- Respondemos en **un mes como máximo**.
- Las solicitudes las atiende y ejecuta **solo el responsable**, después de comprobar que la cuenta es tuya. Te avisamos cuando esté hecho.
- En el registro de seguridad no se borran filas, porque el registro es inmutable. Lo que se destruye es la llave de tu seudónimo, y a partir de ese momento las filas ya no se pueden relacionar contigo. El olvido es completo cuando rotan las copias de seguridad que aún contienen esa llave, en 35 días como máximo. Podemos conservar lo imprescindible para la seguridad del servicio (art. 17.3 RGPD).
- **Casos de moderación.** Funcionan como el registro de seguridad: guardan un seudónimo, no tu identificador. Al atender tu solicitud de supresión destruimos la llave de ese seudónimo, y desde ese momento tus casos ya no se pueden relacionar contigo. El caso en sí (la acción y su fecha) se conserva hasta que cumple 24 meses, por el interés legítimo del servidor en su historial (art. 17.3 RGPD).
  - El motivo es texto libre. Si un moderador escribió en él tu nombre sin mencionarte, ese nombre puede seguir en el texto: dínoslo en la solicitud y lo revisamos a mano.
  - Un moderador no puede borrar un caso, solo anularlo indicando por qué.
- **Apelaciones.** Funcionan como los casos: guardan seudónimos, y al atender tu solicitud de supresión destruimos su llave, así que tus apelaciones ya no se pueden relacionar contigo. Se borran con su caso.
  - El texto de tu apelación no está en nuestros sistemas, sino en el canal de apelaciones del servidor. Para que se borre, pídeselo a su staff; si no te atienden, escríbenos y lo comunicamos al servidor.
  - La respuesta del staff es texto libre. Si alguien del staff escribió en ella tu nombre sin mencionarte, ese nombre puede seguir en el texto: dínoslo en la solicitud y lo revisamos a mano.
- **Strikes de AutoMod.** Guardan seudónimos, como los casos. Pero los que vienen de AutoMod de Discord guardan también el número de su entrada en el registro de auditoría del servidor, donde Discord sí muestra quién fue. Por eso, al atender tu solicitud de supresión **borramos tus strikes**, además de destruir tu llave. Si no, se borran a los 30 días.
- **Registros del servidor.** Zprium no guarda los registros que publica, así que no hay nada que borrar en nuestros sistemas. Las publicaciones están en el canal del servidor: para que se borre una, pídeselo a su staff. Si no te atienden, escríbenos y lo comunicamos al servidor.
- **Verificación.** El reto y los fallos caducan solos: en 10 minutos y en 24 horas como mucho. La fecha de tu verificación se borra a los 30 días de salir del servidor, o al atender tu solicitud de supresión. Las filas del registro de seguridad funcionan como el resto: guardan un seudónimo, y al atender tu solicitud de supresión destruimos su llave. El trabajo programado de la expulsión se borra a los 30 días de terminar, como el resto de los trabajos programados.
- **Roles automáticos.** Las filas del registro de seguridad funcionan como el resto: guardan un seudónimo, y al atender tu solicitud de supresión destruimos su llave. Al atender tu solicitud de supresión borramos también los trabajos programados que iban a darte un rol, y ninguno puede volver a actuar sobre esa entrada, tampoco si restauramos una copia de seguridad. Si uno estaba en marcha en ese momento, se detiene antes de su siguiente paso; lo que Discord ya hubiera hecho (un rol ya dado) no lo deshace la supresión: pídeselo al staff del servidor. Si vuelves a entrar después, es una entrada nueva. El registro de auditoría de Discord lo gestionan Discord y el servidor. Si no quieres roles automáticos, pídeselo al staff del servidor, que puede quitarte el rol (Zprium no te lo vuelve a dar en esa entrada) o desactivar el módulo.
- **Bienvenidas.** Zprium no guarda en disco nada tuyo por este módulo. Recuerda en memoria, como mucho 24 horas, que tu entrada ya recibió la bienvenida, y lo olvida al reiniciarse. Si pides la supresión de tus datos, Zprium no publica bienvenidas ni despedidas sobre ti desde esa fecha. Los mensajes ya publicados en Discord los puede borrar el staff del servidor o tú, según los permisos de Discord.
- **Economía.** Al atender tu solicitud de supresión borramos tu saldo, tus artículos y tus movimientos en todos los servidores; en los movimientos de otros miembros contigo, quitamos tu identificador.
- **Niveles.** Al atender tu solicitud de supresión borramos tu XP y tu nivel en todos los servidores, y no vuelven aunque restauremos una copia de seguridad.
- **Sorteos.** Al atender tu solicitud de supresión borramos tus participaciones en todos los servidores, te quitamos de la lista de ganadores y quitamos tu identificador de los sorteos que organizaste, y no vuelve aunque restauremos una copia de seguridad. **Lo que no podemos borrar desde Zprium:** el resumen de participantes de un sorteo ya cerrado se queda como está y se calculó con tu identificador si participaste, así que podría seguir sirviendo para comprobar que participaste; y los mensajes con el resultado que te mencionan están en el canal del servidor, en Discord: para que se borre uno, pídeselo a su staff.
- **Tickets.** Al atender tu solicitud de supresión **borramos los tickets que abriste** y quitamos tu nombre de los que tomaste o cerraste como staff; tampoco vuelven si restauramos una copia de seguridad. **No borramos los hilos, los mensajes ni los avisos del canal del staff en Discord**, que son del servidor: pídeselo a su staff. Las filas del registro de seguridad sobre tus tickets (abrir, tomar, unirse, cerrar, reabrir) guardan un seudónimo, el número del ticket, su tema y su hilo, nunca lo que escribiste; al suprimir destruimos la llave de ese seudónimo.
- **Tu memoria con la IA.** Con `/ai mydata` puedes:
  - verla;
  - exportarla en un archivo;
  - corregirla, guardando de nuevo la misma clave;
  - borrar una nota o todo, y retirar tu consentimiento, lo que la borra al momento.

  Cada una de esas acciones queda en el registro de seguridad, sin el contenido. Si nos pides la supresión, la borramos en todos los servidores y quitamos tu nombre de las notas del staff que guardaste, y no vuelve aunque restauremos una copia. El borrado es completo cuando rotan las copias de seguridad, en 35 días como máximo.
- **Conversación de `/ai ask` y preguntas sin respuesta.** La conversación desaparece sola a los 30 minutos. Las preguntas sin respuesta no guardan quién las hizo, así que no podemos encontrarlas por tu identificador. Si escribiste en una algo que te identifica, dínoslo y la revisamos a mano.
- **Lista de olvidos.** Para que restaurar una copia de seguridad no pueda deshacer tu olvido, guardamos una lista mínima con tres datos:
  - una huella de tu identificador (HMAC-SHA256), calculada con una clave que se guarda fuera de la base de datos. Nunca tu identificador en claro, y sin esa clave la huella no se puede relacionar contigo;
  - la fecha del olvido;
  - quién lo ejecutó.

  Después de **cualquier** restauración de una copia, y antes de que el bot vuelva a arrancar, se vuelven a aplicar todos los olvidos de la lista: se destruyen otra vez las llaves, los datos de miembro y los strikes de AutoMod anteriores a cada olvido. Si vuelves a usar el bot después del olvido, empiezas de cero y la lista no afecta a tus datos nuevos. La lista se conserva mientras exista el servicio, porque es lo que impide que el olvido se deshaga y lo que demuestra que atendimos tu solicitud.
- Los administradores pueden borrar todos los datos de su servidor sacando al bot: se eliminan a los 30 días.

**Reclamaciones:** también puedes reclamar ante la autoridad de protección de datos de tu país. En **Italia** es el **Garante per la protezione dei dati personali** (https://www.garanteprivacy.it).

## 7. Menores

Zprium no está dirigido a menores de la edad mínima que exige Discord en tu país y no recoge a sabiendas datos de ellos más allá de lo necesario para funcionar en un servidor.

## 8. Cookies

La consola web usa **una única cookie de sesión** estrictamente necesaria para iniciar sesión. No usamos cookies de analítica ni de publicidad.

## 9. Cambios

Si cambiamos esta política, lo anunciaremos en **el servidor de soporte (https://discord.gg/HcfkxN7TcH)** y actualizaremos la fecha de arriba. Los cambios que reduzcan tus derechos no se aplicarán con carácter retroactivo.
