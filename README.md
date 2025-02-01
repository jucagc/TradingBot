# 📊 Proyecto de Bot de Trading de Bitcoin	📈

<p align="center">
  <img src="imagenes/bot_trading1.jpeg" alt="Bot_Trading" width="350">
</p>


## 📈 Objetivo del Proyecto❕ 
Este proyecto tiene como objetivo crear un bot de trading
automatizado que analice el comportamiento del precio de
Bitcoin en tiempo real y tome decisiones de compra, venta o
mantener, basándose en medias móviles simples y
tendencias de mercado.

## ❓❓ Preguntas Claves
- ¿Como se comporta el precio del Bitcoin con el comportamiento del Dólar?
- ¿Como vamos a extraer y de donde la información para su análisi?
- ¿Cuales criterios se usarán para tomar una decisión si comprar o vender?
- ¿Cómo se implementará el Bot?

## ⚙️ Herramientas Utilizadas 
- pandas y numpy para manipulación de datos.
- yfinance para obtener datos financieros de Bitcoin.
- matplotlib para visualización de datos.
- requests y BeautifulSoup para scraping

## Ambiente
Para poder ejecutar el proyecto se ocupan las siguientes bibliotecas instaladas:
```bash
pip install yfinance beautifulsoup4 matplotlib seaborn pandas numpy
```
## 📥 Recopilacion y Tratamiento de Datos
### 📂 Importación de Datos
Se necesitan datos históricos de Bitcoin para el análisis y el desarrollo del algoritmo.
Todos los precios actuales del mercado se descargan mediante la url = "https://coinmarketcap.com/currencies/bitcoin/" de CoinMarketCap utilizando BeautifulSoup.

### 🧹 Limpieza de Datos
Para la limpieza de edatos se usan 2 criterios clave para su uso:
- 📋 **Valores duplicados**: Eliminamos registros con índices duplicados.
- 🧽 **Valores nulos**: Rellenamos los valores faltantes usando el ultimo valor valido

## 📊 Cálculo de SMA
esta es una referencia sobre el tema de SMA:
- **SMA Corto (10 períodos):**
Se calcula sobre los últimos 10 períodos de 5 minutos.
Esto equivale a 50 minutos (10 × 5 minutos).
Es una SMA de corto plazo que reacciona rápidamente a los cambios de precio.

- **SMA Largo (50 períodos):**
Se calcula sobre los últimos 50 períodos de 5 minutos.
Esto equivale a 250 minutos (50 × 5 minutos), que es aproximadamente 4 horas y 10 minutos.
Es una SMA de largo plazo que suaviza las fluctuaciones y refleja la tendencia general.

## ⌨️ Desarrollo del Algoritmo
- **ESTRATEGIA:** Se define una estrategia de trading basada en SMA, especificando las señales de compra y venta.
- **SMA Lenta y Rapida:** Se utilizan dos SMAs con períodos diferentes (uno lento y uno rápido) para generar señales.
- **Cruces:** Se identifican las cruces entre las SMAs para generar señales de compra o venta.

## 💻 Implementacion
- **Web Scrapping**
API Yahoo finance
https://coinmarketcap.com/currencies/bitcoin/
- **Integracion de SMA**
Se implementa la estrategia SMA en el código, utilizando las funciones de la biblioteca para calcular las SMAs y generar señales.
- **Visualizacion**
Se utiliza matplotlib para mostrar la tendencia del Bitcoin y las gráficas de los SMA

## 💡 Conclusiones
- El código proporciona una base sólida para el análisis de trading automatizado en Bitcoin.
- a SMA (Media Móvil Simple) es una herramienta fundamental en el análisis técnico que permite a los traders identificar tendencias, generar señales de compra/venta y filtrar el ruido del mercado.
-El trading de criptomonedas implica riesgos, por lo que es fundamental gestionar el riesgo.

