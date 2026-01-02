# Shopify Abandoned Checkouts → WhatsApp (Rapiwa) + Google Sheets (n8n)

Automatización en n8n para detectar checkouts abandonados en Shopify, validar número en WhatsApp vía Rapiwa, enviar recordatorio y registrar el resultado en Google Sheets.

## Qué hace
- Consulta checkouts abiertos/abandonados en Shopify (ventana configurable)
- Normaliza teléfono (formato E.164 sin +)
- Verifica si el número tiene WhatsApp (Rapiwa)
- Envía recordatorio por WhatsApp (Rapiwa)
- Guarda log en Google Sheets (tabs: `sent` y `skipped`)

## Requisitos
- n8n (self-hosted o cloud)
- Shopify Admin API token
- Rapiwa Bearer token
- Google Sheets con 2 pestañas: `sent` y `skipped`

## Configuración rápida
1) Importá `workflow.json` en n8n
2) En n8n, configurá las credenciales:
   - Shopify (header `X-Shopify-Access-Token`)
   - Rapiwa (Bearer token)
   - Google Sheets (OAuth/Service Account)
3) En los nodos de Google Sheets reemplazá `REPLACE_WITH_SHEET_ID` por tu Spreadsheet ID
4) Ajustá ventana de “abandono” (minutos/horas) según tu negocio
5) Probá con un checkout real en modo test

## Columnas recomendadas (Sheets)
`timestamp | status | verification | checkout_id | name | number | total_price | currency | items_summary | checkout_url | product_links`

## Compliance
Usar solo con consentimiento/opt-in del cliente y cumpliendo políticas de WhatsApp y normativa local anti-spam.

## Soporte
Si querés que lo adaptemos a tu tienda (timing, copy, segmentación), abrí un Issue o contactanos.
