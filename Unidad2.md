# UNIDAD 2
## Actividad 04
### Reto de diseño: sistema visual generativo parametrizable

### 1. Intención visual
Emotividad, alegría y danza/movimiento.

### 2. Entidades que existirán en el sistema
Campos de valores, líneas y color.

### 3. Las relaciones y reglas que producirán el comportamiento
Un campo deforma a otro y sus valores determinan cambio en posición y color(deformación y cambio de color).

### 4. Los invariantes que conservarán su identidad
Las líneas nunca serán deformadas del todo.

### 5. Aquello que podrá variar en cada ejecución
Posición y color de las líneas.


## Adelanto 01

> [!NOTE]
> Logro: Crear líneas y moverlas de posición usand un LFO

-Problemas: las líneas se mueven en -x y necesito que solo ocurra en el eje y

> [!IMPORTANT]
>Tarea: que las líneas se muevan solo en x y el movimiento no sea como puntos fijos sino que se muevan como hilos enredados.

Evidencia avance 01:

[Base inicial del programa]<img width="1440" height="615" alt="image" src="https://github.com/user-attachments/assets/5e256f51-7b03-4309-a40b-0d26075cc416" />

Con SOPs hice cosas básicas como las líneas que se deformaran y un poquito de noise con LFOs para mover parámetros translate y rotate en y.

## Adelanto 02
> [!NOTE]
> Logro: Pude conectar los SOPs a POPs para agregarle más cositas de movimiento y deformación a las líneas.

> [!IMPORTANT]
>En este punto fue muy complejo entender cómo pasar de SOP a POP pero en realidad era muy simple. Al probar con el twist vi que las lineas asemejaban a la silueta de una persona bailando.
> Enseñanza: Los POP son mucho mejor de manejar que los SOP, son como SOP pero modernos.

Evidencia avance 02:
<img width="1182" height="558" alt="image" src="https://github.com/user-attachments/assets/6ba0e308-7faa-4969-9d6d-9cb5dcc01b1d" />

## Adelanto 03
> [!NOTE]
> Logro: El sistema "funciona". Esta relativamente terminado a como queria que se viera terminado.

Agregué un lookuptex con el fin de aplicarle color, también un LFO para variar la ramp que vendría siendo al paleta de colores y finalmente agregué un render simple para ver como se iba viendo.

> [!IMPORTANT]
>La familia de resultados no me desagrada pero se asemeja a un barrilete bailando que a la idea original de líneas entrelazadas como hilos bailando y alegre.

Evidencia 03:
<img width="1061" height="682" alt="image" src="https://github.com/user-attachments/assets/afbb21ff-dcdc-4942-852e-74fc8c73d972" />

Red "completa"
<img width="1917" height="762" alt="image" src="https://github.com/user-attachments/assets/eff8c829-f6eb-4b0b-ad71-77628bbebaf8" />

## Adelanto 04: 
> [!NOTE]
> Logro: La red ya se encuentra en un Base y expusimos los parámetros que queremos modificar

<img width="1911" height="852" alt="image" src="https://github.com/user-attachments/assets/42bb1266-ccf7-41ea-973f-cf077e884fa7" />

Red completa (pero falta agregar el "pulse")
<img width="1803" height="616" alt="image" src="https://github.com/user-attachments/assets/f3ba4987-efdc-4167-9acd-7648b7c0c82e" />

## Tabla. Parámetros expuestos
| Nombre | Tipo | Rango | Efecto visual |
|---------|------|--------|----------|
| Twist | Float | 1 – 10 | Intensidad de la deformación aplicada, modifica parámetro strength del Twist  |
| Noise | Float | 0 – 1 | Amplitud del Noise POP |
| ColorSpeed | Float | 0.1 – 1 | Velocidad de la animación o enq que cambia la paleta de colores mediante un LFO |
| Scale | Float | 0.1 – 1 | Varia la escala general de la geometría en el Render Simple TOP |
| Randomize | Pulse | — | Genera una nueva variación de la composición(me gustaría la de twist al azar, tiene potenfcial |


## Familias de soluciones
<img width="1867" height="912" alt="image" src="https://github.com/user-attachments/assets/186eabd6-4a80-4676-acdb-20ad05ccdec8" />
<img width="1890" height="887" alt="image" src="https://github.com/user-attachments/assets/cf3c88ba-cab9-4637-b69d-171e765d458f" />
<img width="1917" height="952" alt="image" src="https://github.com/user-attachments/assets/97fc9c12-99b4-4ffb-a13f-ae39224eebfd" />

> [!NOTE]
>**Reflexión:**
> La regla más significativa para este sistema fue al deformación, es la que tiene toda la magia de variaciones significativas en el sistema.
> Al estar modificando, cacharreando y viendo qué ponerle al sistema en touchdesigner me equivocaba mucho al intentar conectar nodos, el accidente que logré evitar era renderizar mal la geometría porque estaba usando un render de TOP normal que volvia la imagen en 2D.
> Lo que ajustaría antes de conectar a strudel es poner el random como pulse para tener la cuestión de eventos.
