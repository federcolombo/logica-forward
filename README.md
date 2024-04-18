# Determinación de la Campaña para Contratos Forward de Cultivos Agrícolas en Argentina

## Ciclo de Cultivos Agrícolas en Argentina
A continuación se detallan los ciclos típicos de siembra y cosecha para los principales cultivos en Argentina:

- **Soja**
  - **Siembra**: Octubre a Diciembre
  - **Cosecha**: Marzo a Mayo

- **Maíz**
  - **Siembra**: Septiembre a Diciembre
  - **Cosecha**: Febrero a Junio

- **Trigo**
  - **Siembra**: Mayo a Julio
  - **Cosecha**: Noviembre a Enero

- **Girasol**
  - **Siembra**: Septiembre a Diciembre
  - **Cosecha**: Enero a Marzo

- **Sorgo**
  - **Siembra**: Septiembre a Diciembre
  - **Cosecha**: Marzo a Mayo

Estos periodos son aproximados y pueden variar dependiendo de las condiciones climáticas específicas de cada año y región.

## Descripción General
Este script está diseñado para determinar el año de campaña agrícola para contratos forward de varios cultivos basándose en el mes y año especificado. Soporta múltiples cultivos, incluyendo soja, maíz, trigo, girasol y sorgo, teniendo en cuenta sus ciclos específicos de siembra y cosecha en Argentina.

## Funcionalidad
La función `determinar_campana` calcula el año de campaña para un cultivo dado, mes forward y año. Utiliza diccionarios predefinidos para manejar el inicio de los períodos de cosecha y, para algunos cultivos como el trigo, el final del período de cosecha que puede extenderse al siguiente año calendario.

### Componentes Clave:
- **Diccionario `inicio_cosecha`**: Especifica el mes de inicio de la cosecha para cada cultivo. Esto es crucial para determinar cuándo comienza la nueva campaña de comercialización del cultivo.
- **Diccionario `fin_cosecha`**: Utilizado específicamente para cultivos como el trigo, donde el período de cosecha se extiende al siguiente año calendario.
- **Diccionario `meses`**: Convierte los números de los meses a sus correspondientes abreviaturas en español.

### Lógica Explicada:
- Para cultivos como el trigo, que tienen un período de cosecha que cruza al año siguiente, la función verifica si el mes forward especificado está dentro del período de cosecha. Si es así, asigna el año de campaña en función de si el mes está al inicio o al final del período de cosecha.
- Para otros cultivos, si el mes forward es antes del inicio de la cosecha, se asigna a la campaña del año anterior. De lo contrario, pertenece a la cosecha nueva que comenzó con la siembra del año anterior.

## Uso
Para utilizar este script, simplemente proporcione el cultivo, el mes y el año del contrato forward a la función `determinar_campana`, y obtendrá el año de campaña correspondiente. Esto es útil para administradores de riesgo, traders y analistas en el sector agrícola que necesitan determinar el ciclo de cultivo aplicable para sus contratos forward.
