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
