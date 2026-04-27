# 🍽️ EcoPlate Optimizer

## 🌱 Descripción
EcoPlate Optimizer es un proyecto de ciencia de datos enfocado en reducir el desperdicio de alimentos en restaurantes mediante modelos predictivos que estiman la demanda diaria.

El sistema permite anticipar cuánta comida preparar, optimizando recursos, reduciendo pérdidas económicas y promoviendo prácticas sostenibles.

## 🚨 Problema

Los restaurantes enfrentan una alta incertidumbre en la demanda:

- Preparar demasiada comida → desperdicio de alimentos  
- Preparar muy poca comida → pérdida de ventas  

En Colombia, los alimentos más desperdiciados incluyen:
- Tomate  
- Papaya  

Esto es especialmente crítico en alimentos perecederos como frutas y vegetales.

## 💡 Solución

EcoPlate Optimizer utiliza datos y modelos predictivos para:

- Predecir el número de clientes diarios  
- Estimar la demanda por tipo de plato  
- Optimizar la producción de alimentos  
- Reducir el desperdicio

## 🧠 Metodología

1. Recolección de datos  
2. Limpieza y análisis exploratorio  
3. Identificación de patrones  
4. Modelado predictivo  
5. Evaluación

## 📁 Datos simulados

El archivo `datos_simulados.xlsx` contiene múltiples hojas que representan el funcionamiento completo de un restaurante.

Estos datos fueron generados de forma simulada y utilizados para el análisis y visualización en Power BI.

## 📊 Estructura del dataset

### 1. 🧾 Ventas marzo

Contiene la demanda diaria de clientes durante el mes de marzo. 

**Variables:**
- `fecha`: día del registro  
- `dia_sem`: día de la semana  
- `tipo_dia`: entre semana o fin de semana  
- `num_clientes`: número de clientes por día  

### 2. 🍽️ Platos vendidos

Describe cuántos platos se vendieron por tipo cada día.

### Visualización menu

Vista previa del menu:

![Dashboard Preview](images/menu.png)

**Variables:**
- `fecha`  
- `total_ventas`: total de clientes ese día  
- `plato`: tipo de plato (pollo, carne, cerdo, vegetariano)  
- `cantidad_vendida`: número de platos vendidos  

### 3. 🥘 Principio del plato

Describe el tipo de acompañamiento escogido por plato.

**Variables:**
- `fecha`  
- `plato`  
- `principio`: (frijol o lenteja)  
- `cantidad`: cantidad consumida  

📌 Se utiliza para analizar patrones de preferencia de acompañamientos.

### 4. 🧂 Ingredientes por plato

Define la composición de cada plato.

**Variables:**
- `plato`  
- `ingrediente`  
- `tipo_ingrediente`: proteína, acompañamiento o principio  

📌 Permite modelar el consumo de insumos.

### 5. 💰 Precios

Contiene el precio de cada tipo de plato.

**Variables:**
- `plato`  
- `precio`  

📌 Permite calcular ingresos y rentabilidad.

### 6. 🏷️ Categorías de platos

Clasificación de los platos según su tipo.

**Ejemplo:**
- pollo → proteína  
- carne → proteína  
- cerdo → proteína  
- vegetariano → saludable  

📌 Permite segmentar análisis por tipo de producto.

## 🧠 Descripción general

El dataset simula un sistema real de un resturante tipo "corriente "donde:

- La demanda varía según el día de la semana  
- Los fines de semana presentan mayor número de clientes  
- Los clientes eligen entre diferentes tipos de platos  
- Cada plato tiene una composición de ingredientes específica  
- Se pueden estimar ingresos y consumo de insumos  

Este enfoque permite realizar análisis de:
- reducción de desperdicio (objetivo principal)
- predicción de demanda  
- optimización de producción  

## 🔗 Relación entre tablas

Las hojas están conectadas mediante:

- `fecha` → conecta ventas y platos vendidos  
- `plato` → conecta platos, ingredientes, precios y categorías  

Esto permite construir un modelo relacional en Power BI.

## 📥 Archivo

👉 [Descargar dataset completo](data/datos_simulados.xlsx)

## 📊 Dashboard en Power BI

Vista previa del dashboard desarrollado para el análisis de demanda:

![Dashboard Preview](images/dashboard.png)

## 📊 Dashboard .pbit

🔗 **Descargar plantilla Power BI (.pbit):**  
[Haz clic aquí para descargar](./dashboard.pbit)

### ¿Cómo usarlo?
1. Descargar el archivo `.pbit`
2. Abrirlo en Power BI Desktop
3. Conectar tus propios datos


### 📌 Aclaración:

En esta simulación se asume que el total de platos vendidos es igual al total de clientes.

## 📊 Análisis del dashboard

A partir de la visualización en Power BI, se identifican los siguientes hallazgos clave:

### 💰 Ingresos y volumen de ventas

- **Ingresos totales:** 59,0125 millones  
- **Total de platos vendidos:** 3,462  
- **Total de clientes:** 3,462  

### 📅 Demanda según tipo de día

- **Fin de semana:** ~60% de las ventas  
- **Entre semana:** ~40%  

📌 **Idea:**  
La demanda aumenta significativamente en fines de semana.

👉 **Recomendación:**  
Incrementar producción y abastecimiento en fines de semana, y reducir en días de baja demanda.

### 🧂 Consumo de ingredientes

Ingredientes más utilizados:

- arroz (~3.6 mil)  
- ensalada (~3.6 mil)  
- frijol (~2.0 mil)  
- presa de pollo (~1.8 mil)  

Ingredientes menos utilizados:

- tofu (~0.5 mil)  
- corte de cerdo (~0.4 mil)  

📌 **Idea:**  
Los acompañamientos básicos dominan el consumo, mientras que algunas proteínas tienen menor rotación.

👉 **Recomendación:**  
Optimizar compras enfocándose en ingredientes de alta rotación como carne y pollo y reducir inventario de baja demanda como tofu y cerdo.

### 🍽️ Preferencia de platos

- **Pollo** es el plato más vendido  
- **Carne** tiene demanda intermedia  
- **Cerdo y vegetariano** presentan menor consumo  

📌 **Idea:**  
Existe una preferencia hacia platos con pollo y carne. 

👉 **Recomendación:**  
Ajustar la producción priorizando pollo y carne, y evaluar estrategias para aumentar la demanda de opciones menos consumidas. 

### 🥘 Preferencia de acompañamientos (principio)

- En **pollo**, lenteja supera a frijol  
- En **carne**, frijol domina  
- En **cerdo**, lenteja es más frecuente  

📌 **Idea:**  
Las preferencias de acompañamiento dependen del tipo de plato.

👉 **Recomendación:**  
Preparar combinaciones optimizadas según patrones de consumo para reducir desperdicio.

### 📈 Comportamiento temporal de ventas

- Alta variabilidad diaria  
- Picos de demanda hacia finales de mes  
- Caídas en días específicos entre semana  

📌 **Idea:**  

La demanda no es constante, de manera que resulta util el uso de modelos predictivos. 

## 🧠 Conclusión del análisis

El análisis del dashboard permite evidenciar que el restaurante atendió aproximadamente 3,500 clientes durante el mes de marzo, generando ingresos aproximadamente de 60 millones de pesos, lo que refleja una operación rentable pero con oportunidades de optimización. A partir de los datos, se identifican patrones consistentes en la demanda, especialmente en función del tipo de día, donde los fines de semana presentan una mayor demanda en el consumo en comparación con los días entre semana.

Asimismo, se observa una fuerte preferencia por platos basados en pollo, seguido por la carne. Por otro lado, opciones como cerdo y vegetariano presentan baja rotación, lo que implica un mayor riesgo de desperdicio. Este comportamiento impacta directamente el consumo de ingredientes, donde insumos como arroz, ensalada y frijol muestran alta demanda, mientras que otros asociados a platos menos populares tienen menor uso.

En conjunto, estos hallazgos con las recomendaciones ofrecidas permiten transformar la operación del restaurante hacia un modelo más eficiente, en el que se optimizan recursos, se reduce el desperdicio de alimentos y se maximiza la rentabilidad.

## Actualización 27 de abril, 2026
## Analisis del tablero de visualización de datos
El tablero nos permite observar que el restaurante atendió en el mes de marzo a aproximadamente 3500 clientes, generándoles ganancias de hasta 60 millones de pesos, pues cada plato es vendido aproximadamente a 17000 pesos. Gracias al resto de datos presentados en el tablero, podremos brindarle al restaurante una predicción de que platos venderá más para que el margen de perdidas en el mes no represente mucho de esa ganancia que obtuvo al mes.
Así mismo, nos permite deducir que platos se consumen mas en que días en específico, lo que hace que podamos brindarle una predicción al restaurante sobre que alimentos son los que tendría que preparar en mayor cantidad y cuales no, dependiendo el tipo de día.
Podemos observar, gracias al gráfico de áreas titulado “Total de ventas según plato por fechas”, que el plato que cuenta con más frecuencia del menú es el pollo, aunque al inicio del mes hubo mas compra de carne, el plato que la gente mas ordenó durante el mes en general fue el pollo. También pudimos observar que el plato de cerdo y de vegetariano fueron los menos vendidos, los cuales incluso no se vendieron en algunos días.
Por otro lado, el gráfico de barras titulado “Total de ventas según plato y principio”, nos permitió observar cual fue el plato que más se vendió durante todo el mes, confirmándonos una vez más que el pollo fue el más vendido con una notoria diferencia. Este gráfico también nos permitió saber con qué principio se vendía el plato, siendo el frijol el principio más ordenado por los clientes.
En el gráfico de torta titulado “Promedio de ventas según tipo de día” nos dejo claro en que días las ventas son mayores: Los fines de semana, pues el promedio de platos vendidos un día de fin de semana es de 148, mientras que el promedio de platos vendidos de un día entre semana es de 102, presentando una amplia diferencia con respecto a los fines de semana. Esto también lo podemos observar en el gráfico “Total de ventas según plato por fechas”, pues el día que mas platos se vendieron fue un sábado, por ende, fin de semana.
De la misma forma, el gráfico de barras “Suma de cantidad por ingrediente” nos mostró cuantas porciones de cada ingrediente se vendieron ese día (una porción del ingrediente = 1), afirmándonos que los ingredientes arroz y ensalada están presentes en todos los platos, por ende, son iguales al total de platos vendidos. Así mismo, este gráfico nos muestra que el principio que más se vendió fue el frijol, y la proteína que más se vendió fue la presa de pollo, dejando al corte de cerdo como la proteína menos vendida, por consecuencia, el plato menos vendido fue el de cerdo, reafirmando nuestra conclusión previamente mencionada.
Gracias al cuadro de segmentación ubicado en la parte de arriba del tablero, podemos ver como se comporta cada gráfico según el tipo de día, permitiéndonos reafirmar que cada día entre semana se vende menos comparado con cada día del fin de semana, sin embargo, gracias a las tarjetas ubicadas en la parte superior, podemos observar que el total de platos vendido entre semana y los ingresos representan más de la mitad del total vendido. Esto se debe a que hay más días entre semana (5) que en fines de semana (2), por ende, la suma va a ser mayor, aún así esto no significa que un día de entre semana se pueda vender más que un día del fin de semana, pues si evaluamos cada día individualmente, podremos ver que los sábados y domingos se vende más que la gran mayoría de días de entre semana.

Gracias a este análisis podemos concluir que el restaurante tendría que, entre semana, tener alrededor de 100 platos preparados por día, cada uno con su respectiva porción de arroz y ensalada, contando con una mayor disposición leve de frijol respecto a la lenteja, de igual manera contando con una mayor cantidad de presas de pollo, seguido por cortes de carne y en menor cantidad el tofu y corte de cerdo.  Por otro lado, los fines de semana el restaurante tendría que preparar alrededor de 150 platos por día, con las mismas cantidades de ingredientes especificadas entre semana. 

## 👥 Equipo de trabajo

Este proyecto fue desarrollado por:

- **Juliana Hernández**  
- **María Arias**
