
## Configuración básica de Gatling

1.  Descargar gatling de <http://gatling.io/download/>

> ![](.//media/image1.jpeg)


2.  Ejecutar recorder.bat (Windows) o recorder.sh(Linux) en /bin

> ![](.//media/image2.jpeg)

3.  Se abrirá la siguiente ventana

> ![](.//media/image3.jpeg)

4.  Llenar los siguientes campos con los referentes a la aplicación. Nombre de la simulación y parámetros básicos

> ![](.//media/image4.png)
Qué no debe capturar el proxy

> ![](.//media/image5.png)

Puerto por el que el proxy va a funcionar (Debe ser distinto al de la aplicación)

> ![](.//media/image9.png)
5.  Iniciar el proxy

> ![](.//media/image13.png)

6. (En LINUX) Cierre todas las instancias de Chrome, y ejecútelo de manera que haga uso del Proxy HTTP de Gatling (tenga cuidado en asociar el mismo puerto configurado en el dicho Proxy):

    ```bash
    google-chrome --proxy-server="http://localhost:8081"
    ```



7.  Desde el navegador, ingrese a la aplicación que va a perfilar, y realice la interacción que quiere replicar en las pruebas de carga.
>
> Verifique que en la medida que se realiza dicha interacción, se muestren los eventos capturados en el 'grabador' de Gatling:
>
> ![](.//media/image19.png)

8.  Una vez terminamos la simulación le damos al botón de stop and save

9.  Encontraremos la simulación en el directorio “user-files” bajo el nombre que le dimos

> ![](.//media/image28.jpeg)

10. Al abrir la simulación encontramos un objeto que podemos modificar para añadir más variables

> ![](.//media/image29.jpeg)

11. Para correr esta simulación se utiliza “gatling.bat” o “gatling.sh”

> ![](.//media/image30.jpeg)

12. Escogemos la simulación personalizada. Como se ve, Gatling empezará la simulación que le hemos dado usando nuestro comportamiento de usuario.

> ![](.//media/image31.png)

13. Una vez termine los test dará una URL donde podemos comprobar los resultados

> ![](.//media/image32.png)

14. Al abrir la página estos son desplegados

> ![](.//media/image33.png)
Como se puede ver solo se manejó un usuario

> ![](.//media/image34.png)


15. Si deseamos añadir más usuarios al tiempo solo hay que cambiar la inyección presente

> ![](.//media/image35.png)

16. Y volver a correr gatling.bat o gatling.sh

> ![](.//media/image36.jpeg)


17. Una vez volvamos a tener el reporte podemos ver que se muestran 5 usuarios al tiempo

> ![](.//media/image37.jpeg)

18. Para ver más parámetros de configuración, [revise la documentación oficial de Gatling](https://gatling.io/docs/2.3/general/simulation_setup/).