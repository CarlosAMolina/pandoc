---
geometry: "left=25mm,right=25mm,top=10mm,bottom=25mm"
output: pdf_document
fontsize: 14pt
mainfont: DejaVuSerif.ttf
toc: true
toc-title: Índice
colorlinks: true
header-includes: 
- \usepackage[document]{ragged2e}
---

## Introducción

En este documento se explica diversos temas de sumo interés.

## Base de datos

La base de datos utilizada actualmente es `PostgreSQL`.

Las principales tablas a emplear son:

- foo.t_example_data_with_important_values: información muy importante sobre datos innecesarios.
- bar.t_second_exampe_data: más datos parecidos a los de la otra tabla pero diferentes.

Las vistas disponibles actualmente son las siguientes:

- foo.v_all: todos los datos habidos y por haber. Combinación de las tablas foo.t_example_data_with_important_values y bar.t_second_exampe_data.

En caso de duda sobre los datos, por favor buscar información en <https://duckduckgo.com>.

Ejemplo de petición de datos:

```sql
SELECT
  *
FROM
  foo.v_all
;
```

