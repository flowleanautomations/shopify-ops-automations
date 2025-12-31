# Workflows (n8n) — Shopify DTC

Este repo contiene workflows **sanitizados** (sin credenciales) para mejorar operaciones en Shopify:
- Soporte: triage + derivación a humano
- Inventario: alertas preventivas por SKU
- Revenue recovery: abandonos + winback

## Cómo usar (5 min)
1) Descargá el `.json` del workflow.
2) En n8n: **Import workflow**.
3) Configurá credenciales y variables (placeholders).
4) Ejecutá en modo test y luego activá.

## Lista de workflows
- `shopify-dtc-revenue-recovery-v1.json` — Recupero de ventas (checkout + winback)
- `shopify-inventory-alerts-v1.json` — Alertas de stock por SKU (cobertura + umbrales)
- `shopify-support-triage-v1.json` — Triage automático + handoff a humano

## Seguridad (importante)
- No subimos secretos al repo (API keys, tokens, webhooks reales).
- Todo va con placeholders tipo `{{SHOPIFY_TOKEN}}`, `{{SHEET_ID}}`.

## Contacto
Si querés que lo instale y lo deje funcionando en 7 días:
- flowleanautomation.com
- LinkedIn: Ivan Bacari
