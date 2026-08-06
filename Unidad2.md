# UNIDAD 2
## Actividad 04
### Reto de diseño: sistema visual generativo parametrizable

### 1. Intención visual
Emotividad, alegría y danza/movimiento.

### 2. Entidades que existirán en el sistema
Campos de valores, líneas y color.

### 3. Las relaciones y reglas que producirán el comportamiento
Un campo deforma a otro y sus valores determinan cambio en posición y color.

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

## Adelanto 3
> [!NOTE]
> Logro: El sistema "funciona". Esta relativamente terminado a como queria que se viera terminado.

Agregué un lookuptex con el fin de aplicarle color, también un LFO para variar la ramp que vendría siendo al paleta de colores y finalmente agregué un render simple para ver como se iba viendo.

> [!IMPORTANT]
>La familia de resultados no me desagrada pero se asemeja a un barrilete bailando que a la idea original de líneas entrelazadas como hilos bailando y alegre.

Evidencia 03:
<img width="1061" height="682" alt="image" src="https://github.com/user-attachments/assets/afbb21ff-dcdc-4942-852e-74fc8c73d972" />

Red "completa"
<img width="1917" height="762" alt="image" src="https://github.com/user-attachments/assets/eff8c829-f6eb-4b0b-ad71-77628bbebaf8" />
