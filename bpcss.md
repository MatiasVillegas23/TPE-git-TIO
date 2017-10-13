# Buenas Prácticas de CSS
A veces el resultado de la codificación descuidada desde el principio del diseño, es causa de múltiples cambios de código y de consumo excesivo de tiempo. Escribir código CSS limpio, es simple cuando se empieza con el pie derecho, como consecuencia hacemos que el código sea más fácil de mantener y editar más tarde.

En este articulo te damos unos cuantos consejos para que afiances el proceso en el desarrollo del código CSS, con esto podrás evitar problemas, y, al contrario, crearas un archivo bastante robusto y entendible.

## 1. Sea Organizado
Regla de oro en el desarrollo, vale la pena mantener el código organizado. En lugar de escribir aleatoriamente las clases y los id’s, es bueno tener un orden con esto. Esto le ayudará a mantener el concepto de cascada de CSS y establece su hoja de estilo para tomar ventaja de la herencia en estos archivos.

Declare sus artículos más genéricos primero, entonces siga con el que no es tan genérico y así sucesivamente. Esto permite que su CSS herede correctamente los atributos y lo hace mucho más fácil para que usted elimine un estilo específico cuando sea necesario. Usted será más rápido en la edición de su CSS más tarde porque va a seguir un formato fácil de leer, contara con una estructura lógica.

Utilice una estructura que funciona mejor para usted, manteniendo ediciones futuras y otros cambios futuros.
-	Resets y overrides
-	Enlaces y type
-	Diseño principal
-	Estructuras de diseño secundarias
-	Elementos de formulario

## 2. Título, Fecha Y Signos
Deja que otros sepan quien escribió el código CSS, cuando se escribió y a quién contactar si tienen preguntas al respecto. Esto es especialmente útil en el diseño de plantillas o themes.

## 3. Mantener Una Biblioteca De Plantillas
Una vez que se decida por una estructura para usar, quite todo lo que no es genérico y guarde el archivo como una plantilla CSS para su uso posterior.

Puede guardar varias versiones para múltiples usos: un diseño de dos columnas, un diseño de blog, de impresión, móviles y así sucesivamente. Es una locura tener que volver a escribir cada una de sus hojas de estilo desde el principio, sobre todo cuando se está utilizando las mismas convenciones y metodologías en cada uno.

## 4. Utilice Convenciones de nomenclatura de interés
Se dará cuenta de por encima de donde me declaré un par de columnas de id y les llamé col-alpha y col-beta. ¿Por qué no llamarlos col-left y col-right? Piense en futuras modificaciones, siempre.
Digamos, manejaos columnas en nuestro diseño, queremos mover la columna de la izquierda a la derecha, solo bastaría con cambiar la ubicación, pero tengamos en cuenta que el id, nos daría a entender que debería de estar en la izquierda. Confuso, ¿verdad?

Una de las principales ventajas del CSS es la capacidad de separar estilos de contenido. Puede rediseñar completamente su sitio con sólo modificar el CSS sin tener que tocar el código HTML. Así que no arruinar definitivamente el CSS mediante el uso de nombres de limitantes. Utilice convenciones de nomenclatura más versátiles y coherentes.
Deja posición o estilo palabras específicas de sus estilos y de identificación. Digamos, para una etiqueta A, manejar una clase .link-blue, con esto podemos saber que el color del vínculo será azul, y seguramente tendrá otras propiedades. Esta misma estrategia la puedes aplicar a otros tipos de elementos.

## 5. Guiones En Lugar De Under Lines
Para una mejor compatibilidad con versiones anteriores de los navegadores, es mejor entrar en el hábito de usar guiones en su lugar de los conocidos sub rayados ó under lines. Use #col-alpha en lugar de #col_alpha.

## 6. No Repitas Código
La reutilización de atributos es útil, siempre que sea posible mediante la agrupación de elementos en lugar de declarar los estilos de nuevo. Si su h1 y h2 utilizan el mismo tamaño de fuente, color y márgenes, agruparlos mediante una coma.
Usted también debe hacer uso de los atributos en línea siempre que sea posible. Siempre estar en la búsqueda de oportunidades para los elementos del grupo y utilizar los métodos abreviados de declaración.

## 7. Optimizar Para Archivos CSS Ligeros
El uso de los consejos anteriores, hará que realmente pueda reducir el tamaño de sus hojas de estilo. Cargas más pequeñas más rápido y más pequeño es más fácil de mantener y actualizar. Elimine lo que no es necesario y consolide en lo posible mediante la agrupación. Tenga cuidado también al usar FrameWorks CSS. Es probable que herede una gran cantidad de código que no se utilizará.

## 8. Escriba Su Base Para Gecko, Luego Ajustelo Para Webkit E IE
Sálvate a ti mismo, prevee problemas de dolores de cabeza y escribe el código CSS primero para los navegadores Gecko (Firefox, Mozilla, Netscape, Flock, Camino). Si su CSS funciona correctamente con Gecko, es mucho más probable que no presente inconvenientes en Webkit (Safari, Chrome) e Internet Explorer.

## 9. Validar El Código
Haga uso del validador gratuito de CSS de W3C. Si usted está atascado y su diseño no está haciendo lo que quiere que haga, el validador de CSS será de gran ayuda en señalar los errores.

## 10. Mantenga Una Casa Ordenada
Separe el código CSS específico para cada explorador web a su propia hoja de estilo individual, y úsalas, según sea necesario con JavaScript, código del lado del servidor o comentarios condicionales. Utilice este método para evitar hacks CSS en tus hojas de estilo principales. Esto hará que tu CSS base sea limpio y manejable.
