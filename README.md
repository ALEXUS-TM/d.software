# Venta de Videojuegos

Se propone diseñar un software en el que se calcule el número de videojuegos vendidos en la tienda según el tipo y el valor individual. La tienda vende sus videojuegos dependiendo de si el juego vendido es de **PS4**, **PS5** o **NS**, y del valor individual de cada uno.

El software debe registrar la venta individual y almacenarla en un registro para, al final, sumar y mostrar la venta total del día.

## Aclaraciones

- El valor de la venta individual puede variar con respecto a las demás.
- El cálculo corresponde únicamente al valor bruto.
- La aplicación debe calcular la venta individual y la venta total del día para almacenarlas.
- Los datos de venta deben almacenarse para llevar un registro.

---

# Historia de Usuario

## Título
**Cálculo y registro de ventas**

### Como:
Vendedor de juegos.

### Quiero:
Registrar cada venta indicando el tipo de videojuego (**PS4**, **PS5** o **NS**) y su valor individual.

### Para:
Calcular automáticamente el total vendido en el día y mantener un registro organizado de las ventas realizadas.

---

# Descripción

El sistema permitirá registrar ventas individuales de videojuegos, almacenando el tipo de consola y el valor de cada venta.

Con esta información, el software calculará tanto el valor de cada venta como el total acumulado del día, facilitando el control diario de ingresos.

---

# Criterios de Aceptación

1. El sistema debe permitir registrar una venta indicando:
   - Tipo de videojuego: **PS4**, **PS5** o **NS**.
   - Valor individual del videojuego.

2. El sistema debe calcular automáticamente:
   - El valor de cada venta registrada.
   - El total acumulado de ventas del día.

3. El sistema debe almacenar los datos de cada venta para consulta posterior.

4. El sistema solo calculará valores brutos, sin impuestos ni descuentos.

5. El sistema debe permitir registrar múltiples ventas durante el día.

---

# Diagrama UML: Caso de Uso# Diagrama UML - Caso de Uso

```text
                +------------------+
                |    Vendedor      |
                +------------------+
                         |
                         |
                         v
          +-----------------------------+
          |       Registrar Venta       |
          +-----------------------------+
                         |
                         |
      +------------------+------------------+
      |                                     |
      v                                     v
+------------------+             +----------------------+
| Validar Datos    |             | Calcular Venta       |
+------------------+             +----------------------+
                                             |
                                             v
                              +--------------------------+
                              | Almacenar Registro       |
                              +--------------------------+
                                             |
                                             v
                              +--------------------------+
                              | Actualizar Total del Día |
                              +--------------------------+
```
## Caso de Uso: Registrar Venta

**Nombre:** Registrar venta de videojuego

**Actores:** Vendedor

**Propósito:** Permitir al vendedor registrar la venta de un videojuego indicando el tipo de consola y su valor, para que el sistema calcule y actualice el total de ventas del día y almacene el registro.

---

# Curso de Eventos

1. El vendedor selecciona la opción **Registrar venta**.
2. El sistema solicita el tipo de consola (**PS4**, **PS5** o **NS**) y el valor del videojuego.
3. El vendedor ingresa la información solicitada.
4. El sistema valida que los datos sean correctos.
5. El sistema calcula el valor de la venta.
6. El sistema almacena la venta en el registro.
7. El sistema actualiza el total de ventas del día.
8. El sistema confirma que la venta fue registrada exitosamente.

---

# Postcondición

- La venta queda registrada en el sistema.
- El total de ventas del día se actualiza correctamente.
- La información queda disponible para consultas posteriores.
