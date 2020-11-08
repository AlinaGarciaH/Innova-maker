# Innova-maker
Bienvenido a nuestro para el Mega Hackaton, llamado Asistente de llamadas de emergencia.

# Desarrollo del Bot 
Se utilizaron los siguientes servicios de Azure:
Una instancia App Service F1 
Bot de aplicación web
Cognitive Services - LUIS
Cognitive Services Speech API

Se trabajó con Bot Framework Composer para el desarrollo del Bot y Bot Framework Composer para su emulación.
Para el uso del servicio con Speech se utilizó la herramienta Windows Voice Assistant Client:
https://github.com/Azure-Samples/Cognitive-Services-Voice-Assistant/tree/master/clients/csharp-wpf

# Funcionamiento del Bot (propotipo).
1. Se recibe y se empieza a registrar la llamada 
2. El bot envia un audio o texto indicando cual es su emergencia.
3. El usuario empieza a hablar o escribir y el bot empieza a detectar las palabras.
4. Al terminar su oración (espacio de silencio) si detecta que no es un lenguaje apropiado o no son palabras que se mencionan en una emergencia, en ese momento se termina la comunicación.
5. Si detecta oraciones referente a un servicio, detecta las palabras clave y de inmediato le indica que se continuará con una operadora.
6. En ese momento se transfiere a una operadora donde deberá contestarle de inmediato y que tendrá a la mano todos los datos que generó el Bot.

Las palabras clave para su funcionamiento son:
Oraciones clave para pedir un servicio:
"hola, emergencia? necesito ayuda, quiero denunciar un robo"
"se reporta un accidente de cocina con quemaduras"
"se cayó un árbol en mi colonia"
"hay un accidente de trafico en la via morelos"

Las palabras clave para rechazar la llamada:
"hola mi amor"
"cual es el saldo de mi recibo"
"esta es una llamada de prueba"
"vendo tacos"

# Posibles mejoras del Bot
Por ser un propotipo, se tiene considerado en la siguiente fase de desarrollo:
Mejorar la IA con LUIS integrando todo el catálogo de los servicios de emergencia y mejorar su entrenamiento.
Mejorar el bot donde puedan indicar cualquier tipo de sentencias y verificar como se comporta la IA.
Analizar los audios como sollozos, gritos, risas, etc.
Un servicio con REST para enviar a una base de datos la información recibida en el bot.
