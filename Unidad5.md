# UNIDAD 5 - Input del performer

## Integración de tracking

En esta unidad, la red resultante da paso a un grid con trail y movimiento modulado por hand tracking, la integración además está con open stage y con strudel.


<img width="1299" height="732" alt="Captura de pantalla 2026-09-17 102230" src="https://github.com/user-attachments/assets/40652bc9-6cdd-40f9-936b-0d11e63af45d" />

## Vistazo a la estructura de la red

<img width="1480" height="775" alt="image" src="https://github.com/user-attachments/assets/f27f716d-5665-412d-93af-c016bd823c0e" />

Esta es la estructura general, donde tenemos base con parametros expuestos para modular.

Los OSC in y out, corresponden a la conexión con Open Stage Control. En Open se recibe los frames usados por touchdesigner y en touch se recibe los valores del fader que están usando para modular un invert de los colores.

### El toolkit de strudel es para modular con los sonidos recibidos desde ahí.
<img width="1688" height="604" alt="image" src="https://github.com/user-attachments/assets/76ad8c72-5788-4b63-8a52-c461a8355245" />

### El base de Media Pipe, contiene los gestos y valores usados para modular.
<img width="1640" height="418" alt="image" src="https://github.com/user-attachments/assets/d321f5c2-d97c-4b77-9ead-42e3f6e07995" />

### Finalmente, el base de visuales contiene toda la geometría y demás características de la red.
<img width="1854" height="639" alt="image" src="https://github.com/user-attachments/assets/e75a8260-2c87-4066-a6a4-e14c4ed5cb74" />
<img width="709" height="553" alt="image" src="https://github.com/user-attachments/assets/fe6c1faf-005e-4955-9828-51fdf3dee113" />
<img width="1725" height="460" alt="image" src="https://github.com/user-attachments/assets/572f9796-1000-4335-af19-ab10192504b1" />

