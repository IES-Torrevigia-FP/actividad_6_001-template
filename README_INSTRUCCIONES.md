
# Paquete de Evaluación Automática (Avanzada + IA) – FIX

Incluye correcciones:
- `text_stats` robusto (evita errores de comillas/saltos de línea).
- Fallback seguro de inputs en YAML para `--min-commits` y `--required`.
- Guard en job de IA para ejecutar solo si hay secrets.

## Uso
1. Copia `.github/workflows/evaluacion.yml` y `tools/*` a tu repo/plantilla.
2. Configura secrets (Azure OpenAI u OpenAI API) si quieres el job de IA.
3. Lanza el workflow (o espera a `push`). Descarga artifacts.
