---
name: zelto-launch-experiment
description: Launch a new experiment after reviewing it.
api: openapi/zelto-openapi.json
operations:
- preflightExperiment
- createExperiment
- getExperiment
generated: '2026-10-15'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zelto-openapi.json ; every operationId checked against the contract
---

# zelto-launch-experiment

Launch a new experiment after reviewing it.

## Steps

1. 1. Run `preflightExperiment` with the request body describing the experiment to review it before launch.
2. 2. Run `createExperiment` with the request body containing the experiment definition to launch it.
3. 3. Run `getExperiment` with the path parameter `id` returned from the creation step to retrieve the created experiment details.

## Rules

- Include an `Authorization: Bearer <token>` header for all requests (bearerAuth).
