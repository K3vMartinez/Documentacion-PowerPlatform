# Resetear texto de entrada
En muchos formularios se puede observar que nos dan la opción de clicar en un botón y poder **limpiar todos los campos** del mismo y ponerlos en blanco. El motivo de este botón es aportarle la **comodidad** al usuario para que no tenga que ir campo a campo borrando una entrada errónea. Por esto mismo en las aplicaciones de lienzo existe una manera de **resetear o limpiar** dichas entradas de texto. 

El comando a utilizar es el siguiente: 
```Fpx
Reset(entradaTexto)
```
Como podemos ver en la foto siguiente, hemos aplicado este comando en un icono. Si en la fórmula **"OnSelect"** introducimos el comando **"Reset"** y como parámetro le ponemos exactamente qué **entrada de texto** queremos resetear. 

![img](./img/resetearTexto.png)