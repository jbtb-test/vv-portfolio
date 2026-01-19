# APP2 — TCTC (Traceability & Test Coverage Tool) — Final Summary

## Objectif
Outiller la traçabilité Exigences ↔ Cas de test (exports DOORS / Polarion) via :
- matrice déterministe Req ↔ Tests
- KPI automatiques (couverture, exigences non couvertes, tests orphelins)
- IA optionnelle (suggestion-only, non bloquante)
- outputs démontrables (HTML + CSV)

## Points V&V mis en évidence
- Traçabilité explicite et audit-ready (CSV)
- KPI déterministes (aucune dépendance IA)
- IA gouvernée : ENABLE_AI=0 par défaut, clé absente ⇒ fallback strict
- Robustesse : validation datasets, fallback HTML, outputs toujours générés
- Qualité logicielle : tests unitaires étendus (`pytest -vv`), CI maîtrisée

## Démo recruteur (sans exécution)
Chemin : `vv-app2-tctc/docs/demo/`
- Sans IA : `docs/demo/assets/outputs_no_ai/tctc_report.html`
- Avec IA : `docs/demo/assets/outputs_ai/tctc_report.html`

## Démo technique (optionnelle)
- Run : `python -m vv_app2_tctc.main --out-dir data/outputs --verbose`
- Mode IA : `ENABLE_AI=1` (suggestions uniquement)
- Diagnostic env : `python tools/env_check.py --print --redact-paths`

## Résultat
APP2 est livrable et prêt entretien : traçabilité démontrable, KPI lisibles,
IA non décisionnelle, tests verts, démo figée + exécution locale possible.
