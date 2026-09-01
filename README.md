# Un código, muchos destinos

Explicador interactivo y bilingüe (español / inglés) del trabajo
***Lost in Harmonization: Definitional Uncertainty in Occupational Crosswalks***.

**Página en vivo:** https://etorresram.github.io/crosswalk-explainer/

Autor: Eric Torres Ramírez

## Qué muestra

Las tablas de correspondencia entre clasificaciones de ocupaciones no son
funciones: un mismo código nacional suele admitir varias categorías
internacionales, y la tabla no dice cuál elegir. Quien procesa los datos decide,
y esa decisión no queda registrada. El explicador recorre en ocho escenas lo que
esa decisión invisible implica, medido sobre la encuesta de hogares de Estados
Unidos de 2019 y las tablas oficiales de correspondencia:

| | |
|---|---|
| Empleo con más de un destino admisible | 48,8 % |
| Ambigüedad de origen doméstico, no internacional | 16,1 % |
| Incertidumbre de definición frente a la muestral, a 2 dígitos | 1,74× |
| Códigos que se fijan al exigir que cuadren los totales publicados | 2 de 89, y 0 con holgura mínima |

## Cómo está hecho

Un solo archivo, `index.html`, sin dependencias ni paso de compilación: todo el
CSS y el JavaScript van en línea y los gráficos son SVG generados en el momento.
Lo único externo son las tipografías de Google Fonts, que degradan a fuentes del
sistema si no cargan.

- **Bilingüe.** El botón de la barra superior intercambia textos, narraciones,
  rótulos de las figuras y el separador decimal. El castellano se toma del propio
  documento y solo el inglés vive en el diccionario, de modo que no hay dos
  copias del mismo texto que puedan quedar desincronizadas.
- **Narración por voz.** Usa la Web Speech API del navegador. Las voces
  disponibles las pone el sistema operativo; se ordenan por calidad (las de red
  primero, marcadas con ✦) y recién después por género.
- **Accesibilidad.** Paleta validada para daltonismo (separación ΔE 17,3 en
  deuteranopia), navegación por teclado y respeto de `prefers-reduced-motion`.

## Reproducibilidad

Las cifras salen de los guiones de análisis del proyecto, en un repositorio
aparte. Los microdatos de IPUMS no se redistribuyen aquí porque sus condiciones
de uso no lo permiten.

## Licencia

Contenido bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es).
