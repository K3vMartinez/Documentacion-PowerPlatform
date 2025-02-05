# Formularios

Los **formularios** en **Power Apps** son contenedores que te permiten mostrar, editar o agregar  
datos de una o más fuentes de datos, como **SharePoint, Dataverse,** Office 365, etc.  
Facilitan la creación de **aplicaciones de entrada de datos** al proporcionar una **interfaz** intuitiva  
para que los usuarios interactúen con los datos.  

Los formularios presentan las siguientes características:

1. **Conexión de datos**:  
   Antes de crear un formulario, necesitas conectarlo a una o más fuentes de datos.  
   Pueden ser bases de datos, servicios web, **SharePoint**, etc.

2. **Diseño del formulario**:  
   Una vez que tienes tus datos, arrastras y sueltas un formulario en tu lienzo de **Power Apps**.  
   El formulario puede ser de edición, visualización o entrada de datos, según tus necesidades.

3. **Configuración de campos**:  
   Configuras los campos del formulario para que se vinculen a los campos de tu fuente de datos.  
   Esto determina qué datos se mostrarán o se podrán editar en el formulario.

4. **Interacción del usuario**:  
   Cuando un usuario interactúa con el formulario, puede agregar, editar o eliminar registros  
   según la configuración que hayas establecido.

5. **Validación y envío de datos**:  
   Puedes agregar reglas de validación para garantizar que los datos ingresados sean precisos.  
   Una vez que el usuario completa el formulario, los datos se pueden enviar y guardar en la fuente de datos.

Los formularios en **Power Apps** simplifican el proceso de captura y gestión de datos  
al proporcionar una experiencia de usuario intuitiva y personalizable.  
Puedes diseñarlos según tus necesidades específicas para que se ajusten a tus flujos de trabajo empresariales.

En los formularios se utilizan diferentes **funciones** para cambiar el modo en el que un formulario interactúa con los datos:

- **ViewForm(YourFormName)**:
  - Esta función establece el formulario especificado **(YourFormName)** en modo de vista.
  - En el modo de vista, los usuarios pueden ver los datos existentes pero no pueden editarlos ni agregar nuevos datos.  
    Es útil para mostrar información de solo lectura.

- **EditForm(YourFormName)**:
  - Esta función establece el formulario especificado **(YourFormName)** en modo de edición.
  - En el modo de edición, los usuarios pueden modificar los datos existentes en el formulario.
  - Si el formulario está conectado a una fuente de datos editable, los cambios que los usuarios realicen  
    se guardarán en esa fuente de datos cuando se envíe el formulario.

- **NewForm(YourFormName)**:
  - Esta función establece el formulario especificado **(YourFormName)** en modo nuevo.
  - En el modo nuevo, el formulario se limpia y está listo para que los usuarios ingresen nuevos datos.
  - Es útil cuando quieres permitir que los usuarios agreguen nuevos registros a tu base de datos o fuente de datos.

Estas funciones son útiles para controlar el comportamiento y la interacción de los formularios  
en tus aplicaciones de **Power Apps**, dependiendo de los permisos y las acciones que desees permitir  
a los usuarios realizar sobre los datos.

Cuando interactuamos con el formulario, siempre es bueno mostrar un **mensaje** a nuestro usuario  
para que tenga en cuenta el **resultado** de su interacción.  
En las siguientes fórmulas del formulario podemos ver los distintos tipos de **"salidas"** y opciones que nos puede aportar:

```Fpx
Notify("¡No se ha podido guardar! Por favor, intenta de nuevo más tarde o contacta a un administrador.", NotificationType.Error)
```
- **OnFailure.** Esto muestra una notificación de error si el formulario no se guarda correctamente. 

```Fpx
Navigate(Pantalla; ScreenTransition.Cover);; Notify("You have successfully submitted a record for " & Self.LastSubmit.Name);;
```
- **OnSuccess.** Esto navega a una pantalla llamada "Pantalla" con una transición de cubierta y muestra una notificación de éxito con el nombre del último registro enviado correctamente.

```Fpx
Formulario.LastSubmit.Nombre
```
- **LastSubmit.** Esta expresión obtiene el nombre del último registro enviado correctamente desde el formulario. 
- **OnReset.** Esto restablece el formulario a su estado inicial. 
```Fpx
ThisItem.FirstName & " " & ThisItem.LastName
```
- **Concatenar campos**. Esta expresión concatena los campos **FirstName** y **LastName** de un registro (por ejemplo, de una tabla de datos) con un espacio entre ellos. 

Si al ejecutar la app no aparece el formulario puede ser porque en la propiedad **"Default"** debes ponerlo en **"FormMode.New"** 