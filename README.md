# filminas-IS

Presentaciones de Ingeniería de Software, escritas en Markdown y renderizadas con
[reveal-md](https://github.com/webpro/reveal-md).

**Ver online:** https://franciscoameri.github.io/filminas-IS/

Fork de [UBP-IngenieriaSoftware/filminas](https://github.com/UBP-IngenieriaSoftware/filminas).

---

## Uso local

Requiere [Node.js](https://nodejs.org/) (v20 o superior).

```bash
npm install          # instala reveal-md y gh-pages
npm start            # levanta el servidor en modo watch (http://localhost:1948)
npm run build        # genera el sitio estatico en ./public
```

`npm start` recarga el navegador automaticamente al guardar un archivo de `slides/`.

## Estructura

```
slides/
  U*.md              # un archivo Markdown por unidad
  index.html         # portada con el listado de presentaciones
  css/filminas.css   # estilos propios
  images/            # imagenes de las filminas
  starUML/           # fuentes de los diagramas UML
reveal-md.json       # separadores de slide y CSS custom
reveal.json          # opciones de reveal.js
```

## Como escribir las filminas

- `---` separa slides horizontales (tema nuevo).
- `----` separa slides verticales (subtemas del mismo bloque).
- El front-matter de cada archivo define titulo y tema:

```markdown
---
title: Procesos de Software
theme: solarized
slideNumber: true
---
```

- Para ajustar el tamaño de fuente de una slide:
  `<!-- .slide: style="font-size: 0.80em" -->`
- Las respuestas de los ejercicios van en comentarios HTML (`<!-- ... -->`),
  asi quedan en el fuente pero no se proyectan.
- Las imagenes se referencian como `images/unidadX/archivo.png`.

## Deploy

El workflow `.github/workflows/buildAndDeploy.yml` compila el sitio y lo publica
en la rama `gh-pages` en cada push a `main`. Para que funcione:

1. **Settings → Pages** → Source: *Deploy from a branch* → rama `gh-pages`, carpeta `/ (root)`.
2. **Settings → Actions → General** → Workflow permissions: *Read and write permissions*.

Tambien se puede publicar a mano con `npm run deploy`.

## Referencias del material

Basado principalmente en *Ingeniería de Software* de Ian Sommerville y en
*Ingeniería de Software: un enfoque práctico* de Roger Pressman.

Material de consulta:

- [Procesos de software – Unidad 2 (SlideShare)](https://es.slideshare.net/MatiasGonzaloAcosta/procesos-de-software-unidad-2-software-enginnering-ian-sommerville)
- [SlidePlayer 17988345](https://slideplayer.es/slide/17988345/) · [SlidePlayer 18133590](https://slideplayer.es/slide/18133590/)
- [Diagramas de secuencia](https://es.slideshare.net/rene5254/diagramas-de-secuencia-251060499) · [Diagramas de clases](https://diagramasuml.com/diagrama-de-clases/)

Herramientas utiles:

- [Formateador de Markdown](https://codebeautify.org/markdown-formatter)
- [Tablas de Markdown a HTML](https://markdowntohtml.com/)
