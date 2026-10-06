# Contratación Acuavalle 2024–2026

Tablero de consulta de los contratos, convenios y otrosíes publicados por **Acuavalle S.A. E.S.P.** en su sitio web
([Información sobre procesos de contratación](https://www.acuavalle.gov.co/informacion-sobre-procesos-de-contratacion-2/)),
vigencias 2024, 2025 y 2026.

**Ver el tablero:** https://jlzmontenegro.github.io/contratacion-acuavalle/

## Qué contiene

- `index.html`: tablero con filtros (vigencia, tipo, categoría, contratista, periodo antes/después de una fecha de corte,
  rango de fechas y de valores, búsqueda de texto), gráficas, tabla de resultados con enlace al PDF original de cada
  contrato y exportación a Excel y PDF.
- `contratacion_acuavalle_2024_2026.xlsx`: la misma información en Excel, con hojas de resumen por categoría, valor por
  tipo y vigencia, y la lista de contratos que requieren revisión manual.

## Campos por contrato

Entidad(es) contratante(s), número, fecha de firma, fecha de inicio, fecha de fin, plazo, objeto, síntesis de las
obligaciones específicas, valor, resumen de la forma de pago, contratista(s) y NIT, categoría de gasto, enlace a la fuente
y observaciones.

## Cómo se construyó

1. Se recorrieron las secciones de contratación 2024, 2025 y 2026 del sitio y se descargaron los documentos enlazados.
2. Se conservaron solo contratos, convenios y otrosíes. Se excluyeron órdenes de compra/servicio/trabajo/consultoría,
   actas de erogación, avisos precontractuales y otros documentos no contractuales.
3. Los PDF son escaneos: se leyeron con OCR (Tesseract en todas las páginas y RapidOCR como segunda lectura de las
   portadas con datos dudosos).
4. Los campos se extrajeron con reglas sobre el texto del documento. **No se completan datos por inferencia**: si un dato
   no aparece en el documento, el campo queda vacío y se explica en "Observaciones".
5. El valor se verifica comparando la cifra con el valor escrito en letras del mismo documento. Si no coinciden, el
   contrato no suma en los totales y queda en la lista de revisión manual hasta que se verifique contra el PDF.
6. La categoría de gasto se asigna con reglas de palabras clave sobre el objeto y las obligaciones; cada contrato muestra
   las palabras que la decidieron.

## Limitaciones

- La fecha de inicio casi nunca está en el contrato publicado: la mayoría inicia con un acta de inicio que no se publica.
- La fecha de fin se registra solo cuando el plazo fija una fecha; si el plazo es una duración, se muestra el texto del plazo.
- El OCR puede cometer errores en documentos de baja calidad. Ante cualquier duda, el botón "Ver PDF" lleva al documento
  original publicado por Acuavalle, que es la fuente oficial.
