# Monitor de gandul en conserva

Página estática con el monitor de precios de gandul verde en conserva: precio en chacra (Jayanca), FOB de exportación peruana (partida 2005.99.90.00), precio en góndola en EE. UU. y Emiratos, y exportaciones según SUNAT.

## Estructura

- `index.html`: la página (sin build; abre directo o con GitHub Pages).
- `data/*.json`: los datos. Para actualizar, basta con reemplazar estos archivos.
  - `precios_gondola.json`: precio de una lata por tienda.
  - `supuestos.json`: tipo de cambio SUNAT, rendimientos, flete.
  - `fob_conserva.json`: FOB por kg de embarques peruanos.
  - `mercados.json`, `procesadoras.json`: mercados y conserveras.
  - `sunat_destinos.json`, `sunat_exportadoras.json`: cifras SUNAT vía Exportemos.pe.
  - `meta.json`: fecha de actualización de cada fuente (se muestra al pie).
- `vendor/d3.min.js`: d3 v7.9.0 (licencia ISC en `vendor/d3-LICENSE`).

## Publicar

Settings → Pages → Branch `main`, carpeta `/ (root)`.

## Probar en local

```bash
python3 -m http.server 8000
# abrir http://localhost:8000
```
