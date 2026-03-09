# Alura-store-Latam
# Análisis de Datos para Decisión Estratégica

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-green)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7%2B-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-MIT-yellow)

**Análisis exhaustivo de datos de ventas de 4 tiendas para determinar cuál vender**

[Descripción](#descripción) • [Instalación](#instalación) • [Uso](#uso) • [Resultados](#resultados) • [Autor](#autor)

</div>

---

## Descripción

Este proyecto realiza un **análisis completo de datos** de las 4 tiendas de la cadena Alura Store para ayudar al Sr. Juan a tomar una decisión informada sobre **qué tienda vender** para poder iniciar un nuevo emprendimiento.

### Objetivo

Identificar la tienda con menor rendimiento a traves el análisis de múltiples métricas clave como las siguientes:

- **Ingresos totales** por tienda
- **Satisfacción del cliente** (calificaciones)
- **Categorías y productos** más/menos vendidos
- **Costos de envío** promedio
- **Puntuación integral** ponderada

### Metodología

El análisis se basa en **9,435 transacciones** reales distribuidas en 4 tiendas ubicadas en diferentes ciudades de Colombia. Se utilizó un enfoque cuantitativo con:

1. **Análisis exploratorio de datos (EDA)**
2. **Análisis estadístico descriptivo**
3. **Visualizaciones comparativas**
4. **Sistema de puntuación ponderada** (Ingresos 40%, Satisfacción 30%, Eficiencia 30%)
5. **Informe ejecutivo** con recomendaciones

---

## Tecnologías Utilizadas

| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| **Python** | 3.8+ | Lenguaje de programación |
| **Pandas** | 2.0+ | Manipulación y análisis de datos |
| **Matplotlib** | 3.7+ | Visualización de datos |
| **NumPy** | 1.24+ | Operaciones numéricas |
| **Google Colab** | - | Entorno de desarrollo |

---

## Instalación

### Requisitos Previos

- Python 3.8 o superior
- Conexión a Internet (para cargar datos desde GitHub)
- Navegador web (para usar los notebooks de Google Colab)

### Opción 1: Google Colab (Recomendado ya que en este caso fue el que yo use)

1. **Abre Google Colab**: [https://developers.google.com/colab)

2. **Sube el notebook**: 
   - Click en `Archivo` → `Subir notebook`
   - Selecciona `AluraStoreLatam.ipynb`

3. **Ejecuta las celdas**: 
   - Click en `Entorno de ejecución` → `Ejecutar todas`

**¡Listo!** No necesitas instalar dependencias, Colab ya cuenta con estas.

### Opción 2: Entorno Local

1. **Clona el repositorio**:
```bash
git clone https://github.com/tu-usuario/alura-store-analysis.git
cd alura-store-analysis
```

2. **Crea un entorno virtual**:
```bash
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

3. **Instala las dependencias**:
```bash
pip install pandas matplotlib numpy jupyter
```

4. **Ejecuta Jupyter Notebook**:
```bash
jupyter notebook AluraStoreLatam.ipynb
```

---

## Uso

### Ejecución Paso a Paso

El notebook está dividido en secciones marcadas:

#### 1️**Importación de Datos**
```python
# Los datos se cargan automáticamente desde GitHub
tienda = pd.read_csv(url)
tienda2 = pd.read_csv(url2)
tienda3 = pd.read_csv(url3)
tienda4 = pd.read_csv(url4)
```

#### 2️**Análisis de Ingresos**
- Calcula ingresos totales por tienda
- Identifica la tienda con mayores/menores ingresos
- Compara con el promedio

#### 3️**Análisis de Categorías**
- Ventas por categoría de producto
- Top 3 categorías más vendidas
- Distribución porcentual

#### 4️**Análisis de Satisfacción**
- Calificación promedio por tienda
- Distribución de calificaciones (1-5 estrellas)
- % de calificaciones positivas/negativas

#### 5️**Análisis de Productos**
- Top 10 productos más vendidos
- Productos menos vendidos
- Productos exclusivos por tienda

#### 6️**Análisis de Costos de Envío**
- Costo promedio de envío
- Comparación entre tiendas
- Impacto en el cliente

#### 7️**Visualizaciones**
- 4 gráficos principales:
  - Ingresos totales (barras)
  - Calificaciones (barras + distribución)
  - Costos de envío (barras horizontales)
  - Dashboard comparativo (4 subgráficos)

#### 8️**Informe Final**
- Recomendación basada en datos
- Justificación detallada
- Análisis de fortalezas/debilidades

### Ejecución Rápida

Para ejecutar todo el análisis de una vez:

1. Abre el notebook en Google Colab
2. Click en `Entorno de ejecución` → `Ejecutar todas`
3. Espera 30-60 segundos
4. ¡Revisa los resultados!

---

### Recomendación Final

**VENDER TIENDA 4**

### Métricas Clave

| Tienda | Ingresos | Calificación | Costo Envío | Puntuación |
|--------|----------|--------------|-------------|------------|
| Tienda 1 | $1,150.88M | 3.98/5.00 | $26,018 | 63.86/100 |
| Tienda 2 | $1,116.34M | 4.04/5.00 | $25,216 | **63.95/100**  |
| Tienda 3 | $1,098.02M | 4.05/5.00 | $24,806 | 63.85/100 |
| **Tienda 4** | **$1,038.38M** | 4.00/5.00 | $23,459 | **63.02/100** |

### Hallazgos Clave

1. **Tienda 4** genera **10.8% menos ingresos** que la mejor tienda
2. Diferencia de **$112.50M COP** con respecto a Tienda 1
3. Aunque tiene los **menores costos de envío**, no compensa la falta de ventas
4. Todas las tiendas tienen **calificaciones similares** (3.98-4.05)
5. El problema es la **capacidad de generar ingresos**, no la satisfacción

### Razones para Vender Tienda 4

**Bajo rendimiento financiero** ($1,038M vs $1,151M de la mejor)  
**Puntuación más baja** (63.02/100)  
**Menor cantidad de ventas**  
**Recursos subutilizados**  
**Oportunidad de reinversión** en tiendas exitosas  

---

##  Visualizaciones

El proyecto genera 4 gráficos profesionales:

### 1. Ingresos Totales
- Gráfico de barras comparativo
- Código de colores (verde=mejor, rojo=peor)
- Valores en millones sobre cada barra

### 2. Satisfacción del Cliente
- Calificación promedio (barras)
- Distribución de calificaciones (barras apiladas)
- Líneas de referencia (4.0 = buena, 3.5 = aceptable)

### 3. Costos de Envío
- Barras horizontales
- Ordenadas de más económica a más costosa
- Código de colores según eficiencia

### 4. Dashboard Comparativo
- 4 subgráficos en uno:
  - Ingresos
  - Calificaciones
  - Costos de envío
  - Cantidad de ventas

---

## Datos

### Fuente de Datos

Los datos provienen de archivos CSV alojados en GitHub (repositorio oficial de Alura):

```
https://github.com/alura-es-cursos/challenge1-data-science-latam/
```

### Estructura de Datos

Cada archivo CSV contiene las siguientes columnas:

| Columna | Tipo | Descripción |
|---------|------|-------------|
| `Producto` | String | Nombre del producto |
| `Categoría del Producto` | String | Categoría (Muebles, Electrónicos, etc.) |
| `Precio` | Float | Precio de venta en COP |
| `Costo de envío` | Float | Costo de envío en COP |
| `Fecha de Compra` | String | Fecha de la transacción |
| `Vendedor` | String | Nombre del vendedor |
| `Lugar de Compra` | String | Ciudad de la compra |
| `Calificación` | Integer | Calificación del cliente (1-5) |
| `Método de pago` | String | Forma de pago |
| `Cantidad de cuotas` | Integer | Número de cuotas |
| `lat` | Float | Latitud |
| `lon` | Float | Longitud |

### Estadísticas del Dataset

- **Total de transacciones**: 9,435
- **Tienda 1**: 2,359 transacciones
- **Tienda 2**: 2,360 transacciones
- **Tienda 3**: 2,359 transacciones
- **Tienda 4**: 2,357 transacciones
- **Período**: 2020-2022
- **Ubicaciones**: 19 ciudades de Colombia

---

## Insights y Aprendizajes

### Insights del Negocio

1. **Los envíos baratos no garantizan ventas**: Tienda 4 tiene los menores costos de envío pero los menores ingresos
2. **Calificaciones homogéneas**: Las 4 tiendas tienen satisfacción similar (3.98-4.05), lo que indica que el problema no es la calidad del servicio
3. **Categorías consistentes**: Los productos más vendidos son los mismos en todas las tiendas
4. **Gestión es clave**: Con los mismos productos, unas tiendas venden más que otras

### Aprendizajes Técnicos

- Análisis exploratorio de datos con Pandas
- Visualización efectiva con Matplotlib
- Creación de sistemas de puntuación ponderada
- Análisis estadístico descriptivo
- Presentación de resultados de forma ejecutiva

---

## Contribuciones

Toda contribuciones es bienvenida, esto sirve para poder avanzar. En el caso de que quieras mejorar este proyecto:

1. Fork el repositorio
2. Crea una rama (`git checkout -b feature/mejora`)
3. Commit tus cambios (`git commit -m 'Agrega nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/mejora`)
5. Abre un Pull Request

---
## Autor

**Tu Jostyn Yesid Reyes**

- LinkedIn: (www.linkedin.com/in/yesid-reyes-348844324)
- Email: jostynreyes.jr@gmail.com

---

## Agradecimientos

- **Alura Latam** Muchisimas gracias por proporcionar el dataset y el desafío
---

** Espero que este proyecto sea de su agrado y que puedan aprender con el.**

Hecho por Yesid

</div>
