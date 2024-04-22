## Valores NaN

Para las variables categóricas como `sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, `ca` y `thal`, los valores NaN no pueden simplemente rellenarse con promedios. En estos caso valoraremos:

- Eliminar las filas si el número de casos faltantes no es significativo en comparación con el tamaño del dataset.
- Imputar los NaN basándote en la moda (el valor más frecuente) de la columna, o mediante un modelo de imputación más sofisticado.

Para variables continuas como `age`, `trestbps`, `chol`, `thalach` y `oldpeak`, puedes:

- Imputar los valores faltantes con la media o la mediana de la columna, dependiendo de la distribución (la mediana es menos sensible a los valores atípicos).

## Valores Atípicos o Incorrectos

- `chol`: Un valor de -9 es claramente incorrecto, ya que el colesterol no puede ser negativo. Este valor debería tratarse como un valor faltante.
- `slope`, `ca` y `thal`: Los valores de -9 no son válidos según la descripción. Estos también deberían ser tratados como valores faltantes.
- Para `ca` y `thal`, que son categóricas pero tienen NaN, lo mejor sería imputar según la moda o algún método de imputación multivariante si no quieres perder datos eliminando filas.
- Para `fbs`: Si el NaN es significativo (es decir, el dato no fue recogido o se desconoce), podría ser apropiado imputar con la moda dado que es una variable binaria.

## Consistencia de Datos

Hay que asegurar que todas las variables categóricas (como `cp`, `restecg`, `slope`, `ca` y `thal`) tengan valores dentro del rango esperado. Los valores fuera de rango deben ser tratados como faltantes o corregidos si es un error claro.

## Datos de Frecuencia Cardíaca (`thalach`)

Si hay valores extremadamente bajos o altos que no son fisiológicamente posibles, los consideraremos como errores de entrada y tratarlos como valores faltantes.

## Análisis y Decisión Basada en el Dominio

Tenémos que tener una consideración del conocimiento del dominio. Por ejemplo, si la variable `oldpeak` tiene un valor de 0, esto podría ser válido, pero si se supone que es un valor continuo y el 0 indica que no se tomó la medida, entonces deberías tratarlo según corresponda.
