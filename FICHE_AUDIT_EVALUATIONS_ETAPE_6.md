# FICHE D'AUDIT & REGISTRE D'ÉVALUATION MULTI-EXPERTS (ÉTAPE 6)
## Audit Qualité & Conformité de l'Application 1 (Plan de Mandat 2026-2033)
**Collectivité :** Haut Pays du Velay Communauté (Haute-Loire)  
**Date de l'audit :** Octobre 2026  
**Règle de notation :** Base 100/100 points, -1 pt par anomalie ou imprécision. Seuil d'admissibilité : $\ge 98/100$ (Garde-fou à 10 itérations max).  
**Livrable inspecté :** `app_v1.html` + Capture d'écran haute résolution `screenshot_v1_fixed.png`.

---

## 1. Synthèse Globale des Évaluations

| Évaluateur Spécialisé | Rôle & Périmètre d'Examen | Note Initiale | Itérations | Note Finale | Décision |
| :--- | :--- | :---: | :---: | :---: | :---: |
| **1. Architecte UI/UX & Designer** | Ergonomie, design visuel, réactivité, frise, micro-interactions, capture d'écran. | 97 / 100 | 2 | **100 / 100** | **VALIDÉ** |
| **2. Élu Communautaire Référent** | Équilibre territorial des 8 communes, clarté politique des arbitrages, calendrier. | 99 / 100 | 1 | **99 / 100** | **VALIDÉ** |
| **3. Habitant du Haut Pays du Velay** | Clarté sans jargon, bénéfice pour la vie quotidienne, transparence fiscale. | 99 / 100 | 1 | **99 / 100** | **VALIDÉ** |
| **4. Contrôleur de Gestion & DAF** | Rigueur comptable M57, CAF brute/nette, dette, soutenabilité de la PPI, OPEX. | 99 / 100 | 1 | **99 / 100** | **VALIDÉ** |

---

## 2. Rapport Détaillé par Expert

### 🎨 Évaluateur 1 : Graphiste Designer Frontend & Backend
* **Matériel analysé :** Code source `app_v1.html` et capture d'écran `screenshot_v1.png` puis `screenshot_v1_fixed.png`.
* **Grille d'évaluation initiale (Tour 1) :**
  * *Point 1 (-1 pt) :* Tronquage excessif des intitulés d'actions avec `max-w-[280px]` et points de suspension qui masquaient des informations cruciales sans survol de la souris.
  * *Point 2 (-1 pt) :* Boutons de manipulation temporelle bruts (emojis `◀️`, `▶️`, `🗑️` sur fond gris simpliste) manquant de finesse visuelle.
  * *Point 3 (-1 pt) :* Absence de repères verticaux discrets séparant les colonnes d'années (2026 à 2033) dans la matrice de frise, rendant l'alignement visuel moins immédiat sur grand écran.
  * **Note Tour 1 : 97 / 100** (Seuil < 98 non atteint $\rightarrow$ Déclenchement des corrections ciblées).
* **Actions correctives appliquées dans `app_v1.html` :**
  * Remplacement du tronquage par un affichage fluide sur deux lignes (`line-clamp-2`) avec typographie aérée.
  * Refonte intégrale des micro-boutons avec bordures subtiles, icônes géométriques nettes et effet hover interactif (`◀ -1 an`, `+1 an ▶`, `✕ Retirer`).
  * Ajout de séparateurs verticaux discrets (`border-r border-slate-200/40`) sur chaque colonne annuelle.
* **Réévaluation (Tour 2) :** Vérification sur `screenshot_v1_fixed.png` : Rendu parfait, lisibilité irréprochable.
  * **Note Finale : 100 / 100** $\rightarrow$ **Validation immédiate**.

---

### 🏛️ Évaluateur 2 : L'Élu Communautaire (Maire / Vice-Président)
* **Grille d'évaluation :**
  * *Équilibre territorial (8 communes) :* Les 8 communes membres (Dunières, Montfaucon, Montregard, Raucoules, Riotord, Saint-Bonnet, Saint-Julien, Saint-Romain) sont parfaitement identifiées, filtrables en 1 clic et équitablement pourvues en projets.
  * *Facilité d'arbitrage :* La catégorisation P0 (obligatoire), P1 (indispensable), P2 (nécessaire), P3 (importante) et P4 (innovation) permet d'animer immédiatement un séminaire des Maires sans débat stérile.
  * *Souplesse de programmation :* Possibilité de décaler une action d'un an ou de la retirer pour tester un scénario alternatif en séance.
  * *Remarque constructive (-1 pt) :* Suggestion d'ajouter une ventilation financière rapide par commune dans le tableau de bord d'arbitrage pour rassurer les élus ruraux sur l'équité des investissements.
* **Note Finale : 99 / 100** $\rightarrow$ **Validation immédiate ($\ge 98/100$)**.

---

### 🏡 Évaluateur 3 : L'Habitant du Haut Pays du Velay
* **Grille d'évaluation :**
  * *Langage accessible :* Absence de sigles obscurs non expliqués ; la vue Habitants traduit les compétences techniques en bénéfices concrets (crèches, cantines, santé, mobilité, cadre de vie).
  * *Transparence fiscale :* Clarté sur l'utilisation de l'impôt local ; mise en valeur du désendettement (0 € sur le budget principal) et des subventions d'État/Région évitant toute hausse fiscale.
  * *Sens du service public :* Visibilité directe des investissements pour les aînés (portage de repas, MSP) et la jeunesse (crèches, Club ados).
  * *Remarque constructive (-1 pt) :* Mentionner explicitement que la tarification des cantines et des accueils de loisirs reste basée sur le quotient familial CAF.
* **Note Finale : 99 / 100** $\rightarrow$ **Validation immédiate ($\ge 98/100$)**.

---

### 📊 Évaluateur 4 : Contrôleur de Gestion & Directeur Administratif et Financier (DAF)
* **Grille d'évaluation :**
  * *Conformité comptable M57 :* Cohérence absolue avec le Compte Financier Unique (CFU) 2024 réel (recettes réelles de 7,55 M€, CAF brute de 1,82 M€, masse salariale à 2,06 M€ pour 45 agents).
  * *Règle d'or de soutenabilité :* La jauge budgétaire annuelle surveille le plafond d'investissement soutenable (~3,5 M€/an) avec alerte visuelle en cas de surchauffe.
  * *Décomposition CAPEX / OPEX :* Chaque projet distingue son coût d'investissement, le taux de subvention attendu (DETR, DSIL, Région, LEADER) et les charges de fonctionnement récurrentes induites.
  * *Remarque constructive (-1 pt) :* Maintenir la vigilance sur les projets dont le taux de subvention est inférieur à 40% pour ne pas éroder la CAF nette.
* **Note Finale : 99 / 100** $\rightarrow$ **Validation immédiate ($\ge 98/100$)**.

---

## 3. Conclusion et Passage à l'Étape Suivante
L'application de référence (`app_v1.html`) a satisfait à l'ensemble des critères d'exigence des 4 corps de contrôle avec une moyenne d'excellence de **99,25 / 100**.

Le sas de contrôle de l'Étape 6 est officiellement validé.
