# DermatoscopIA

Antes de tratar una lesión pigmentada: dermatoscopia y criterio de derivación. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/dermatoscopia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24203717.svg)](https://doi.org/10.5281/zenodo.24203717)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Sexta app del [Kit EstéticIA](https://fborrasumh.github.io/kitesteticia/): la valoración de una lesión pigmentada antes de cualquier tratamiento estético. Ninguna mancha se trata sin nombre.

- **La lesión**: localización, tamaño, tratamiento que se plantea, descripción y siete señales clínicas de alarma (cambio, lesión nueva en mayores de 40 años, «patito feo», sangrado, más de 6 mm, antecedentes de melanoma, nódulo reciente).
- **Dermatoscopia**, puntuada por el médico:
  - Regla ABCD de Stolz con el cálculo del TDS paso a paso.
  - Lista de tres puntos de Soyer.
  - Lista de siete puntos de Argenziano.
  - Criterios faciales de lentigo maligno de Schiffner, si la lesión está en la cara.
- **Decisión combinada**: sin criterios de alarma, vigilar o derivar, con el porqué de cada criterio. «No puedo clasificarla con seguridad» lleva a derivar. Aviso si el médico decide tratar una lesión con criterios de alarma.
- **Imágenes** anterior y actual para compararlas; se ven en el navegador y no se guardan ni se envían.
- **Informe y carta de derivación** en Word o para copiar, con las referencias de cada regla.

No usa IA ni clasifica imágenes: la app suma y combina los criterios que marca el médico. No hace ninguna llamada de red. Español, inglés y portugués.

## Referencias

- Stolz W et al. ABCD rule of dermatoscopy. Eur J Dermatol 1994;4:521-527.
- Soyer HP et al. Three-point checklist of dermoscopy. Dermatology 2004;208:27-31. doi:10.1159/000075042
- Argenziano G et al. 7-point checklist. Arch Dermatol 1998;134:1563-1570. doi:10.1001/archderm.134.12.1563
- Schiffner R et al. Early recognition of lentigo maligna using dermatoscopy. J Am Acad Dermatol 2000;42:25-32. doi:10.1016/S0190-9622(00)90005-7

## Límites

Para médicos con formación en dermatoscopia. Las reglas se aplican a lesiones melanocíticas, orientan y no diagnostican. Ante la duda, se deriva.

## Pruebas

`node tests/test_nucleo.js` (cálculo y cortes de cada regla, decisión combinada, informe y carta) y `python3 tests/smoke.py` (recorrido completo, pestaña facial, imágenes sin guardar, Word, persistencia, tres idiomas, accesibilidad WCAG 2.2 AA, CSP y móvil).

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Elena Caride Miana (Dra. Caride Medicina Estética & Antiaging).

Sexta app del Kit EstéticIA, diseñado para el alumnado del Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento (UMH).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Elena Caride Miana [0000-0002-7620-4857](https://orcid.org/0000-0002-7620-4857)

## Cómo citar

Borrás Rocher, F. y Caride Miana, E. (2026). *DermatoscopIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.24203717](https://doi.org/10.5281/zenodo.24203717)

## Licencia

MIT. Véase [LICENSE](LICENSE).
