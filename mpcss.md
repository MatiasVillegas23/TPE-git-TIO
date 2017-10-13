## 1. Uso innecesario del valor 0
El código siguiente no necesita la unidad especificada si el valor es cero.
__padding__:0px 0px 5px 0px;
En su lugar puede ser escrito de esta manera:
__padding__:0 0 5px 0;
De la misma manera es igual para otros estilos. Ej.:
__margin__:0;
No malgastes espacios agregando unidades tales como px, pt, em, etc., cuando el valor es cero. La única razón de hacer esto es si necesitas cambiar estos valores más tarde. Si no declarar estas unidades no tiene sentido. Los pixeles cero son iguales que los puntos cero.
Sin embargo, line-height puede no tener unidad. Por eso es válido lo siguiente:
__line-height__:1;
De cualquier manera, puedes utilizar una unidad en concreto como em si lo deseas.
## 2. Los colores en formato hexadecimal necesitan una almohadilla
Esto está mal:
__color__: ea6bc2;
Debe ser:
__color__: #ea6bc2;
O esto otro:
__color__: rgb (234.107.194);
## 3. Valores duplicados en los códigos de colores
No escribir el código de esta manera:
__color__: #ffffff;
__background-color__:#000000;
__border__:1px solid #ee66aa;
Los valores duplicados pueden ser omitidos. Escribiendo los códigos de esta manera:
__color__:#fff;
__background-color__:#000;
__border__:1px solid #e6a;
¡Por supuesto esto no debes hacerlo con códigos como este!
__color__: #fe69b2;
## 4. Evitar repeticiones de código innecesaria
Evita usar varias líneas cuando lo puedes conseguir con una sola. Por ejemplo, al fijar los bordes, algunas veces se debe hacer por separado, pero en casos como el siguiente no es necesario:
__border-top__:1px solid #00f;
__border-right__:1px solid #00f;
__border-bottom__:1px solid #00f;
__border-left__:1px solid #00f;
Podríamos resumirlo en una única línea esta:
__border__:1px solid #00f;
## 5. La duplicación es necesario con los estilos en cascada
En los estilos en cascada es aceptable repetir el mismo codigo para un elemento dos veces, si significa evitar la repetición mencionada en el punto arriba. Por ejemplo, digamos que tenemos un elemento donde solamente es diferente el "border" izquierda. En vez de poner cada "border" escrito usando cuatro líneas, uso sólo dos:
__border__:1px solid #00f;
__border-left__:1px solid #f00;
En este caso primero definimos todos los "borders" con el mismo color, pero más tarde para ahorrarnos dos lineas de código redefinimos el "border" izquierda a otro color, de esta manera hemos ahorrado dos líneas de código. <7p>
El ejemplo malgastando espacio quedaría así:
__border-top__:1px solid #00f;
__border-right__:1px solid #00f;
__border-bottom__:1px solid #00f;
__border-left__:1px solid #f00;
Obviamente supuestamente este ahorro de carga supone un retraso en la carga de la página pues estamos definiendo el "border" izquierda dos veces, pero la carga de este proceso es insignificante.
## 6. Los estilos inválidos no hacen nada
Un ejemplo es suficiente para explicar este error:
__padding__:auto
Este estilo solo puede ser aplicado a width y height pero no a padding.
## 7. Código Específico para cada navegador
Obviamente este tipo de código solo funcionará en el navegador al que va destinado, pero es hay que pensar si es rentable puesto que solo algunos usuarios podrán apreciar esos cambio.
## 8. Espacio perdido
No estoy seguro del porqué pero muchos diseñadores estan empeñados en desaprovechar el espacio en su código, usando un montón de innecesarios saltos de línea. Recuerda que eso sólo lo verás tu y estas haciendo un uso excesivo de ancho de banda. Tambien tu código será más facil de leer puesto que tendrá menos "boquetes".
Por supuesto es sabio dejar un cierto espacio para mantenerlo legible, aunque a algunos les encanta condensar todo, no dejando ningún espacio.
## 9. Especificar los colores sin usar palabras
Definir los colores usando las palabras que lo definen no es una buena idea puesto que estaríamos confiando en el navegador para que el interprete que color y código debe aplicar.Las tonalidades para un mismo nombre de color cambian mucho de un navegador a otro.
Es una buena práctica especificar siempre el color por su código hexadecimal.
Ej.: utilizar "#fff" en lugar de blanco.
## 10. Agrupar estilos idénticos
Es común ver los estilo escritos una y otra vez con el mismo código, aún cuando el estilo es igual.
Sería conveniente agruparlos y asi optimizaríamos espacio:
h1, p, #footer, .intro {
font-family:Arial,Helvetica,sans-serif;
}
Tambien nos hara mucho más facil la tarea de actualizar el código.
