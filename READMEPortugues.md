# Optimización de Precios y Mix de Producto

Para este caso utilizaremos uno de los principales frameworks de optimización lineal, PuLP. Usaremos esta excelente herramienta para tratar de resolver el siguiente problema empresarial:

Lua Smart Tech ensambla y prueba dos modelos de teléfonos inteligentes, Lua1 y Lua2. Para el próximo mes, la empresa quiere decidir cuántas unidades de cada modelo ensamblará y luego probará.

No hay ningún teléfono inteligente en stock desde el mes anterior y, dado que estos modelos se cambiarán después de este mes, la compañía no quiere mantener ningún stock para el mes siguiente.

Ella cree que lo máximo que puede vender este mes son 600 unidades del modelo Lua1 y 1200 unidades del modelo Lua2.

Cada modelo Lua1 se vende por R$ 300,00 y cada modelo Lua2 por R$ 450,00. El costo de los componentes para un Lua1 es de R$ 150,00 y para un Lua2 es de R$ 225,00.

Se requiere mano de obra para el montaje y las pruebas. Hay un máximo de 10.000 horas de montaje y 3.000 horas de prueba disponibles. Cada hora de trabajo de montaje cuesta R$ 11 y cada hora de trabajo de prueba cuesta R$ 15. Cada Lua1 requiere cinco horas para el montaje y una hora para la prueba. Cada Lua2 requiere seis horas para el montaje y dos horas para la prueba.

Lua Smart Tech quiere saber cuántas unidades de cada modelo debe producir (ensamblar y probar) para maximizar su utilidad neta, pero no puede usar más horas-hombre de las disponibles y no quiere producir más de lo que puede vender.

### Documentación
https://pypi.org/project/PuLP/

https://coin-or.github.io/pulp/

## Fórmula Matemática
<img width="637" alt="formula" src="https://user-images.githubusercontent.com/97414922/224586331-9bb8dfe7-2b8d-4cbc-afdf-aaa2829f0ae5.png">

### Parámetros
- Ai = Número máximo de smartphones tipo i a vender este mes, donde i pertenece al conjunto {Lua1, Lua2}
- Bi = Precio de venta de los smartphones modelo tipo i, donde i pertenece al conjunto {Lua1, Lua2}
- Ci = Precio de costo de los componentes de los smartphones tipo i, donde i pertenece al conjunto {Lua1. Lua2}
- Di = Costo por hora de mano de obra de montaje de los smartphones modelo tipi i, donde i pertenece al conjunto {Lua1, Lua2}
- Ei = Costo laboral por hora de prueba del modelo de smartphone tipo i, donde i pertenece al conjunto {Lua1, Lua2}
- F = Número máximo de horas de trabajo de montaje
- G = Número máximo de horas de trabajo de prueba
- Hf,i = Horas de montaje necesarias para construir cada modelo de smartphone tipo i, donde i, pertenece al conjunto {Lua1, Lua2}
- Hg,i = Horas de prueba requeridas para probar cada modelo de smartphone tipo i, donde i pertenece al conjunto {Lua1, Lua2}

### Decisión Variable
- Xi = Número de teléfonos inteligentes tipo i que se producirán este mes, donde i pertenece al conjunto {Lua1, Lua2}

También definiremos restricciones, para que no tengamos valores negativos y valores que estén fuera de los definidos en el problema de negocio.

### Restricciones
- El número de smartphones modelo i a fabricar no puede ser negativo, es decir, Xi >=0, donde i pertenece al conjunto (Lua1, Lua2).
- El número total de horas de montaje no puede ser superior al número máximo de horas de mano de obra de montaje disponibles
- El número total de horas de prueba no puede ser mayor que las horas de mano de obra de prueba máximas disponibles.
- La cantidad de teléfonos inteligentes tipo i que se producirán no puede ser mayor que la cantidad máxima de teléfonos inteligentes tipo i que se venderán en este mes, donde i pertenece al conjunto {Lua1, Lua2}
