# Books to Scrape Spider

Este proyecto utiliza **Scrapy** para extraer información de libros desde el sitio [Books to Scrape](http://books.toscrape.com/).  
El script `BookstoScrapeTwo.py` recorre todas las páginas del catálogo y extrae datos como título, precio, disponibilidad y calificación.

---

## 📌 Requisitos

- Python 3.7+
- [Scrapy](https://scrapy.org/) instalado

Instalar Scrapy con:

```
bash
pip install scrapy

```
---

## 🚀 Uso
Guarda el archivo BookstoScrapeTwo.py dentro de un proyecto de Scrapy (por ejemplo, en la carpeta spiders/).

Para instalar Scrapy:

```bash
pip install scrapy

```
Ejecuta el spider desde la carpeta raíz del proyecto:

```
bash
scrapy runspider BookstoScrapeTwo.py -o libros.json

```
El parámetro -o permite guardar los resultados en un archivo (.csv, .json, .jl).

---

## 📄 Datos extraídos
El spider obtiene para cada libro:

title → Título del libro

price → Precio (en libras esterlinas)

availability → Disponibilidad (por ejemplo, "In stock")

rating → Calificación en estrellas (One, Two, Three, Four, Five)

---

## 🛠 Funcionamiento del código
start_urls: comienza en la página 1 del catálogo.

parse: extrae la información de cada libro usando selectores CSS.

Paginación: sigue el enlace "next" para recorrer todas las páginas.

---

## 📁 Estructura
```
books_spider/
│
├── books_spider.py       # Código del spider
├── README.md             # Documentación del proyecto

```
---

## ⚖ Licencia
Este código es solo para fines educativos y de práctica de web scraping.
Verifica siempre las políticas de uso del sitio web antes de extraer datos. 