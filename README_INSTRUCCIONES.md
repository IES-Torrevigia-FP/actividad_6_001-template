
# Paquete de Evaluación Automática (Avanzada + IA) – FIX v2

Cambios clave respecto a FIX v1:
- El job `ia` ya **no** usa `if: ${{ secrets... }}` a nivel de job. En su lugar, incluye un paso **gate** (`Detectar credenciales IA`) que decide si ejecutar o no los pasos de IA.
- Mantiene el `text_stats` robusto para evitar errores de literales de cadena.
- Sigue usando fallback seguro para `--min-commits` y `--required`.

## Uso
1) Copia `.github/workflows/evaluacion.yml` y `tools/*` a tu repo/plantilla.
2) (Opcional IA) Añade secrets en *Settings → Secrets and variables → Actions*:
   - Azure OpenAI: `AZURE_OPENAI_ENDPOINT`, `AZURE_OPENAI_API_KEY`, `AZURE_OPENAI_DEPLOYMENT`
   - OpenAI: `OPENAI_API_KEY`, `OPENAI_MODEL`
3) Haz commit & push, o lanza el workflow manualmente (Run workflow) para ajustar `min_commits`/`required_files`.
