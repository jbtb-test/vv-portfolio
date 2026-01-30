# APP4 — VVDR (Verification & Validation Decision Register) — Final Summary

## Objectif
Outiller la **traçabilité des décisions V&V humaines** via :
- un registre décisionnel versionné
- un pipeline déterministe
- des exports auditables
- aucune automatisation, aucune IA

## Points V&V mis en évidence
- Décisions strictement humaines (non automatisées)
- Source unique et versionnée (YAML)
- Déterminisme total (validation + tri)
- Couverture explicite des risques (R1 à R6)
- Indépendance complète des outils techniques

## Démo recruteur (sans exécution)
Chemin : `vv-app4-vvdr/docs/demo/`
- Registre décisions (Markdown)
- Exports CSV / JSON
- Lisible localement, sans exécuter de code

## Démo technique (optionnelle)
- Génération des exports depuis `demo_decisions.yaml`
- Aucun prérequis IA
- Tests unitaires + smoke E2E (`pytest -q`)

## Résultat
APP4 complète le portfolio par une **preuve de gouvernance V&V**.
Il explicite le WHY des choix réalisés et sécurise leur justification
en audit, revue ou entretien.
