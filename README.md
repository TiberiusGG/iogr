# Proyecto LaTeX

Este es un proyecto LaTeX con estructura tradicional.

## Estructura del proyecto

```
.
├── main.tex          # Archivo principal del documento
├── figures/          # Carpeta para imágenes y figuras
├── bibliography/     # Carpeta para archivos de bibliografía
└── README.md         # Este archivo
```

## Compilación

Para compilar el documento, puedes usar:

```bash
pdflatex main.tex
```

O si usas `latexmk`:

```bash
latexmk -pdf main.tex
```

## Requisitos

- LaTeX instalado (TeX Live, MiKTeX, etc.)
- Paquetes necesarios según el documento

