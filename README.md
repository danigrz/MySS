##MySS ( My Sreaming Sound )

¿Cansados de no tener siempre a mano es canción que necesitamos de vez en cuando para continuar con armonía a través de nuestra intensa jornada de quehaceres? ¿Artos de no encontrar para escuchar vuestra canción favorita por internet y que tenéis almacenada a salvo en vuestro ordenador? ¿O quizás sois de esos que usáis tantos dispositivos que ni sabéis la música que tenéis y Spotify no os deja satisfechos? ¡¡Pues estáis de suerte porque habéis acertado eligiendo nuestra aplicación!!

¡**MySS** es un servicio que os permitirá escuchar vuestras melodías allá donde vayáis! Con una intuitiva y personal interfaz de usuario disponible para navegadores podréis subir a vuestro espacio personal vuestras canciones favoritas y totalmente ¡¡¡**gratis**!!! ¡Lo que os permitirá escucharlas en cualquier dispositivo a cualquier hora! ¡Crea tus listas de reproducción! ¡Comparte tus canciones, tus listas con tus amigos! y además, por si fuera poco, ¡tú! que siempre has soñado con llevar tu propia radio, ofrecemos servicio de **streaming** para que te sientas como en los viejos tiempos y crees con tus canciones tu ¡¡estelar radio!! Te sorprenderás, oh hipster, escuchando tanto tú como tus amigos una radio completamente personal y chapada a la antigua. ¡Además nuestro increíble equipo está trabajando en la posibilidad de compartir con un click el audio de tu sistema con cualquier ser existente y por existir! Todos nosotros, fans de los discos de vinilo, sabemos lo costoso que es subir una canción de 400MB para que nuestros amigos puedan escucharla.... pues intentaremos solucionarlo para que todos puedan escuchar por streaming desde cualquier lugar del mundo tu colección de discos originales virtualizados de los 80, ¡estate atento a nuestras actualizaciones!

####*Características*

* Sube y escucha tus canciones personales desde cualquier dispositivo.
* Crea listas de reproducción.
* Crea de tus listas, radios streaming.
* Comparte tus canciones, tus listas y tus radios.
* *Comparte el audio de tu sistema con un click* ( Estamos trabajando en esta posibilidad )

####*Infraestructura*

Estamos usando Ubuntu Server 14.04 bajo Microsoft Azure como plataforma para el servicio. Actualmente solo hemos hecho pruebas con el sreaming de audio para saber si era posible la realización de la radio. Para ello hemos usado Icescast2 como servidor streaming y Ices0 como *feeder* de flujo de audio a Icecast dentro del propio Ubuntu Server. La aplicación se servirá a través de una página web que desarrollaremos en la que los usuarios podrán ver y subir las canciones que deseen desde sus equipos y, a través de la misma podrán escuchar de forma estática ( cuando ellos quieran ) las canciones, crear listas de reproducción, crear radios streaming en tiempo real de las mismas y compartir todo este contenido con otros usuarios, por tanto el sistema se desglosa en:

* Usuarios con su nick y contraseña.
* Carpetas con música.
* Listas de reproducción ( sobre carpetas )
* Compartición de las mismas y de canciones ( mediante links a las mismas en carpetas compartidas )
* Radios Streaming ( sobre listas de reproducción usando Icecast2 + Ices0 )
* Compartición de las radios ( mediante enlaces http que lleven a una reproducción embebida )

Además, nos gustaría poder añadir la compartición streaming del audio del equipo del usuario ( de la misma forma que las radios ) pero de momento desconocemos como podríamos enviar el flujo de audio del sistema a Icecast2 de una forma transparente al usuario, por eso lo comentamos como **opcional** pese a que ni siquiera sabemos si es posible.
