# Proyecto-baston-inteligente-para-personas-con-discapacidad-visual

## 🎯Objetivo
Diseñar e implementar un prototipo funcional de bastón electrónico inteligente, enfocado en mejorar la movilidad, seguridad y autonomía de personas con discapacidad visual total o parcial. Este dispositivo integrará tecnologías de detección, señalización y respuesta inmediata, permitiendo identificar obstáculos en el entorno del usuario a través de sensores ultrasónicos u otros métodos de proximidad.

El sistema será capaz de detectar obstáculos a distintas distancias (cortas, medias o largas) y generar alertas en tiempo real mediante señales hápticas (vibración), acústicas (buzzer) o una combinación de ambas, dependiendo del nivel de riesgo o proximidad del objeto. Estas alertas permiten al usuario reaccionar con anticipación, evitando accidentes o colisiones durante sus desplazamientos.

El bastón estará diseñado con una arquitectura modular basada en tecnología de bajo consumo energético y microcontroladores programables (como Arduino Nano), permitiendo su portabilidad, bajo costo y adaptabilidad. También se contempla su posible evolución hacia versiones mejoradas con conectividad inalámbrica, asistencia por voz o integración con smartphones.

Con este proyecto se busca no solo crear una herramienta útil, sino también concientizar sobre la inclusión tecnológica para personas con capacidades diferentes, aplicando conocimientos de electrónica, programación y diseño centrado en el usuario.

## 👥Integrantes
- **Hewing Odair Dimas CH**  
  - **Roles**:  
    - Hardware / Software / Documentación  
    - Diseño / Pruebas / Simulación  
    - Redacción / Ensamblado / Otros

## 📁Estructura del proyecto
- **Docs** : informes, presentación, cronograma
- **Codigo** : programas Arduino 
- **Esquematicos** : circuitos en PDF, CIRKIT DESIGNER IDE
- **Pruebas**: resultados,, fotos del circuito, videos
- **README.md**: este documento

## 🛠️ Recursos y Componentes Utilizados

| Componente              | Descripción                        |
|-------------------------|------------------------------------|
| [Arduino Nano CH340G](https://naylampmechatronics.com/ardusystem-tarjetas/88-arduboard-nano-ch340g-mini-usb.html)            | Microcontrolador principal         |
| [Sensor ultrasónico HC-SR04](https://naylampmechatronics.com/sensores-proximida9d/10-sensor-ultrasonido-hc-sr04.html)  | Medición de distancia con precisión |   
| [Buzzer activo de 5V](https://www.electromania.pe/producto/buzzer-activo-de-5v/ )          | Alerta sonora                      |  
| [Módulo motor vibrador](https://mecatronica.saisac.pe/producto/modulo-motor-vibrador-pwm/)      | Alerta táctil                      |   
| [Protoboard o PCB](https://www.teslaelectronic.com.pe/producto/protoboard-830-puntos/?srsltid=AfmBOorUNzrG_SfqL80-2YSSKAOINMZ1qC-t08mY8mVDi2wpZLwlb3Xg)      | Para conexiones                    |
| [Cableado / Jumpers](https://hifisac.com/shop/sch4015phmc-cable-jumper-dupont-macho-hembra-de-colores-largo-15cm-x-40-hilos-de-cobre-aluminio-113#attr=)     | Conexiones físicas                 |
| [Power Bank o batería](https://hifisac.com/shop/il-406080-406080-bateria-de-3-7-v-3000mah-ion-litio-recargable-overclick-60x80mm-3181?page=2&category=356#attr=)| Fuente de alimentación portátil   |
| [Modulo de Carga](https://naylampmechatronics.com/baterias/867-cargador-de-bateria-litio-tp4056-con-proteccion-usb-c.html)          | Carga del sistema                      |  
| [Elevador de Voltaje](https://www.electromania.pe/producto/modulo-elevador-de-voltaje-dc-dc-mt3608-2a/ )          | Controlara la tension adecuada para el Microcontrolador                      |  

## ⚙️ Funcionamiento

1. El sensor ultrasónico mide continuamente la distancia al obstáculo más cercano.
2. Si la distancia es menor a un umbral definido (por ejemplo, 100 cm), se activa una señal:
   - **Menos de 25 cm:** vibración leve
   - **Menos de 15 cm:** vibración + sonido intermitente
   - **Menos de 10 cm:** vibración + sonido continuo
3. Si no hay obstáculos cercanos, el sistema permanece en reposo.

## 📘 Guía de Instalación
## 🧰 Paso 1: Ensamblado del circuito

1. Conecta el sensor HC-SR04 a los pines D9 (Trig) y D8 (Echo) del Arduino.
2. Conecta el buzzer al pin D6.
3. Conecta el motor vibrador al pin D5, usando un transistor NPN para control si es necesario.
4. Usa la protoboard para organizar las conexiones.
5. Alimenta el Arduino Nano desde un Power Bank por el puerto USB.

## 💻 Paso 2: Subida del código

1. Abre el archivo `main.ino` en el IDE de Arduino.
2. Selecciona placa: `Arduino Nano`, procesador: `ATmega328P (Old Bootloader)`.
3. Conecta el cable USB y selecciona el puerto COM correcto.
4. Carga el código.

## ✅ Paso 3: Pruebas

1. Acerca un objeto al sensor para comprobar que el sistema reacciona.
2. Observa la vibración y sonido según la distancia.

## ⚠️ Recomendaciones
1. Asegúrate de que las conexiones sean firmes (usa soldadura o cinta si es necesario).
2. Monta el sistema en una estructura estable y protegida contra humedad o golpes.
3. Usa una caja impresa 3D o carcasa si planeas uso exterior frecuente.

🧪 Paso 4: Pruebas de Campo
1. Camina en una zona abierta con obstáculos de diferentes alturas.
2. Ajusta los umbrales en el código si detectas falsos positivos o falta de sensibilidad.
3. Prueba con diferentes superficies (paredes, personas, árboles) para validar la respuesta.
  
## 📅Avances semanales
| Semana | Actividad Realizada                                     | Responsable             |
|--------|----------------------------------------------------------|-------------------------|
| 1      | Solución a la problemática                              | Hewing Odair Dimas CH   |
| 2      | Plan o cronograma de trabajo                            | Hewing Odair Dimas CH   |
| 3      | Marco teórico y macro conceptual                        | Hewing Odair Dimas CH   |
| 4      | Objetivos generales y específicos del proyecto          | Hewing Odair Dimas CH   |
| 5–7    | Análisis general del proyecto                           | Hewing Odair Dimas CH   |
| 8–9    | Definición de las etapas del proyecto                   | Hewing Odair Dimas CH   |
| 10     | Implementación de hardware (Parte 1: simulación inicial)| Hewing Odair Dimas CH   |
| 11     | Hardware Parte 2: integración, simulación intermedia, presentación | Hewing Odair Dimas CH |
| 12     | Diseño de hardware físico (Parte 3: etapas finales)     | Hewing Odair Dimas CH   |
| 13     | Simulación completa del sistema                         | Hewing Odair Dimas CH   |
| 14     | Construcción del prototipo                              | Hewing Odair Dimas CH   |
| 15     | Implementación final con hardware                       | Hewing Odair Dimas CH   |
| 16     | Pruebas finales                                          | Hewing Odair Dimas CH   |
| 17     | Informe final y exposición                              | Hewing Odair Dimas CH   |

## 🔗Enlaces relevantes

- [**Carpeta de Drive**][(https://drive.google.](https://docs.google.com/document/d/11SQ5qAYkyvGoFjbeqlhEDSrGLlfBoQZC/edit?usp=sharing&ouid=116189080242814573393&rtpof=true&sd=true)

- [**Circuito en Cirkit Designer IDE**][(https://easyeda.](https://app.cirkitdesigner.com/project/67272e73-9a4e-40c8-9393-b1d8ad5ef423)

- [**presentacion PreziE**][(https://prezi.com](https://prezi.com/view/G4iW6ZMITZEsAauHOBNr/)

- [**Presentación en PPT**][(https://drive.google.](https://docs.google.com/presentation/d/1sXzTnTgZQWETXmpCuHFqTPqGexhuzV33/edit?usp=drive_web&ouid=116189080242814573393&rtpof=true)
  
- [**Presentación en YouTube**][(https://YouTube.com.](https://youtube.com/shorts/tHSOtOXz0b4?feature=share)
