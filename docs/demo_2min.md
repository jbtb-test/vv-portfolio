# Démo portfolio V&V  2 minutes (sans exécution)

Objectif : démontrer la valeur V&V **en < 2 minutes**, sans lancer de code, en sappuyant uniquement sur
les docs et les outputs figés.

Pré-requis : ouvrir les fichiers localement (ou via GitHub) et suivre le script.

---

##  0:00  0:15  Contexte (1 phrase)
> « Dans les systèmes critiques, la difficulté cest dobtenir des **preuves V&V fiables** :
> qualité dexigences, traçabilité, couverture, conception de tests. Ce portfolio outille ce flux de bout en bout. »

---

##  0:15  0:30  Vue globale (portfolio)
 Ouvrir : `README.md`

Points à dire :
- 3 apps indépendantes mais chaînées : **APP1  APP2  APP3**
- Outputs figés : **lisibles sans exécution**
- IA : **assistive, suggestion-only, non décisionnelle**

---

##  0:30  0:45  Architecture & gouvernance IA (slide)
 Ouvrir : `docs/architecture.md` (si besoin, 1 scroll max)
 Ouvrir : `docs/vmodel_ai_overview.png`

Points à dire :
- « Le **V-cycle reste maître** »
- « LIA est un **accélérateur**, jamais un décideur »
- « Deterministic-first + fallback safe »

---

##  0:45  1:10  APP1 (QRA) : Qualité des exigences
 Ouvrir : `docs/APP1-QRA_overview.md`

Message :
- « APP1 sécurise la **qualité des exigences** via règles déterministes »
- « LIA peut suggérer, mais ne modifie rien automatiquement »

 Montrer un output figé (repo APP1) :
- `vv-app1-qra/docs/demo/.../outputs_no_ai/...html`
- (optionnel) version IA : `.../outputs_ai/...html`

---

##  1:10  1:35  APP2 (TCTC) : Traçabilité + KPI couverture
 Ouvrir : `docs/APP2-TCTC_overview.md`

Message :
- « APP2 construit la traçabilité exigences  tests »
- « Calcule des KPI auditables : couverture, non-couverts, tests orphelins »
- « IA optionnelle = suggestions de liens manquants uniquement »

 Montrer un output figé (repo APP2) :
- `vv-app2-tctc/docs/demo/.../outputs_no_ai/...html`
- (optionnel) version IA : `.../outputs_ai/...html`

---

##  1:35  1:55  APP3 (AITA) : Pack de tests (baseline + IA gouvernée)
 Ouvrir : `docs/APP3-AITA_overview.md`

Message :
- « APP3 accélère la conception de tests »
- « Baseline déterministe toujours produite »
- « IA optionnelle pour enrichir, sous gouvernance »

 Montrer un output figé (repo APP3) :
- `vv-app3-aita/docs/demo/.../outputs_no_ai/test_pack.md` (ou .json)
- (optionnel) version IA : `.../outputs_ai/...`

---

##  1:55  2:00  Conclusion (phrase de clôture)
> « Résultat : un flux V&V complet, outillé, auditable, reproductible,
> compatible contextes critiques, avec une IA strictement gouvernée. »
