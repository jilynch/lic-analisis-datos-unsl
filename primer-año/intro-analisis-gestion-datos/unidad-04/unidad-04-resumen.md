# Resumen: Medidas de Tendencia Central y de Dispersión - Asimetría y Curtosis

## Contexto en el Proceso de Investigación

El análisis estadístico se sitúa principalmente en la 4ª etapa del proceso de investigación, el **Procesamiento de datos**, donde se busca reducir la información a cifras significativas, y en la 5ª etapa de **Explicación e interpretación** para dar sentido a los resultados.

## Medidas de Tendencia Central (MTC)

Son valores típicos que representan un conjunto de datos agrupándose en torno al centro de la distribución. Su valor práctico reside en la reducción del conjunto inicial de observaciones.

**Media Aritmética ($\overline{X}$)**
Es la medida más representativa, calculada sumando todos los valores divididos por el número total de observaciones. Requiere un nivel de medición intervalar o métrico. Aunque es la más usada, se ve afectada por valores extremos y siempre debe complementarse con una medida de dispersión.

**Mediana ($\tilde{X}$)**
Es el valor que ocupa la posición central de la distribución cuando los datos están ordenados, dejando el 50% de los datos a su izquierda y el otro 50% a su derecha. Es una medida robusta, lo que significa que **no se ve afectada por valores extremos**.

**Moda ($\hat{X}$)**
Es el valor (o valores) que se presenta con mayor frecuencia. Puede calcularse para cualquier nivel de medición y la distribución puede ser unimodal, bimodal, multimodal o amodal.

## Medidas de Posición: Percentiles

Indican el valor de la variable por debajo del cual se encuentra un porcentaje dado de observaciones. Para calcular cualquier percentil $i$-ésimo ($P_i$), primero se deben ordenar los datos y calcular su posición específica en la muestra.

## Medidas de Dispersión (MD)

Las MTC reducen la información a un solo valor, por lo que las MD son necesarias para indicar la variabilidad (concentración o dispersión) de los datos en torno a la medida central. Se calculan solo para variables cuantitativas.

**Rango o Recorrido ($R$)**
Es la primera aproximación a la dispersión (diferencia entre el máximo y el mínimo). Considera solo los extremos sin tener en cuenta el interior de la distribución.

**Rango Intercuartílico ($R_I$)**
Es la diferencia entre el tercer cuartil ($P_{75}$) y el primer cuartil ($P_{25}$). Es la medida adecuada cuando la distribución presenta valores extremos, ya que indica cuántas unidades contienen al 50% central de la distribución.

**Varianza ($S^2$) y Desviación Estándar ($S$)**
La varianza es el promedio de los desvíos al cuadrado respecto de la media; las desviaciones grandes influyen mucho en el resultado. La **Desviación Estándar** es la raíz cuadrada de la varianza; su ventaja es que mantiene las mismas unidades que los datos originales.

**Desviación Absoluta respecto a la Mediana (MAD)**
Frente a la presencia de **valores extremos (outliers)**, es conveniente usar la Mediana en lugar de la Media, y la MAD es la medida de dispersión adecuada para acompañarla. Se calcula como la mediana de los valores absolutos de las distancias entre cada dato y la mediana.

**Coeficiente de Variación ($CV$)**
Es una medida de dispersión relativa (adimensional, expresada en porcentaje). Es fundamental para decidir la fiabilidad de la media aritmética.

* **Regla de decisión:** Si el $CV \leq 20\%$, la media se considera **representativa** del conjunto de datos.

## Momentos, Asimetría y Curtosis

Los momentos son valores esperados que caracterizan la distribución. El 3º momento se relaciona con la asimetría y el 4º con la curtosis.

**Coeficiente de Asimetría de Fisher ($A_s$)**
Evalúa el comportamiento de los datos alrededor de la media:

* **$A_s > 0,3$ (Positiva):** Mayor concentración de valores a la izquierda [cola a la derecha].
* **$-0,3 \leq A_s \leq 0,3$ (Simétrica):** Distribución aproximadamente simétrica.
* **$A_s < -0,3$ (Negativa):** Mayor concentración de valores a la derecha [cola a la izquierda].

**Coeficiente de Curtosis ($C_U$)**
Mide el grado de agrupamiento de las observaciones en torno a la media [apuntamiento]:

* **$C_U > 0,3$ (Leptocúrtica):** Alta concentración, más homogénea respecto a la media.
* **$-0,3 \leq C_U \leq 0,3$ (Mesocúrtica):** Distribución normal o uniforme respecto a la media.
* **$C_U < -0,3$ (Platicúrtica):** Baja concentración, más heterogénea [aplanada].

# Formulario Completo - Unidad 4

### Medidas de Tendencia Central

* **Media Aritmética:**
    $$\overline{X} = \frac{\sum_{i=1}^{n} x_i}{n}$$
* **Posición de la Mediana:**
    $$(\tilde{X})_0 = \frac{n}{2} + 0,5$$
    *(Nota: Si n es par, se promedian los dos valores centrales; si es impar, es el valor en la posición exacta)*.

### Medidas de Posición

* **Posición del Percentil ($P_i$):**
    $$(P_i)_0 = \frac{(i \times n)}{100} + 0,5$$

### Medidas de Dispersión

* **Rango:**
    $$R = x_{Max} - x_{Min}$$
* **Rango Intercuartílico:**
    $$R_I = P_{75} - P_{25}$$
* **Varianza:**
    $$S^2 = \frac{\sum_{i=1}^{n} (x_i - \overline{X})^2}{n - 1}$$
* **Desviación Estándar:**
    $$S = \sqrt{S^2}$$
* **MAD (Median Absolute Deviation):**
    $$MAD = Mediana \{ |x_1 - \tilde{X}|, |x_2 - \tilde{X}|, ..., |x_n - \tilde{X}| \}$$
* **Coeficiente de Variación:**
    $$CV = \frac{S}{|\overline{X}|} \times 100$$

### Asimetría y Curtosis

* **Coeficiente de Asimetría (Fisher):**
    $$A_S \cong \frac{m_3}{S^3}$$
    *Donde $m_3 = \frac{\sum (x_i - \overline{X})^3}{n}$*

* **Coeficiente de Curtosis:**
    $$C_U \cong \frac{m_4}{S^4} - 3$$
    *Donde $m_4 = \frac{\sum (x_i - \overline{X})^4}{n}$*
