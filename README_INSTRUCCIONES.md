
# Paquete de Evaluación Automática (Avanzada + IA) – FIX v3

Mejoras respecto a v2:
- **Job Summary bien formateado**: se añade `sed 's/$/  /'` para preservar saltos de línea y tablas Markdown.
- Mantiene el **patrón gate** para IA (sin `if: secrets` a nivel de job).
- `text_stats` robusto y fallbacks para inputs.

## Uso
1) Copia `.github/workflows/evaluacion.yml` y `tools/*` a tu repo/plantilla.
2) (Opcional IA) Añade secrets en *Settings → Secrets and variables → Actions*:
   - Azure OpenAI: `AZURE_OPENAI_ENDPOINT`, `AZURE_OPENAI_API_KEY`, `AZURE_OPENAI_DEPLOYMENT`
   - OpenAI: `OPENAI_API_KEY`, `OPENAI_MODEL`
3) Commit & push o lanza **Run workflow** para ajustar `min_commits` / `required_files`.
