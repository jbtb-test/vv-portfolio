# Démo croisée QRA → TCTC  
## De la qualité des exigences à la qualité de la couverture

### Objectif
Montrer qu’une **couverture de tests “verte”** ne garantit pas une **preuve V&V solide**,  
et expliquer comment **QRA** et **TCTC** se complètent pour révéler le risque réel.

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

## 5. Message clé (à dire en entretien / appel client)

> “QRA explique *pourquoi* certaines exigences sont difficiles à prouver.  
> TCTC montre *où* la couverture est structurellement absente.  
> Ensemble, ils révèlent le risque V&V que les KPI seuls ne montrent pas.”

---

## 6. Positionnement clair (sans bullshit)
- ❌ Pas un remplacement de Polarion / DOORS.
- ❌ Pas une IA décisionnelle.
- ✅ Audit indépendant, rapide, explicable.
- ✅ Outils utilisables en amont des revues lourdes.
- ✅ Aligné avec une démarche V&V senior (ISTQB, cycle en V).

---

## 7. Conclusion
La qualité V&V ne se résume ni à la conformité process,  
ni à un pourcentage de couverture.

**QRA + TCTC** apportent une lecture complémentaire :
- prouvabilité des exigences
- robustesse de la couverture

👉 Objectif : **réduire le risque d’audit tardif**, pas “faire joli dans l’outil”.
