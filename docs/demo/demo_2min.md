# Démo portfolio V&V — 2 minutes (sans exécution)

Objectif : démontrer la valeur V&V **en < 2 minutes**, sans lancer de code, en s'appuyant uniquement sur
les docs et les outputs figés.

Pré-requis : ouvrir les fichiers localement (ou via GitHub) et suivre le script.

---

## 0:00 — 0:15  Contexte (1 phrase)
> « Dans les systèmes critiques, la difficulté c'est d'obtenir des **preuves V&V fiables** :
> qualité d'exigences, traçabilité, couverture, conception de tests. Ce portfolio outille ce flux de bout en bout. »

---

## 0:15 — 0:30  Vue globale (portfolio)
Ouvrir : `README.md`

Points à dire :
- 4 apps indépendantes mais chaînées : **APP1 / APP2 / APP3** + **APP4**
- Outputs figés : **lisibles sans exécution**
- IA : **assistive, suggestion-only, non décisionnelle**

---

## 0:30 — 0:45  Architecture & gouvernance (slide)
Ouvrir : `docs/architecture.md` (si besoin, 1 scroll max)  
Ouvrir : `docs/vmodel_ai_overview.png`

Points à dire :
- « Le **V-cycle reste maître** »
- « L'IA est un **accélérateur**, jamais un décideur »
- « Deterministic-first + fallback safe »

---

## 0:45 — 0:55  APP4 (VVDR) : Decision trail / WHY (gouvernance)
Ouvrir : `docs/APP4-VVDR_overview.md`

Message :
- « APP4 trace les **décisions humaines V&V** : standards, gouvernance IA, arbitrages. »
- « Source of truth versionnée (YAML) exports **MD / CSV / JSON** »
- « Aucune IA : registre strictement humain, audit-ready »

Montrer (repo APP4) :
- `vv-app4-vvdr/docs/demo/` (outputs figés)

---

## 0:55 — 1:20  APP1 (QRA) : Qualité des exigences
Ouvrir : `docs/APP1-QRA_overview.md`

Message :
- « APP1 sécurise la **qualité des exigences** via règles déterministes »
- « L'IA peut suggérer, mais ne modifie rien automatiquement »

Montrer un output figé (repo APP1) :
- `vv-app1-qra/docs/demo/.../outputs_no_ai/...html`
- (optionnel) version IA : `.../outputs_ai/...html`

---

## 1:20 — 1:45  APP2 (TCTC) : Traçabilité + KPI couverture
Ouvrir : `docs/APP2-TCTC_overview.md`

Message :
- « APP2 construit la traçabilité exigences ? tests »
- « Calcule des KPI auditables : couverture, non-couverts, tests orphelins »
- « L'IA optionnelle = suggestions de liens manquants uniquement »

Montrer un output figé (repo APP2) :
- `vv-app2-tctc/docs/demo/.../outputs_no_ai/...html`
- (optionnel) version IA : `.../outputs_ai/...html`

---

## 1:45 — 2:00  APP3 (AITA) : Pack de tests (baseline + IA gouvernée)
Ouvrir : `docs/APP3-AITA_overview.md`

Message :
- « APP3 matérialise la conception de tests en packs exploitables »
- « Baseline déterministe toujours produite »
- « IA optionnelle pour enrichir, sous gouvernance »

Montrer un output figé (repo APP3) :
- `vv-app3-aita/docs/demo/.../outputs_no_ai/test_pack.md` (ou .json)
- (optionnel) version IA : `.../outputs_ai/...`

---

## 2:00  Conclusion (phrase de clôture)
> « Résultat : un flux V&V complet, outillé, auditable et reproductible,
> adapté aux contextes critiques, avec une IA strictement gouvernée
> et un **decision trail** explicite (APP4). »
