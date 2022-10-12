Antes de empezar a crear una solución de IoT, es importante comprender los recursos que están disponibles.

Cuando planee adoptar una solución de IoT, quizás la primera consideración es qué hardware va a necesitar (o tiene ya). Este problema se debe en parte al hecho de que los datos son el principal impulsor de la implementación de muchas soluciones de IoT, por lo que averiguar cuáles quiere recopilar y cómo hacerlo es fundamental en la arquitectura.

Aunque el hardware implementado en una solución de IoT incluye los dispositivos de infraestructura de red que se usan para proporcionar comunicaciones de Internet seguras, aquí se centrará en el hardware del dispositivo IoT.

# Dispositivos IoT habilitados para IP

Un dispositivo habilitado para IP es, simplemente, un dispositivo que puede establecer una conexión a una red (para muchos dispositivos IoT, esta conexión de red es Internet) y tiene una identidad única en esa red. "IP" significa "protocolo de Internet" y define la forma en que se entregan los mensajes sobre una red. En términos de redes, un mensaje es simplemente un paquete de información y un único paquete podría entregar parte de un mensaje de texto o un archivo de vídeo. La mayoría de los datos que se transfieren por Internet usan este protocolo de comunicación.

En términos de una solución de IoT, un dispositivo habilitado para IP es el que puede conectarse directamente a una red como Internet y usar esa conexión para comunicarse con un centro de IoT. Entre los ejemplos de dispositivos de consumidor se incluyen dispositivos de automatización domésticos, como videoporteros y termostatos que usan una conexión a Internet para comunicarse con un servidor central. Pero los dispositivos IoT de nivel industrial también pueden estar habilitados para IP. Los dispositivos habilitados para IP usan hardware especializado para habilitar esta funcionalidad.

Como podría esperar, los usuarios implementan dispositivos habilitados para IP en escenarios en los que los datos se deben recopilar, entregar y analizar en tiempo real, casi en tiempo real o de manera periódica.

# Dispositivos no habilitados para IP

No es necesario que un dispositivo esté habilitado directamente con IP para formar parte de una solución de IoT. Algunos dispositivos no usan IP para conectarse a otras partes de una solución de IoT, pero pueden utilizar otros protocolos. Estos dispositivos no se conectan a Internet por sí mismos, pero sus mensajes se enrutan a Internet por medio de otro hardware, como una puerta de enlace de campo (dispositivo IoT Edge) que se describe a continuación. Los dispositivos no habilitados para IP pueden usar protocolos específicos del sector (como CoAP5, OPC) y tecnologías de comunicación de corto alcance (como Bluetooth, ZigBee, etc.) para conectarse a otro hardware.

Por ejemplo, un sistema de seguridad doméstico que incluye sensores de ventana y una cerradura controlable puede proporcionar comunicación local entre los sensores dentro del hogar y usar un dispositivo de puerta de enlace de campo centralizado (que está habilitado para IP y conectado a Internet) para comunicarse con un servicio en la nube. Después, el propietario de la vivienda puede usar su teléfono inteligente para comprobar el estado de las ventanas y controlar la cerradura.

Los dispositivos de este tipo pueden ser útiles en escenarios donde se deben agregar datos de dos o más dispositivos, limpiarse e incluso analizarse antes de enviarse a un servicio en la nube. Como los dispositivos habilitados para IP suelen tener más recursos, los dispositivos con poca potencia o con restricciones de recursos (o espacio) pueden usar protocolos con menos requisitos de consumo de recursos que se transmiten a un dispositivo que no tiene estas restricciones.

# Sensores

Un sensor es un circuito (o dispositivo) que recopila un tipo específico de datos sobre el entorno físico. A medida que IoT sigue evolucionando, la lista de sensores disponibles sigue creciendo, a menudo de maneras inimaginables hace cinco años.
Un sensor inteligente es básicamente un dispositivo que recopila la entrada del entorno físico y procesa esa información localmente antes de comunicar los datos del mensaje. Es decir, el propio dispositivo procesa los datos hasta cierto punto antes de enviarlos al siguiente nodo de la arquitectura de IoT.

Los sensores se pueden insertar directamente en un dispositivo IoT, o bien implementarse como un producto externo de hardware que se conecta al dispositivo IoT mediante una interfaz definida. Algunos ejemplos de medidas de sensor sencillas son: temperatura, humedad, distancia y luz.

# Dispositivos IoT Edge y puertas de enlace de campo

En términos generales, una puerta de enlace de campo es un dispositivo especializado o software de uso general que actúa como habilitador de comunicación y, potencialmente, como sistema de control de dispositivos local y centro de procesamiento de datos de dispositivos. Una puerta de enlace de campo puede realizar funciones de control y procesamiento local que se dirigen hacia los dispositivos secundarios que están conectados a ella. En el caso de los servicios orientados a la nube, se puede usar una puerta de enlace de campo para filtrar o agregar telemetría de dispositivo y, por tanto, reducir la cantidad o frecuencia de los datos que se transfieren al back-end en la nube.

El ámbito de una puerta de enlace de campo incluye la propia puerta de enlace de campo y todos los dispositivos que están conectados a ella. Como su nombre implica, las puertas de enlace de campo actúan fuera de las instalaciones de procesamiento de datos dedicadas y a menudo se encuentran cerca de los dispositivos.

Una puerta de enlace de campo es diferente de un simple enrutador de tráfico, ya que tiene un rol activo en la administración del acceso y el flujo de información. Es una entidad dirigida a la aplicación y una conexión de red o terminal de sesión. Por ejemplo, en este contexto las puertas de enlace pueden facilitar el aprovisionamiento de dispositivos, el filtrado de datos, el procesamiento por lotes y la agregación, el almacenamiento en búfer de datos, la traducción de protocolos y el procesamiento de reglas de eventos. Por el contrario, los dispositivos o firewalls NAT no se califican como puertas de enlace de campo, ya que no son terminales de conexión o sesión explícitos, sino que enrutan (o deniegan) conexiones o sesiones realizadas mediante ellos.

# Revisión de las tecnologías de Azure IoT

Las soluciones de IoT requieren una combinación de tecnologías para conectar eventos, dispositivos y acciones de forma eficaz a aplicaciones en la nube. Las tecnologías y los servicios que usa dependen del desarrollo del escenario, la implementación y las necesidades de administración.

La pila de tecnologías y servicios de Azure IoT proporciona dos opciones de plataforma para la transformación digital de su organización.

- Plataforma como servicio (PaaS) es un modelo de informática en la nube en el que se adaptan las herramientas de hardware y software de Azure a una tarea o función de trabajo específica. Con los servicios de PaaS, es usted quien debe encargarse del escalado y la configuración, pero si usa la infraestructura como servicio (IaaS) subyacente, esta se encarga del trabajo.
- Plataforma de aplicaciones como servicio (aPaas) proporciona un entorno en la nube para compilar, administrar y entregar aplicaciones a los clientes. Las ofertas de aPaaS se encargan del escalado y la mayor parte de la configuración, pero todavía requieren la intervención del desarrollador para crear una solución finalizada.

![Stack Tecnologico](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.13.35.png "Stack Tecnologico")

# Soluciones de aPaaS administradas

Comience rápidamente con Azure IoT Central, una solución de un extremo a otro completamente administrada y que habilita escenarios de IoT muy eficaces sin necesidad de tener un gran conocimiento de soluciones en la nube.

La plataforma de aplicaciones de IoT Central es un entorno listo para el desarrollo de soluciones de IoT. Creada a partir de servicios de PaaS de Azure de confianza, reduce la carga y el costo del desarrollo, administración y mantenimiento de soluciones de IoT de nivel empresarial. Ofrece recuperación ante desastres integrada, multiinquilino, disponibilidad global y una estructura de costos predecible.

La interfaz de usuario web personalizable de IoT Central y la superficie de API permiten supervisar y administrar millones de dispositivos y sus datos a lo largo de su ciclo de vida. Introducción a la exploración de IoT Central en pocos minutos con el teléfono como dispositivo IoT: consulte telemetría en directo, cree reglas, ejecute comandos desde la nube y exporte los datos para el análisis empresarial.

Elija dispositivos del catálogo de dispositivos Azure Certified for IoT para conectarse rápidamente a la solución o desarrolle un dispositivo personalizado mediante las plantillas de dispositivo de IoT Central.

# Soluciones PaaS flexibles

Como cuentan con la cartera más completa de servicios IoT, las tecnologías de plataforma como servicio (PaaS) para IoT permiten crear, personalizar y controlar fácilmente todos los aspectos de la solución de IoT. Establezca comunicaciones bidireccionales con miles de millones de dispositivos de IoT y administre los dispositivos de IoT a gran escala mediante IoT Hub. A continuación, integre los datos de los dispositivos de IoT con otros servicios de plataforma, como Azure Cosmos DB y Azure Stream Analytics, para mejorar la información de la solución.

Para compilar una solución de IoT desde cero, use uno o varios de los siguientes servicios y tecnologías de Azure IoT:

## Dispositivos

Desarrolle sus dispositivos de IoT mediante uno de los kits de inicio de IoT de Azure o elija el dispositivo que desee usar en el catálogo de dispositivos Azure Certified for IoT. Implemente el código insertado mediante los SDK de dispositivo de código abierto. Los SDK de dispositivo admiten varios sistemas operativos, como Linux, Windows y sistemas operativos en tiempo real. Hay SDK para varios lenguajes de programación, como C, Node.js, Java, .NET y Python.

Puede simplificar aún más la forma de crear el código insertado para los dispositivos mediante el servicio IoT Plug and Play. IoT Plug and Play permite a los desarrolladores de soluciones integrar dispositivos en sus soluciones sin necesidad de escribir código integrado. En el núcleo de IoT Plug and Play se encuentra un esquema de modelo de funcionalidad del dispositivo que describe dichas funcionalidades. Use el modelo de funcionalidad del dispositivo para generar un código del dispositivo insertado y configurar una solución basada en la nube, como una aplicación de IoT Central.

Azure IoT Edge permite descargar en los dispositivos partes de una carga de trabajo de IoT de los servicios en la nube de Azure. IoT Edge puede reducir la latencia de una solución, reducir la cantidad de datos que los dispositivos intercambian con la nube y habilitar escenarios sin conexión. Los dispositivos IoT Edge se pueden administrar desde IoT Central y algunos aceleradores de soluciones.

Azure Sphere es una plataforma de aplicaciones segura y de alto nivel con características de comunicación y seguridad integradas para dispositivos conectados a Internet. Incluye una unidad de microcontrolador protegida, un sistema operativo basado en Linux personalizado y un servicio de seguridad basado en la nube que proporciona seguridad continua y renovable.

## Conectividad en la nube

El servicio Azure IoT Hub permite una comunicación bidireccional confiable y segura entre millones de dispositivos IoT y una solución basada en la nube. Azure IoT Hub Device Provisioning es un servicio asistente para IoT Hub. El servicio ofrece aprovisionamiento Just-In-Time sin interacción de dispositivos a la instancia correcta de IoT Hub sin necesidad de intervención humana. Estas funcionalidades permiten a los clientes aprovisionar millones de dispositivos de forma segura y escalable.

IoT Hub es un componente básico de los aceleradores de soluciones que se puede usar para cumplir los desafíos de implementación de IoT, como:

- La administración y la conectividad de los dispositivos de gran volumen.
- La ingesta de telemetría de gran volumen.
- El comando y el control de dispositivos.
- El cumplimiento de la seguridad de los dispositivos.
- Eliminación de la separación entre los mundos físico y digital

Azure Digital Twins es un servicio de IoT que permite modelar un entorno físico. Usa un grafo de inteligencia espacial para modelar las relaciones entre personas, espacios y dispositivos. Al correlacionar los datos de los mundos digital y físico, se pueden crear soluciones dependientes del contexto.

IoT Central usa gemelos digitales para sincronizar los dispositivos y datos del mundo real con los modelos digitales que permiten a los usuarios supervisar y administrar esos dispositivos conectados.

## Datos y análisis

Los dispositivos de IoT suelen generar grandes cantidades de datos de series temporales, como las lecturas de temperatura de los sensores. Azure Stream Analytics y Azure Data Explorer se pueden usar para procesar, consultar, analizar y visualizar datos.
Azure Maps es una colección de servicios geoespaciales que emplea datos de mapas recientes para proporcionar contexto geográfico preciso a las aplicaciones web y móviles. Para compilar las aplicaciones, puede usar una API REST, un control de JavaScript basado en web o un Android SDK.

# Opciones de software de dispositivo IoT

Como cualquier otro producto de hardware electrónico complejo actual, los dispositivos IoT deben ejecutar código para ser útiles. Pero como los dispositivos IoT tienden a ser pequeños y con restricciones de recursos, el entorno en el que se ejecuta el código variará según la funcionalidad, la superficie de memoria y el conjunto de características. Los dispositivos también tendrán que programarse para completar las tareas que los ingenieros necesitan que realicen. Hay muchos proveedores que desarrollan entornos de ejecución, sistemas operativos para dispositivos con recursos restringidos y herramientas de programación. 

El software que elija para las soluciones se verá afectado por una combinación de los siguientes elementos:

- Disponibilidad del software que necesita.
- Compatibilidad del software con los dispositivos que ha elegido.
- Compatibilidad con otros sistemas de software o nube de la solución.
- Reputación y longevidad del proveedor de software.
- El compromiso del proveedor de software de actualizar el sistema operativo y las herramientas para solucionar problemas de seguridad, errores y nuevas características.
- Requisitos de seguridad y privacidad.

La solución puede implicar dispositivos con dos o más sistemas operativos y entornos de desarrollo. Es importante recordar que cuanto más se necesite de la solución, más complejo será el desarrollo y el mantenimiento, por lo que se debe tener en cuenta el software que elija y las implicaciones que esta decisión tiene durante la fase de arquitectura del proyecto.

# Sistemas operativos de los dispositivos

Como se ha mencionado antes, hay muchas opciones para los sistemas operativos de los dispositivos. En la tabla siguiente se enumeran algunas de las opciones más populares para proporcionar una idea de las características y opciones disponibles.

![Tabla](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.21.00.png "Sistemas Operativos")

# Lenguajes de programación

En lo que respecta a la programación de dispositivos, el sistema operativo que se ejecuta en el dispositivo suele determinar qué lenguajes de programación se pueden usar. Muchos dispositivos de hardware modernos pueden admitir varios lenguajes y los ingenieros de placas pueden desarrollar tipos específicos de hardware para admitir varios lenguajes.

La diversidad de opciones hace que la elección de una plataforma de programación sea compleja e intentar incluso describir la matriz de opciones aquí no presentaría una imagen adecuada. En su lugar, se puede sugerir cómo abordar el proceso de toma de decisiones para una plataforma de programación.

- Determine qué datos quiere recopilar. Como se ha visto a lo largo del curso, la arquitectura de IoT generalmente comenzará por determinar qué problemas se van a resolver y esto, la mayoría de las veces, se caracterizará en términos de los datos que se quieren recopilar. Esto se relaciona con los lenguajes de programación, porque los datos que se quieren recopilar afectarán a los dispositivos que elija y los lenguajes de programación que elija tendrán que funcionar con la infraestructura de dispositivos que implemente.

- Piense en el equipo de desarrollo. Al considerar los lenguajes de programación que quiere usar en la solución, deberá tener en cuenta si quiere utilizar el talento del que ya dispone, aportar nuevos recursos o usar una combinación de ambos. Si el equipo de desarrollo de software actual tiene conocimientos de C# pero no de Python, la elección de una plataforma que admita C# como lenguaje de programación probablemente le permitirá una comercialización más rápida que tener que entrenar al talento existente en otro lenguaje o incorporar nuevos talentos que conozcan un lenguaje alternativo.

- Piense en el entorno de software más amplio. Al igual que en el elemento 2 anterior, cuando piense en qué plataforma de software quiere usar, puede resultar útil pensar en el entorno de desarrollo del grupo de negocio o empresa. El uso de un lenguaje que ya está implementado en otras áreas de la empresa puede hacer que tareas como el equilibrio de recursos, el uso compartido de código, el control de código fuente, la contratación y factores similares sean más eficaces.

- Elija un dispositivo o una plataforma de dispositivos. Cuando haya determinado qué datos quiere recopilar y haya pensado en el ecosistema más amplio, estará mejor informado para cuando tenga que elegir una plataforma de dispositivos. Es posible que necesite más de una plataforma de dispositivos, por lo que elegir las que sean más compatibles con los elementos 1 a 4 anteriores le dará un entorno general más eficaz en el que desarrollar la solución.

Por supuesto, estos elementos no son los únicos factores que se deben tener en cuenta. Elementos como el costo pueden tener un impacto significativo en la decisión, pero a veces el uso de una plataforma de dispositivos con un costo ligeramente mayor por elemento puede compensar al final si admite una plataforma de lenguaje que mejorará la eficacia durante la vida de la solución.

¿Qué sucede con la nube? No hace falta recordarlo, pero se recordará de todos modos: un componente esencial a la hora de elegir la plataforma de software son los servicios en la nube que se usarán para admitir el software y el hardware. En el tema siguiente se hablará más sobre la nube, pero es importante destacarlo aquí como un aspecto esencial del proceso de toma de decisiones.

# Kits de desarrollo de software

Los kits de desarrollo de software (SDK) a menudo se pueden usar para acelerar el proceso de creación de la solución. Si nunca ha usado un SDK, estos kits pueden acelerar el proceso de desarrollo de software y proporcionar al desarrollador todas las herramientas, paquetes de software y software de integración necesarios para crear una solución completa. Aunque el grado en que un SDK determinado beneficia al desarrollador variará en función de los proveedores y las empresas, un buen SDK proporcionará muchas de las herramientas relacionadas con el software necesarias para crear una solución.

# Puertas de enlace en la nube

Una puerta de enlace en la nube le permite administrar los dispositivos IoT y controla la comunicación con otros servicios en la nube. Las puertas de enlace en la nube pueden proporcionar cargas de trabajo como las siguientes (entre otras):

- Autenticación y autorización.
- Agentes de mensajes.
- Almacenamiento y filtrado de datos.
- Análisis de datos.
- Funciones (bloques de código discretos que realizan tareas específicas).

![Gateway](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.30.03.png "Puerta de enlace")

# Opciones de almacenamiento de datos

Dada la centralidad de los datos en una solución de IoT, la determinación de las opciones correctas de almacenamiento y recuperación de datos basadas en la nube ocupa un lugar destacado en la lista en términos de importancia. Los dispositivos IoT pueden generar grandes cantidades de datos rápidamente y almacenar grandes volúmenes de datos en la nube no solo puede resultar costoso, sino también difícil de controlar: debe ser capaz de hacer algo con los datos y un exceso de ellos puede dificultar el análisis y la toma de decisiones.

Los proveedores de servicios en la nube actualizan continuamente sus servicios de datos para que las organizaciones almacenen, administren y analicen los datos de forma más fácil y rentable. Aun así, un análisis exhaustivo de las opciones técnicas y los precios del almacenamiento en la nube debe ser una parte fundamental de cualquier arquitectura de IoT. Por ejemplo, algunas arquitecturas pueden exigir un enfoque de varios niveles con algunos datos almacenados en el dispositivo, otros en bases de datos locales y otros en la nube. En función de la arquitectura necesaria, debe asegurarse de que los servicios en la nube que elija admitan las necesidades.

Estos son otros conceptos que se deben tener en cuenta al considerar el almacenamiento en la nube.

A menudo, los datos son datos de serie temporal que se deben almacenar donde se puedan usar para tareas de visualización y generación de informes, además de ser accesibles posteriormente para más procesamiento. Es habitual dividir los datos en almacenes de datos "intermedios" y "en reposo". El almacén de datos intermedio contiene datos recientes a los que es necesario acceder con baja latencia. Los datos almacenados en almacenamiento en reposo suelen ser datos históricos. A menudo, la solución de base de datos de almacenamiento en reposo tendrá un costo menor, pero ofrece menos características de consulta y generación de informes que la solución de base de datos intermedia.

__Nota:__
La arquitectura Lambda para el almacenamiento de datos intermedio y en reposo se presenta más adelante en este curso.

Una implementación común del almacenamiento consiste en mantener un intervalo reciente (por ejemplo, el último día, semana o mes) de datos de telemetría en almacenamiento intermedio y los datos históricos en almacenamiento en reposo. Con esta implementación, la aplicación tiene acceso a los datos más recientes y puede observar rápidamente tendencias y datos de telemetría recientes. La recuperación de información histórica de los dispositivos se puede realizar mediante el almacenamiento en reposo, generalmente con una latencia mayor que si los datos estuvieran en almacenamiento intermedio.

![Almacenamiento](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.32.25.png "Almacenamiento")

Los proveedores de servicios en la nube pueden proporcionar servicios para admitir ambos tipos de almacenamiento y facilitar la administración de datos en estos tipos.
Puede obtener más información sobre las tecnologías de almacenamiento intermedio y en reposo que proporciona Microsoft Azure en la sección 3.5 del [documento Arquitectura de referencia de Azure.](https://learn.microsoft.com/en-us/azure/architecture/reference-architectures/iot)

![Arquitecture2](/img/Captura%20de%20Pantalla%202022-10-12%20a%20las%207.35.47.png "Arquitectura de la plataforma")

# Servicios de análisis y visualización de datos

Los servicios de análisis de datos suelen ser compatibles con las visualizaciones de datos. Las visualizaciones se pueden incluir en informes y colocarse en paneles. Una buena visualización puede comunicar información importante rápidamente.

# Análisis

Los datos que se capturan y almacenan solo resultan útiles cuando proporcionan información sobre el mundo de donde provienen. La necesidad de generar conclusiones es donde entran en juego los servicios analíticos.

Los servicios de análisis permiten a los arquitectos usar características avanzadas de mashup y modelado para combinar datos de varios orígenes de datos, definir métricas y proteger los datos en un único modelo de datos tabulares semántico de confianza. El modelo de datos proporciona a los usuarios una forma más fácil y rápida de examinar grandes cantidades de datos para el análisis de datos ad hoc.

Sin el análisis, los datos recopilados de IoT serían demasiado voluminosos y desestructurados para poder visualizar u obtener conclusiones. Los servicios de análisis permiten a los arquitectos crear relaciones significativas entre conjuntos de datos para facilitar la administración. Por ejemplo, Azure Stream Analytics puede tomar datos de flujo de dispositivos IoT y los ingenieros pueden especificar una consulta de transformación que defina cómo buscar datos, patrones o relaciones. La consulta de transformación usa un lenguaje de consulta similar a SQL que se utiliza para filtrar, ordenar, agregar y unir datos de streaming durante un período de tiempo.

# Visualización de datos

El análisis de flujos puede facilitar el condicionamiento de los datos para que sean más fáciles de administrar y proporciona modelos que ofrecen conclusiones sobre lo que necesita comprender o aprender. Una vez que los datos están condicionados y se han creado los modelos adecuados, los datos se pueden visualizar mediante herramientas como Time Series Insights de Microsoft o Power BI para que se pueda actuar sobre ellos.

Las herramientas de visualización de datos pueden tomar entradas de varios flujos de datos y combinarlas en "paneles" que se pueden usar para contar una historia sobre los datos recopilados. En última instancia, sacar más partido de los datos es el objetivo de IoT.

# Machine Learning

El aprendizaje automático (ML) es uno de los desarrollos más atractivos de la informática moderna. Es un campo complejo, pero que genera resultados positivos significativos con grandes conjuntos de datos. Los dispositivos IoT generan grandes volúmenes de datos. Los sistemas de análisis ayudan a los ingenieros a modelar los datos existentes de maneras significativas. El aprendizaje automático lleva este proceso un paso más allá y puede realizar predicciones sobre los nuevos datos que se mostrarán y proporcionar conclusiones que no serían posibles sin los algoritmos de aprendizaje automático.

Como el nombre indica, la tecnología ofrece a los equipos la capacidad de "aprender" (predecir) de los datos mediante la expresión de tendencias o la dirección que tomarán los datos en el futuro. Esta tecnología puede proporcionar a los ingenieros un mecanismo eficaz para habilitar una amplia variedad de escenarios.

El uso de macrodatos y el aprendizaje automático para predecir decisiones de compra es un ejemplo sencillo. Imagine que un minorista tiene almacenes en varias ciudades y debe determinar las existencias de los productos en esas ciudades para poder ofrecerlos a los clientes de la manera más eficaz y rápida. Mediante el aprendizaje automático, el minorista puede predecir, por ejemplo, que un conjunto determinado de usuarios que compran una televisión específica suele a comprar un tipo concreto de cable y otros accesorios, como soportes de televisión y equipos de audio. Esto permitiría al minorista mantener esos artículos en el almacén cerca de las ventas de televisión populares, de modo que si un cliente pide el cable u otro accesorio, el artículo se le pueda enviar más rápidamente.

¿Se le ocurren otros escenarios específicos de IoT en los que el aprendizaje automático podría ayudar a habilitar varios escenarios que pueden hacer que la arquitectura de IoT sea más eficaz? Debido a la enorme cantidad de potencia informática necesaria para realizar los cálculos necesarios para este tipo de análisis, la tecnología de ML basada en la nube tiende a ser la más eficaz para proporcionar el tipo de conclusiones que el aprendizaje automático promete.