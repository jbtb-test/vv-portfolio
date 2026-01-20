# V&V AI Portfolio — Requirements ? Traceability ? Test Design

Ce dépôt est le **point d’entrée recruteur** d’un portfolio V&V complet,
aligné **V-Model / ISTQB**, avec **IA gouvernée (suggestion-only)**.

Objectif : comprendre la valeur **en moins de 2 minutes**,  
**sans exécuter de code**.

---

## Vue d’ensemble

Ce portfolio couvre l’ensemble du flux V&V :

Exigences ? Qualité ? Traçabilité ? Couverture ? Conception de tests

Il s’appuie sur **3 applications Python indépendantes**, toutes :
- testées (`pytest -vv`)
- documentées
- livrées avec **démos figées lisibles localement**
- IA **désactivée par défaut**, jamais décisionnelle

---

## Les 3 applications

### APP1 — QRA (Quality Risk Assessment)
**Objectif** : outiller la revue qualité d’exigences (DOORS / Polarion).

- règles déterministes (ambiguïté, testabilité, critères d’acceptation)
- IA optionnelle : suggestions uniquement
- outputs démontrables : **HTML + CSV**

Repo : https://github.com/jbtb-test/vv-app1-qra  
Démo figée (sans exécution) :  
`vv-app1-qra/docs/demo/`  
- `assets/outputs_no_ai/rapport.html`
- `assets/outputs_ai/rapport.html`

---

### APP2 — TCTC (Traceability & Test Coverage)
**Objectif** : traçabilité Exigences ? Cas de test + KPI de couverture.

- matrice déterministe Req ? Tests
- KPI auditables (couverture, exigences non couvertes, tests orphelins)
- IA optionnelle : suggestions de liens uniquement

Repo : https://github.com/jbtb-test/vv-app2-tctc  
Démo figée (sans exécution) :  
`vv-app2-tctc/docs/demo/`  
- `assets/outputs_no_ai/tctc_report.html`
- `assets/outputs_ai/tctc_report.html`

---

### APP3 — AITA (AI-assisted Test Ideas & Traceability Accelerator)
**Objectif** : accélérer la génération de packs de tests, sous gouvernance.

- génération déterministe sans IA
- IA optionnelle : enrichissement non bloquant
- outputs auditables : **Markdown + JSON**

Repo : https://github.com/jbtb-test/vv-app3-aita  
Démo figée (sans exécution) :  
`vv-app3-aita/docs/demo/`  
- `assets/outputs_no_ai/test_pack.md / .json`
- `assets/outputs_ai/test_pack.md / .json`

---

## Gouvernance IA (principe non négociable)

- IA **désactivée par défaut**
- IA = **moteur de suggestion uniquement**
- aucune décision automatique
- fallback strict si clé absente ou erreur IA

Les résultats déterministes restent **la référence V&V**.

---

## Pour aller plus loin (optionnel)

- Architecture globale : `docs/architecture.md`
- Vue V-cycle + IA : `docs/vmodel_ai_overview.png`
- Script démo 2 minutes : `docs/demo_2min.md`
- Notes entretien : `docs/interview_notes.md`

---

## Disclaimer

Portfolio personnel à but démonstratif.  
Les fonctionnalités IA sont **assistives** et **non décisionnelles**.
