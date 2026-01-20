# APP3 — AITA (AI-assisted Test Ideas & Traceability Accelerator) — Final Summary

## Objectif
Outiller la **génération de packs de tests** à partir d’exigences (exports DOORS / Polarion) via :
- règles déterministes (checklists de conception de tests)
- IA optionnelle (suggestion-only, non bloquante)
- outputs démontrables et auditables (Markdown + JSON)

## Points V&V mis en évidence
- Déterminisme prioritaire : génération complète sans IA par défaut
- IA gouvernée : ENABLE_AI=0 par défaut, clé absente ⇒ fallback strict
- Traçabilité : chaque test est lié à une exigence source
- Auditabilité : packs lisibles (MD) + données outillage (JSON)
- Robustesse : tests unitaires (pytest -vv), CI documentée

## Démo recruteur (sans exécution)
Chemin : `vv-app3-aita/docs/demo/`
- Sans IA : `docs/demo/assets/outputs_no_ai/test_pack.md` / `test_pack.json`
- Avec IA : `docs/demo/assets/outputs_ai/test_pack.md` / `test_pack.json` (+ `ai_suggestions.md`)

## Démo technique (optionnelle)
- Run : `python -m vv_app3_aita.main --out-dir data/outputs --verbose`
- Outil diagnostic : `python tools/env_check.py --print --redact-paths`

## Résultat
APP3 est livrable et prêt entretien : génération de packs de tests, IA cadrée, démo figée, tests verts et repo propre.
