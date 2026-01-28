# APP1 — QRA (Quality Risk Assessment) — Final Summary

## Objectif
Outiller la revue qualité d’exigences (export DOORS / Polarion) via :
- règles déterministes (détection défauts : ambiguïté, testabilité, critères d’acceptation)
- IA optionnelle (suggestion-only, non bloquante)
- outputs démontrables (HTML + CSV)

## Points V&V mis en évidence
- Déterminisme prioritaire : score/statut basés sur règles explicites
- IA gouvernée : ENABLE_AI=0 par défaut, clé absente ⇒ fallback strict
- Traçabilité : issues typées, output CSV audit-ready
- Robustesse : tests unitaires (pytest -vv), CI GitHub Actions
- Réduit les défauts injectés dans la traçabilité et les tests

## Démo recruteur (sans exécution)
Chemin : `vv-app1-qra/docs/demo/`
- Sans IA : `docs/demo/assets/outputs_no_ai/rapport.html` (+ screenshot)
- Avec IA : `docs/demo/assets/outputs_ai/rapport.html` (+ screenshot)

## Démo technique (optionnelle)
- Run : `python -m vv_app1_qra.main --verbose`
- Outil diagnostic : `python tools/env_check.py --print --redact-paths`
- Diagnostic env : `python tools/env_check.py --print --redact-paths`

## Résultat
APP1 est livrable et prêt entretien : pack démo figé + CI + tests verts.
