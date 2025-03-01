## Desplegar contenedor docker
Para desplegar este contenedor necesitoamos realizar los siguientes comandos:

1. **Construir la imagen Docker**:
   ```sh
   docker build -t pps/apache-csp -f Dockerfile .
   ```
2. **Ejecutar el contenedor**:
   ```sh
   docker run -d -p 8080:80 -p 8443:443 pps/apache-csp
   ```
3. **Comprobar si la política CSP está aplicada**:
   ```sh
   curl -I http://localhost:8080
   ```
Si todo esta bien deberiamos ver una salida similar a la que se muestra en la siguiente captura de pantalla.

![Modificacion del apache2.conf](Capturas/Captura1.png)
