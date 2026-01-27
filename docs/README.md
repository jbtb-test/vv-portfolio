# Documentation — Portfolio V&V

Ce dossier regroupe la documentation transversale du portfolio V&V.
Il est conçu pour être **lisible sans contexte technique** et sans exécuter de code.

---

- **Démo croisée QRA → TCTC**  
  Audit de la prouvabilité des exigences et de la robustesse de la couverture tests.  
  👉 [demo_qra_tctc_cross_analysis.md](demo_qra_tctc_cross_analysis.md)

## Parcours recommandé (lecture < 2 minutes)

1. **Vue d’ensemble & gouvernance IA**
   - `vmodel_ai_overview.png`  
   → compréhension immédiate du positionnement V-cycle et de l’IA (non décisionnelle)

2. **Architecture globale**
   - `architecture.md`  
   → chaîne de valeur V&V : exigences → qualité → traçabilité → tests

3. **Script de démonstration**
   - `demo_2min.md`  
   → déroulé chronométré utilisable en entretien

4. **Notes entretien**
   - `interview_notes.md`  
   → réponses courtes, valeur métier, pièges IA

---

## Documentation par application

- **APP1 — QRA** : `APP1-QRA_overview.md`  
  Qualité des exigences, règles déterministes, suggestions IA optionnelles

- **APP2 — TCTC** : `APP2-TCTC_overview.md`  
  Traçabilité exigences -> tests, KPI de couverture auditables

- **APP3 — AITA** : `APP3-AITA_overview.md`  
  Génération de packs de tests, baseline déterministe + IA gouvernée

---

## Principes clés du portfolio

- IA **désactivée par défaut**
- IA **suggestion-only**, jamais décisionnelle
- Outputs **auditables** (HTML / CSV / MD / JSON)
- Démos **figées**, lisibles sans exécution

---

## Public cible

- Recruteurs techniques
- Leads V&V / QA
- Ingénieurs système / safety
- Responsables outillage & process
