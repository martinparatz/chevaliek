# Formato de publicación de los informes de leyes

Cada ley se publica como una entrada de Jekyll en `_posts/`, generada automáticamente a partir del informe completo (la misma fuente que la versión en Google Docs) con el script `generar_publicacion_md.py` del proyecto.

## Archivos por ley

| Archivo | Contenido |
|---|---|
| `_posts/AAAA-MM-DD-ley-NNNNN-slug.md` | El informe. La fecha es la de publicación de la ley en el Boletín Oficial. |
| `assets/img/leyes/NNNNN/` | Hemiciclos y mapas de cohesión (PNG generados con R). |
| `assets/data/leyes/NNNNN/` | Votaciones por alineamiento y por bloque (CSV) para descarga. |

## Front matter

```yaml
layout: post
title: "Ley 27.742 (Ley Bases)"           # número y nombre corto
subtitle: "Ley de Bases y Puntos de ..."   # nombre completo
description: "..."                         # 1 oración; se usa en buscadores y redes
date: 2024-07-08                           # publicación en el BO
last_modified_at: 2026-11-16               # versión del informe
categories: [leyes]                        # alimenta el índice /leyes/
tags: [...]                                # temas
ley: 27742                                 # número, para el índice
permalink: /leyes/27742-ley-bases/
image: /assets/img/leyes/27742/hemiciclo_D5142.png   # imagen para redes
```

## Estructura del cuerpo

1. Bajada (`{: .lead }`): qué cubre el informe.
2. **Ficha técnica** en tabla (Autor, presentación, cámara de origen, media sanción, sanción con modificaciones de la revisora si la hubo, sanción, promulgación y publicación) y **Estado** destacado (`{: .estado }`).
3. Índice automático (`{:toc}`).
4. Secciones 1 a 7 del informe completo: resumen ejecutivo, trámite, contenido normativo, votaciones, debate, efectos, estado actual.
5. En **Votaciones**: recuadro «Cómo leer las tablas» (`{: .nota }`), tabla de votaciones en general, **hemiciclos** incrustados con epígrafe, tablas por bloque, votaciones en particular **plegadas** (`<details>`) y mapas de cohesión.
6. Fuentes, método y confianza; **Datos y código** (CSV); **Cómo citar**.

## Convenciones

- Cámaras: HCDN, HSN y PEN. Fechas del trámite: `dd/mm/aaaa - Tipo de sesión - Cámara`.
- Cada celda de alineamiento: `Sí/No/Abst. (R índice de Rice)`.
- Lo que proviene de medios se marca **[prensa]**.
- Imágenes y enlaces internos con `{{ '/ruta' | relative_url }}` para que funcionen con o sin `baseurl`.

## Vista previa local

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000/chevaliek/
```
