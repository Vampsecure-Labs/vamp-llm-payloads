# vamp-llm-payloads

> **VampSecure Labs Security Research Division**

Colección de datasets adversariales para la fase 6 (Red Team) de
[vamp-llm-probe](https://github.com/Vampsecure-Labs/vamp-llm-probe).

## Contenido

| Fichero | Descripción | Entradas |
|---------|-------------|----------|
| `jailbreak_prompts.csv` | Prompts de jailbreak en inglés | ~7 600 |
| `jailbreak_prompts_es.csv` | Prompts de jailbreak en español | ~30 |
| `injection_prompts.csv` | Vectores de inyección directa (EN) | ~220 |
| `injection_prompts_es.csv` | Vectores de inyección en español | ~50 |
| `forbidden_questions.csv` | Preguntas en categorías restringidas | ~390 |
| `ascii_smuggling_payloads.json` | Payloads de referencia Unicode Tag | 18 |

## Uso con vamp-llm-probe

Los datasets se descargan automáticamente al primer escaneo con `--dataset`:

```bash
vamp-llm-probe --endpoint http://localhost:11434 --dataset
```

Para descargar/actualizar manualmente sin lanzar el probe:

```bash
vamp-llm-probe --update-payloads
```

Los ficheros se almacenan en `~/.cache/vamp-llm-probe/payloads/`.

## Aviso legal

Estos datasets se distribuyen **exclusivamente para uso en seguridad ofensiva autorizada**,
investigación y desarrollo de defensas contra ataques de inyección de prompts en sistemas LLM.
Cualquier uso fuera de estos contextos es responsabilidad del usuario.

© VampSecure Studios — VampSecure Labs Security Research Division
