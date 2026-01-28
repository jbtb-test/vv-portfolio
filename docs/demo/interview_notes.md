# Notes entretien  Portfolio V&V (APP1  APP2  APP3)

> Document interne — support d’entretien (non destiné à une lecture recruteur autonome)

---

## 1) Pitch (2030 secondes)

- « Je couvre le flux V&V complet : **qualité des exigences,  traçabilité/KPI et conception de tests**. »
- « Le coeur est **déterministe et auditable** (CSV/HTML/MD/JSON) : reproductible, compatible contextes critiques. »
- « L'IA est **gouvernée** : **suggestion-only**, jamais décisionnelle, fallback non bloquant. »

---

## 2) Valeur métier (à marteler)

### Ce que ça réduit
- Défauts injectés en aval (exigences ambiguës / non testables)
- Coût de maintien de traçabilité (ou oubli)
- KPIs de surface non auditables
- Variabilité de conception de tests selon les personnes

### Ce que ça apporte
- Revue exigences outillée (APP1)
- Traçabilité + couverture mesurable (APP2)
- Accélération test design sous contrôle (APP3)
- Preuves concrètes : exports + rapports lisibles

---

## 3) Mapping V-Model / ISTQB (réponse courte)

- APP1 = **qualité amont** (prévention, critères de testabilité)
- APP2 = **preuves de couverture** (traçabilité Req  Tests + KPI)
- APP3 = **aide à la conception** (test ideas + pack structuré)
- Les artefacts sont pensés pour : **revue**, **audit**, **discussion déquipe**

---

## 4) Gouvernance IA  réponse anti-piège

### Ce que je dis (simple)
- « L'IA na pas le droit de décider. Elle propose, l'ingénieur valide. »
- « Tout ce qui impacte une preuve V&V reste déterministe. »
- « Si l'IA tombe, l'outil fonctionne pareil (fallback). »

### Ce que je refuse (si on me pousse)
- Auto-modifier des exigences
- Auto-générer une traçabilité officielle
- Remplacer des KPI déterministes par un score IA opaque

---

## 5) Questions typiques & réponses prêtes

### Q1  Pourquoi 3 apps ? Pourquoi pas une seule ?
- « Séparation claire des responsabilités : qualité / traçabilité / test design.
  Chaque app est utilisable seule et s'intègre facilement dans un SI existant. »

### Q2  Comment tu garantis l'auditabilité ?
- « Exports CSV/JSON + rapports lisibles + logique déterministe.
  Les suggestions IA sont séparées et traçables. »

### Q3  Comment tu gères la sécurité / secrets ?
- « Secrets jamais committés. IA optionnelle, activée via env.
  Le mode par défaut est sans IA. »

### Q4  Quel est l'indicateur le plus utile ?
- « Couverture exigences (APP2), non-couverts, tests orphelins.
  Cest actionnable immédiatement en plan de test / revue. »

### Q5  Comment tu valides la qualité des règles ?
- « Tests unitaires + jeux de données démo, cohérence des outputs figés.
  Je privilégie la reproductibilité sur la magie. »

---

## 6) Variantes de positionnement selon le poste

### Poste QA / Test Lead
- « Je rends la couverture testable mesurable et pilotable (KPIs + preuves). »

### Poste V&V système / safety
- « Je sécurise l'amont (qualité exigences) et je rends les preuves auditables. »

### Poste outillage / process
- « Industrialisation : formats simples, portabilité, documentation recruteur-grade. »

---

## 7) Closing (10 secondes)
- « Mon axe : **preuve V&V** + **reproductibilité** + **IA maîtrisée**.
  Le portfolio est lisible en 2 minutes, sans exécuter de code. »

Pour illustrer concrètement la complémentarité QRA / TCTC :
- voir la démo croisée QRA ? TCTC (analyse sur dataset réaliste)