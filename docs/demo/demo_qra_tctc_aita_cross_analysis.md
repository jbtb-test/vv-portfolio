# Démo croisée QRA → TCTC → AITA

Cette démo illustre comment les constats V&V
peuvent être expliqués (QRA),
localisés (TCTC),
puis matérialisés en tests exploitables (AITA).

---

## De la qualité des exigences à des tests exploitables

### Objectif
montrer comment QRA, TCTC et AITA couvrent la chaîne V&V complète :
qualité des exigences → preuve de couverture → tests exploitables

---

## 1. Contexte (client / recruteur)
- Exigences validées process (ALM, revues, workflow).
- Traçabilité exigences ↔ tests en place.
- KPI de couverture acceptables (ex. 90%).
- Pourtant : incertitude sur la **prouvabilité** réelle.

👉 Question clé V&V : *peut-on prouver l’intention des exigences avec les tests existants ?*

---

## 2. Étape 1 — QRA : audit de la prouvabilité des exigences

**QRA analyse les exigences indépendamment des outils ALM.**  
Il détecte des risques V&V structurels, même sur des exigences “validées”.

### Exemples détectés par QRA
- **REQ-005** — *“high accuracy”*  
  → Ambiguïté non mesurable, pas de seuil ni conditions d’opération.
- **REQ-019** — *“The system shall be safe”*  
  → Objectif safety haut niveau, non testable tel quel.

**Résultat QRA**
- Exigences marquées *À risque*.
- Explication factuelle (rules déterministes).
- Suggestions de clarification (IA suggestion-only).

👉 QRA répond à la question :  
**“Cette exigence est-elle prouvable sans interprétation humaine ?”**

---

## 3. Étape 2 — TCTC : audit de la traçabilité exigences ↔ tests

**TCTC analyse la structure de couverture**, pas la qualité sémantique des tests.

### Résultats sur le même dataset
- 20 exigences / 35 tests
- **Coverage KPI : 90%**
- **2 exigences non couvertes** : REQ-005, REQ-019
- **2 tests orphelins** : TC-034, TC-035

👉 Malgré un KPI “vert”, il existe des **trous structurels**.

### Rôle de l’IA dans TCTC
- Propose des **candidats de lien** (suggestion-only).
- N’applique aucun lien automatiquement.
- Aide à la **revue humaine**, sans tricher sur les KPI.

---

## 4. Lecture croisée QRA → TCTC (le point clé)

| Observation QRA | Observation TCTC | Interprétation V&V |
|-----------------|------------------|--------------------|
| Exigence ambiguë / non prouvable | Exigence non couverte | Logique : pas de test pertinent possible |
| Safety goal haut niveau | Exigence non couverte | Doit être décomposée (safety requirements + safety case) |
| Suggestion IA de clarification | Suggestion IA de lien | Support à la décision, pas automatisation |

👉 **Des exigences faibles produisent mécaniquement une couverture fragile**,  
même avec des outils et KPI en place.

---

## 5. Étape 3 — AITA : de l’analyse à des tests exploitables

QRA et TCTC révèlent un problème V&V.
**AITA matérialise les constats V&V en tests concrets et auditables.**, sans automatiser la décision.

### Rôle d’AITA
- Prendre en entrée :
  - des exigences (idéalement clarifiées via QRA),
  - une vision claire des zones non couvertes (via TCTC).
- Générer un **pack de tests structuré**, cohérent et exploitable.

### Ce que produit AITA
- Idées de tests issues d’une **baseline déterministe** (checklist ISTQB)
- Pack de tests structuré (MD / JSON) :
  - test_id
  - requirement_id
  - steps
  - expected results
- Sorties **auditables**, lisibles sans exécuter de code

### Rôle de l’IA dans AITA
- L’IA peut suggérer des **idées complémentaires** (edge cases, scénarios oubliés)
- Elle :
  - ne supprime rien
  - ne valide rien
  - ne décide rien
- Si l’IA est absente ou désactivée :
  - le pack est **quand même produit** (baseline déterministe)

👉 AITA répond à la question :
**“À partir de ces constats V&V, quels tests concrets puis-je réellement exécuter ?”**

---

## 6. Lecture croisée QRA → TCTC → AITA (tableau)

| Observation QRA | Observation TCTC | Apport AITA | Interprétation V&V |
|-----------------|------------------|-------------|--------------------|
| Exigence ambiguë | Exigence non couverte | Peu de tests générés | Signal amont : exigence à clarifier |
| Exigence clarifiée | Liens manquants | Génération de tests structurés | Couverture testable améliorée |
| Suggestion IA QRA | Suggestion IA TCTC | Suggestion IA AITA | Support à la décision humaine |

---

## 7. Message clé V&V

> “QRA explique *pourquoi* certaines exigences sont difficiles à prouver.  
> TCTC montre *où* la couverture est structurellement absente.  
> AITA transforme ces constats en **tests exploitables**, sans jamais automatiser la décision.”

👉 Ensemble, les trois outils couvrent :
- la qualité amont,
- la preuve de couverture,
- la matérialisation des tests.

