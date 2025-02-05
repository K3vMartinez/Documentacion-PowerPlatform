# Conectar desde una aplicación de lienzo un flujo y asociarlo a un botón 
Podemos conectar un flujo desde una aplicación de lienzo y asociarlo a un botón para que cuando se presione se ejecute el flujo de datos. La sintaxis es la siguiente **"MiFlujo.Run(Campos)"**. 

En el siguiente ejemplo podemos ver como realizarlo: 

```Fpx
NOVACTA.Run(Cierre.Selected.Value; Fecha.SelectedDate)
```
## Explicación breve del código:

### **MiFlujo.Run(Campos)**:
- **"MiFlujo"** representa el nombre de un flujo de trabajo, proceso, o función que se ha definido en el sistema.  
  Podría estar asociado con una serie de operaciones o acciones automatizadas  
  que se ejecutan en base a datos o eventos específicos.

- **"Run"** es un método o función que, en este contexto, inicia la ejecución del flujo **"MiFlujo"**.

- **"Campos"** sería un parámetro o una serie de parámetros que se pasan al flujo de trabajo cuando se ejecuta.  
  Estos parámetros pueden influir en el comportamiento del flujo o determinar qué operaciones se realizarán durante su ejecución.

### Ejemplo: NOVACTA.Run(Cierre.Selected.Value; Fecha.SelectedDate): 
- **"NOVACTA"** aquí parece ser el nombre específico de un flujo de trabajo.  
  Podría ser el nombre de una función o proceso diseñado para manejar o procesar ciertas actividades dentro de una aplicación.

- **"Run"** sigue siendo el método para ejecutar el flujo.

- **"Cierre.Selected.Value"** y **"Fecha.SelectedDate"** son los parámetros específicos que se pasan al flujo **"NOVACTA"**:
  - **"Cierre.Selected.Value"** podría referirse al valor seleccionado de un control  
    (como un **dropdown** o una lista desplegable) llamado **"Cierre"**.  
    Este valor seleccionado se utiliza como entrada para el flujo.
  - **"Fecha.SelectedDate"** se refiere a la fecha seleccionada en un control de fecha,  
    utilizada como otro parámetro para el flujo.

Estos parámetros permiten que el flujo de trabajo **"NOVACTA"** realice sus operaciones  
tomando en cuenta un valor de **"cierre"** y una **"fecha"** específicos,  
lo que es útil para procesos que dependen de entradas de usuario,  
como cierres de actividad, actualizaciones de estado, registros, etc.

## Conclusiones importantes 
El código se debe agregar a la propiedad **"onSelect"** del componente **botón**. 