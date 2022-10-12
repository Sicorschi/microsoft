Una arquitectura de solución describe los componentes de la solución y cómo funcionan conjuntamente.

Durante la última década, el Internet de las cosas (IoT) ha sido definido de muchas formas por muchas personas. Esta es la definición que captura la esencia de IoT para desarrolladores:

```El Internet de las cosas es una red de dispositivos conectados a Internet que comunican datos de sensores integrados a la nube para un procesamiento centralizado.```

Como se indica en esta definición simple, una solución de IoT implica dos componentes esenciales:

- Un lado del dispositivo (que se consta de dispositivos individuales) que actúa como origen de datos.
- Un lado de la nube que recopila datos y proporciona recursos para analizar y administrar esos datos.

Una vez que su empresa comienza a planear una solución de IoT, descubre que tanto el lado del dispositivo como el lado de la nube implican implementaciones complejas que proporcionan cientos de características necesarias, e incluso la comunicación entre el dispositivo y la nube puede ser compleja y requerirá protocolos de comunicación seguros. Para ayudarle a cumplir estos desafíos, Microsoft ha desarrollado Marco de buena arquitectura de Azure (WAF).

Azure WAF proporciona instrucciones que se pueden usar para establecer una arquitectura en la nube de alta calidad, estable y eficaz.

# Subsistemas principales de una solución de IoT

En esencia, una arquitectura de solución de IoT consta de los subsistemas siguientes:

- Dispositivos que tienen la capacidad de registrarse de forma segura en la nube y opciones de conectividad para enviar y recibir datos (entre dispositivos y la nube).
- Un servicio de puerta de enlace en la nube, o centro, que proporciona capacidades de gestión de dispositivos y acepta datos de dispositivos de forma segura.
- Procesadores de flujos que consumen datos del centro, se integran con procesos empresariales y colocan los datos en el almacenamiento.
- Una interfaz de usuario visualiza los datos de telemetría y facilita la administración de dispositivos.

Estos subsistemas principales se pueden alinear con un modelo de cosas/conocimientos/acciones, como se muestra a continuación en una vista de alto nivel de la arquitectura de referencia de Azure IoT.

![Arquitectura](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%206.54.56.png "Arquitectura - subsistemas")

### Dispositivos IoT
dispositivos físicos donde se originan los datos.

### Puerta de enlace en la nube
proporciona un centro en la nube para la conectividad segura, la telemetría y la ingesta de eventos y las funcionalidades de administración de dispositivos (incluidos los comandos y el control).

### Interfaz de usuario e informes
la interfaz de usuario de una aplicación de IoT se puede entregar en una amplia gama de tipos de dispositivos, en aplicaciones nativas y exploradores.

### Procesamiento de secuencias
procesa grandes flujos de registros de datos y evalúa las reglas de esas secuencias.

### Almacenamiento
se puede dividir en ruta de acceso de acceso intermedio (datos que deben estar disponibles para informes y visualizaciones inmediatamente desde dispositivos) y ruta de acceso en frío (datos que se almacenan a largo plazo y se usan para el procesamiento por lotes).

### Integración de procesos empresariales
facilita la ejecución de acciones basadas en información procedente de los datos de telemetría del dispositivo durante el procesamiento de flujos. La integración podría incluir el almacenamiento de mensajes informativos, alarmas, envío de correo electrónico o SMS, integración con CRM, etc.

# Subsistemas opcionales

Además de los subsistemas principales, muchas aplicaciones de IoT incluirán subsistemas para lo siguiente:

- Dispositivos perimetrales que proporcionan conexiones de dispositivo mejoradas y procesamiento local.
- Transformación de datos de telemetría enviados desde dispositivos.
- Interfaces de administración de usuarios que proporcionan las herramientas correctas para distintos roles y usuarios.
- Aprendizaje automático para admitir escenarios, como el mantenimiento predictivo.
- Rutas de acceso de almacenamiento de acceso frecuente, en frío e intermedio.
- Aprovisionamiento masivo de dispositivos para implementar flotas de dispositivos.

![Arquite](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.01.05.png "Arquitectura completa")

### Transformación de datos
la manipulación o agregación del flujo de telemetría antes o después de que lo reciba el servicio de puerta de enlace en la nube (el IoT Hub). La manipulación puede incluir la transformación de protocolo (por ejemplo, la conversión de datos binarios transmitidos a JSON), la combinación de puntos de datos y mucho más.

### Subsistema de aprendizaje automático (ML)
permite a los sistemas aprender de datos y experiencias y actuar sin programarse explícitamente. Los escenarios como el mantenimiento predictivo se habilitan mediante ML.

### Subsistema de administración de usuarios
permite especificar diferentes funcionalidades para que los usuarios y grupos realicen acciones en dispositivos (por ejemplo, comandos y controles, como actualizar el firmware de un dispositivo) y funcionalidades para los usuarios de las aplicaciones.

### Dispositivos perimetrales
estos dispositivos desempeñan un rol activo en la administración del acceso y el flujo de información. Pueden facilitar el aprovisionamiento de dispositivos, el filtrado de datos, el procesamiento por lotes y la agregación, el almacenamiento en búfer de datos, la traducción de protocolos y el procesamiento de reglas de eventos y mucho más.

### Aprovisionamiento masivo
facilita el aprovisionamiento de un gran número de dispositivos.

# Análisis del flujo de datos y el procesamiento

Es importante comprender que cuando los datos se entregan al back-end de IoT, el flujo de procesamiento de datos se puede implementar de varias maneras. En función de los escenarios y las aplicaciones, los registros de datos pueden fluir a través de distintas fases, combinadas en orden diferente y procesadas a menudo por tareas simultáneas y paralelas.

Estas fases se pueden clasificar en cuatro categorías: almacenamiento, enrutamiento, análisis y acción/presentación:

- El almacenamiento incluye cachés en memoria, colas temporales y archivos permanentes (por ejemplo, una base de datos).
- El enrutamiento permite enviar registros de datos a uno o varios puntos de conexión de almacenamiento, procesos de análisis y acciones. El enrutamiento toma decisiones sobre qué datos deben ir a qué destino y cuándo.
- El análisis se usa para ejecutar registros de datos a través de un conjunto de condiciones y puede generar diferentes registros de datos de salida. Por ejemplo, los datos de telemetría de entrada codificados en un formato pueden devolver telemetría de salida codificada en otro formato.
- Los registros de datos de entrada originales y los registros de salida de análisis normalmente se almacenan y están disponibles para mostrarse, y pueden desencadenar acciones como correos electrónicos, mensajes instantáneos, incidencias de incidentes, tareas de CRM, comandos de dispositivo, etc.

Estos procesos se pueden combinar en gráficos simples, por ejemplo, para mostrar datos de telemetría sin procesar recibidos en tiempo real, o gráficos más complejos que ejecutan varias tareas avanzadas, como actualizar paneles, desencadenar alarmas e iniciar procesos de integración empresarial, etc.

Las arquitecturas de IoT también pueden admitir varios sistemas para aceptar y procesar datos. Por ejemplo, aunque algunos dispositivos pueden conectarse directamente a la nube para el procesamiento de datos (como se muestra en la ruta de acceso anterior), otros dispositivos pueden almacenar o analizar datos localmente dentro de puertas de enlace perimetrales o de campo antes que los servicios proporcionados por la nube. En otro escenario, la traducción de protocolos proporcionada por una puerta de enlace perimetral puede ser necesaria para conectar dispositivos heredados o restringidos a la nube (la traducción de protocolos se puede usar para conectar dispositivos que no están habilitados para IP).

# Análisis de las necesidades arquitectónicas transversales

Las necesidades transversales (o cuestiones transversales) son aspectos de la solución que afectan al otro subsistema dentro de una solución y que no se pueden separar de estos subsistemas.

Hay varias necesidades transversales para las soluciones de IoT que son fundamentales para el éxito, entre las que se incluyen las siguientes:

- Requisitos de seguridad; incluidos la administración y auditoría de usuarios, la conectividad de dispositivos, la telemetría en tránsito y la seguridad en reposo.
- El registro y la supervisión de una aplicación en la nube de IoT es fundamental para determinar el estado y solucionar problemas de errores, tanto para subsistemas individuales como para toda la aplicación.
- Alta disponibilidad y recuperación ante desastres, que se usa para recuperarse rápidamente de errores sistémicos.

![Transversal](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.06.56.png "Arquitectura transversal")

### Seguridad
la seguridad es una consideración fundamental en cada uno de los subsistemas. La protección de las soluciones de IoT requiere un aprovisionamiento seguro de dispositivos, conectividad segura entre dispositivos, dispositivos periféricos y la nube, acceso seguro a las soluciones de back-end y protección de datos segura en la nube durante el procesamiento y almacenamiento (cifrado en reposo).

### Registro y supervisión
las acciones de registro y la actividad de supervisión asociadas a la solución de IoT son fundamentales para determinar el tiempo de actividad del sistema y solucionar los errores.

### Alta disponibilidad y recuperación ante desastres
la alta disponibilidad y recuperación ante desastres (HA/DR) se centra en garantizar que un sistema IoT siempre está disponible, incluidos los errores resultantes de desastres. La tecnología usada en subsistemas de IoT tiene diferentes características de conmutación por error y compatibilidad entre regiones. En el caso de las aplicaciones de IoT, esto puede dar lugar a la necesidad de hospedar servicios duplicados y duplicar los datos de la aplicación entre regiones en función del tiempo de inactividad y la pérdida de datos de la conmutación por error aceptables.

