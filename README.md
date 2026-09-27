# Translon container images

Build recipes for the custom containers used by the `translon-analysis`
pipeline.

## Images

| Directory | Intended image |
|---|---|
| `iribo` | `ghcr.io/jackcurragh/translon-iribo` |
| `orfquant` | `ghcr.io/jackcurragh/translon-orfquant` |
| `orfrater` | `ghcr.io/jackcurragh/translon-orfrater` |
| `translon-python` | `ghcr.io/jackcurragh/translon-python` |
| `riborf` | `ghcr.io/jackcurragh/translon-riborf` |
| `ribotie` | `ghcr.io/jackcurragh/translon-ribotie` and `translon-ribotie-cuda` |
| `gedi-price` | GEDI/PRICE support image |

The Dockerfiles pin upstream source commits where applicable. The ORF-RATER
source under `orfrater/source` is part of this repository because the pipeline
uses its compatibility-patched Python implementation.

Build from an image directory, for example:

```bash
docker build -t ghcr.io/jackcurragh/translon-iribo:1.0.0 iribo
```

Published tags should be immutable release tags, and the pipeline should use
the resulting digest after a release has been validated.
