# Política de privacidad de Zprium

**Última actualización:** 4 de octubre de 2026

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
- aplicas sobre un mensaje la acción "Resumir".

Nunca guardamos ese texto.

| Datos | Para qué | Base jurídica | Cuánto tiempo |
| :--- | :--- | :--- | :--- |
| Identificador, nombre e idioma del servidor | Saber dónde está Zprium y en qué idioma responder | Prestación del servicio | Hasta 30 días después de que el bot salga del servidor |
| Qué módulos activó el servidor y su configuración, con el identificador del administrador que la cambió | Aplicar la configuración que eligió el servidor | Prestación del servicio | Igual que el anterior |
| Registro de seguridad (identificadores de quien hace y de quien recibe una acción, la acción y sus detalles; en una cuarentena, los roles retirados para poder devolverlos) | Detectar y registrar ataques (borrados masivos, raids) y las acciones de administración, en un registro a prueba de manipulación | Interés legítimo (seguridad) | **Hoy sin borrado automático.** Desde la versión 8.0.6, los registros nuevos guardan un seudónimo en lugar de tu identificador, y el olvido se hace destruyendo la llave de ese seudónimo (ver §6). El archivo de los registros de más de 12 meses llegará más adelante. Hasta entonces atendemos las solicitudes a mano |
| Casos de moderación, si el servidor activa el módulo de moderación. Cada caso guarda: la acción (aviso, nota, aislamiento, expulsión o baneo), un **seudónimo** de la persona afectada y otro del moderador (nunca el identificador de Discord de ninguno de los dos), el motivo que escribe el moderador, la duración, la fecha y si el caso se anuló. También se registran como casos los aislamientos, las expulsiones y los baneos que el staff hace desde Discord | Que el staff del servidor lleve un historial de moderación y que cada acción quede registrada y se pueda comprobar | Interés legítimo (seguridad y convivencia del servidor) | **24 meses** desde el caso; después se borra solo. También se borra si el bot sale del servidor (30 días) |
| Apelaciones de casos de moderación, si el servidor las activa. Cada apelación guarda: su estado (pendiente, aceptada o rechazada), las fechas, un **seudónimo** tuyo y otro de quien la decidió (nunca el identificador de Discord de ninguno de los dos) y la respuesta del staff, si escribe una. **El texto de tu apelación no lo guardamos:** se publica en el canal de apelaciones del servidor | Que puedas pedir al staff que revise un caso, y que su decisión quede registrada | Interés legítimo (seguridad y convivencia del servidor, y que puedas defenderte de una sanción) | Lo mismo que su caso: **24 meses** desde el caso, y se borra con él. También se borra si el bot sale del servidor (30 días). Lo publicado en el canal queda allí mientras su staff lo conserve |
| Registros del servidor, si el servidor activa el módulo de registros. Zprium publica en los canales que elige el staff: entradas y salidas de miembros (con la fecha de creación de la cuenta), mensajes borrados o editados (autor, canal y hora; **nunca el texto**), entradas y salidas de los canales de voz, canales y roles creados, cambiados o borrados (y quién lo hizo) y los casos de moderación | Que el staff del servidor vea lo que pasa en él y pueda moderarlo | Interés legítimo (seguridad y convivencia del servidor) | **Zprium no los guarda:** cada evento espera en memoria como mucho 15 minutos hasta que se publica, y se pierde si el bot se reinicia. Lo publicado queda en el canal del servidor mientras su staff lo conserve |
| Registro de eventos (identificadores en los eventos del servidor, sin texto de mensajes) | Recuperación ante fallos y análisis de seguridad | Interés legítimo | 30 días |
| Automatizaciones del servidor (Z-Flow): definiciones, ejecuciones (solo metadatos, nunca el texto) y fallos | Ejecutar las automatizaciones que crea el servidor | Prestación del servicio | Ejecuciones: 90 días. Fallos resueltos: 30 días. Definiciones: hasta la purga del servidor |
| Equipos, alineaciones y resultados de scrims (esports) | Organizar partidas del servidor | Prestación del servicio | Hasta la purga del servidor |
| Documentos que el staff añade a la base de conocimiento de IA, y sus vectores | Responder preguntas con IA local | Prestación del servicio | Hasta que se borra el documento o se purga el servidor |
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

**Registros del servidor.** Si el servidor activa el módulo de registros, Zprium publica en un canal del staff cuándo entras o sales del servidor, cuándo entras o sales de un canal de voz y cuándo se borra o se edita un mensaje tuyo. De un mensaje solo indica el autor, el canal y la hora: **nunca su texto**, que Zprium no lee. Si el mensaje no estaba en la memoria del bot, ni siquiera el autor. Zprium no informa de nada que pase en un canal que Discord le oculta, y sus publicaciones no notifican a nadie. Esos registros los lee el staff del servidor, que los guarda o los borra como cualquier otro mensaje de su servidor. Zprium no conserva copia.

**Lista completa, generada desde el código:** [datos por módulo](https://izkron.github.io/zprium-legal/privacidad-datos-por-modulo.html).

**Inteligencia artificial:**
- La IA de Zprium (resúmenes, preguntas a la base de conocimiento) funciona **solo en nuestro equipo**, con modelos locales.
- Ningún texto sale hacia servicios de IA de terceros.
- No usamos tus datos para entrenar modelos.
- Las respuestas generadas por IA se identifican como tales.

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
- **Registros del servidor.** Zprium no guarda los registros que publica, así que no hay nada que borrar en nuestros sistemas. Las publicaciones están en el canal del servidor: para que se borre una, pídeselo a su staff. Si no te atienden, escríbenos y lo comunicamos al servidor.
- **Lista de olvidos.** Para que restaurar una copia de seguridad no pueda deshacer tu olvido, guardamos una lista mínima con tres datos:
  - una huella de tu identificador (HMAC-SHA256), calculada con una clave que se guarda fuera de la base de datos. Nunca tu identificador en claro, y sin esa clave la huella no se puede relacionar contigo;
  - la fecha del olvido;
  - quién lo ejecutó.

  Después de **cualquier** restauración de una copia, y antes de que el bot vuelva a arrancar, se vuelven a aplicar todos los olvidos de la lista: se destruyen otra vez las llaves y los datos de miembro anteriores a cada olvido. Si vuelves a usar el bot después del olvido, empiezas de cero y la lista no afecta a tus datos nuevos. La lista se conserva mientras exista el servicio, porque es lo que impide que el olvido se deshaga y lo que demuestra que atendimos tu solicitud.
- Los administradores pueden borrar todos los datos de su servidor sacando al bot: se eliminan a los 30 días.

**Reclamaciones:** también puedes reclamar ante la autoridad de protección de datos de tu país. En **Italia** es el **Garante per la protezione dei dati personali** (https://www.garanteprivacy.it).

## 7. Menores

Zprium no está dirigido a menores de la edad mínima que exige Discord en tu país y no recoge a sabiendas datos de ellos más allá de lo necesario para funcionar en un servidor.

## 8. Cookies

La consola web usa **una única cookie de sesión** estrictamente necesaria para iniciar sesión. No usamos cookies de analítica ni de publicidad.

## 9. Cambios

Si cambiamos esta política, lo anunciaremos en **el servidor de soporte (https://discord.gg/HcfkxN7TcH)** y actualizaremos la fecha de arriba. Los cambios que reduzcan tus derechos no se aplicarán con carácter retroactivo.
