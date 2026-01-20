# Architecture globale — Portfolio V&V avec IA gouvernée

Ce document présente l’architecture fonctionnelle du portfolio V&V,
indépendamment de toute implémentation technique.

Il vise à démontrer :
- une **vision bout-en-bout V-Model**
- une **chaîne de valeur V&V cohérente**
- une **gouvernance IA maîtrisée**, compatible contextes critiques

---

## 1. Problématique industrielle

Dans les systèmes complexes et réglementés, les difficultés récurrentes sont :

- Qualité hétérogène des exigences
- Traçabilité incomplète ou non maintenue
- KPIs de couverture peu fiables ou coûteux à produire
- Génération de tests dépendante de l’expertise individuelle
- Méfiance légitime vis-à-vis de l’IA non maîtrisée

👉 Le portfolio répond à ces enjeux **sans automatiser la décision**.

---

## 2. Vue d’ensemble — Chaîne de valeur V&V

Le portfolio est structuré en **3 applications indépendantes mais chaînées** :

Exigences
	↓
[ APP1 — Qualité ]
	↓
[ APP2 — Traçabilité & Couverture ]
	↓
[ APP3 — Conception de tests ]


Chaque application :
- peut être utilisée seule
- produit des **artefacts auditables**
- s’intègre naturellement dans un cycle en V

---

## 3. Positionnement dans le V-Model

### Côté gauche — Spécification & préparation V&V
- **APP1 (QRA)**  
  → sécurise la qualité des exigences  
  → réduit les défauts injectés en aval

- **APP2 (TCTC)**  
  → prépare la vérification via la traçabilité  
  → rend la couverture mesurable

### Côté droit — Vérification & validation
- **APP2 (TCTC)**  
  → fournit les preuves de couverture (KPIs, matrices)

- **APP3 (AITA)**  
  → accélère la conception des tests  
  → tout en conservant une validation humaine

👉 Les artefacts produits sont exploitables en audit, revue ou entretien.

---

## 4. Rôle et périmètre de chaque application

### APP1 — QRA (Quality Risk Assessment)
**Rôle**
- Détecter précocement les défauts de qualité d’exigences

**Entrées**
- Exigences (CSV type DOORS / Polarion)

**Traitements**
- Règles déterministes (ambiguïté, testabilité, complétude…)
- IA optionnelle : suggestions de reformulation uniquement

**Sorties**
- Rapport HTML lisible
- Export CSV auditable

---

### APP2 — TCTC (Traceability & Test Coverage)
**Rôle**
- Construire et exploiter la traçabilité exigences ↔ tests

**Entrées**
- Exigences
- Cas de test existants

**Traitements**
- Matrice de traçabilité déterministe
- Calcul de KPIs (couverture, exigences non couvertes, tests orphelins)
- IA optionnelle : suggestions de liens manquants

**Sorties**
- Rapports HTML / CSV
- Indicateurs directement exploitables en revue V&V

---

### APP3 — AITA (AI-assisted Test Ideas & Traceability Accelerator)
**Rôle**
- Accélérer la génération de packs de tests

**Entrées**
- Exigences qualifiées
- Contexte projet / règles de test

**Traitements**
- Génération déterministe de tests (baseline)
- IA optionnelle : enrichissement d’idées de tests

**Sorties**
- Pack de tests structuré (Markdown / JSON)
- Séparation claire déterministe / IA

---

## 5. Gouvernance IA — Principe fondamental

L’IA est **strictement encadrée** dans l’ensemble du portfolio.

### Principes non négociables
- **IA désactivée par défaut**
- **Suggestion-only**
- **Jamais décisionnelle**
- **Jamais bloquante**
- **Fallback systématique**

### Concrètement
- Les résultats déterministes restent la référence
- Les suggestions IA sont :
  - traçables
  - séparées
  - validées manuellement

👉 Le portfolio reste compatible avec des contextes :
- safety
- réglementés
- auditables

---

## 6. Artefacts & auditabilité

Tous les outputs sont :
- lisibles sans exécution
- versionnés
- exploitables en revue

Types d’artefacts :
- HTML (lecture rapide)
- CSV (audit / KPI)
- Markdown / JSON (packs de tests)

👉 Aucun “black box”.

---

## 7. Indépendance technique & portabilité

Choix assumés :
- Python standard
- CSV / HTML / Markdown
- Pas de dépendance plateforme

Objectif :
- reproductibilité
- compréhension rapide
- démonstration en entretien

---

## 8. Conclusion

Ce portfolio démontre qu’il est possible de :
- structurer un flux V&V complet
- intégrer de l’IA **sans perte de maîtrise**
- produire des preuves concrètes
- rester aligné **V-Model / ISTQB**

L’IA y est un **accélérateur**, jamais un décideur.
