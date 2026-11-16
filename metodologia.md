---
layout: page
title: Metodología
permalink: /metodologia/
---

- **Votaciones nominales:** actas de votaciones.hcdn.gob.ar y senado.gob.ar/votaciones, una por acta, con hash SHA-256 del documento descargado.
- **Alineamiento:** cada bloque se clasifica como Oficialismo (LLA), Aliado (PRO, UCR, MID y afines), Dialoguista (bloques provinciales y federales) u Oposición (UxP/Justicialismo, izquierda).
- **Índice de Rice:** |A − N| / (A + N), donde A son los votos afirmativos y N los negativos del grupo. 1 = el grupo votó unido; 0 = partido al medio.
- **Bloques del Senado:** los vigentes a la fecha de cada sesión, tomados del «Listado por bloques» del Senado archivado en web.archive.org (la página de cada acta muestra el bloque actual).
- **Debate parlamentario:** versiones taquigráficas del Senado y Diarios de Sesiones de Diputados, segmentados por orador; los términos distintivos se calculan con log-odds por alineamiento.
- **Gráficos:** hemiciclos y mapas de cohesión generados con R (ggplot2) a partir de la base del proyecto.
- **Fuentes de prensa:** lo marcado **[prensa]** proviene de medios y no de fuentes oficiales (confianza media).
