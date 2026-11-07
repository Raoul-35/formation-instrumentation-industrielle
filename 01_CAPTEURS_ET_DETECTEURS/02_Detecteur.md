# LEÇON 02 : LE DÉTECTEUR INDUSTRIEL

## 1. Objectifs pédagogiques

À la fin de cette leçon, nous devons être capables de :

- Définir un détecteur industriel.
- Identifier les principaux éléments constitutifs d'un détecteur.
- Expliquer son principe de fonctionnement.
- Reconnaître les principales familles de détecteurs.
- Comprendre le fonctionnement des détecteurs TOR.
- Identifier les différences entre les sorties PNP et NPN.
- Reconnaître les applications industrielles des détecteurs.

## 2. Définition du détecteur industriel

Un détecteur industriel est un dispositif destiné à détecter la présence, l'absence, le passage ou l'atteinte d'une condition particulière par un objet ou un phénomène, puis à fournir une information exploitable par un système de commande.

Contrairement à un instrument de mesure qui cherche généralement à déterminer une valeur, le détecteur fournit souvent une information de type Tout Ou Rien (TOR).

Il possède généralement deux états :

- 0 : condition non détectée.
- 1 : condition détectée.

**Exemple industriel :**

Sur un convoyeur transportant des pièces métalliques, un détecteur inductif permet de détecter le passage des pièces.

- Aucune pièce détectée : sortie = 0.
- Pièce détectée : sortie = 1.

L'automate programmable industriel (API ou PLC) reçoit cette information et peut déclencher une action.

## 3. Constitution d'un détecteur inductif

Un détecteur de proximité inductif comporte généralement plusieurs éléments.

### 3.1. Face sensible

C'est la partie située à l'avant du détecteur. Elle est orientée vers l'objet à détecter.

### 3.2. Oscillateur électronique

Il génère un champ électromagnétique alternatif au niveau de la face sensible.

### 3.3. Circuit de traitement

Il analyse les modifications du champ électromagnétique et détermine si un objet métallique est présent.

### 3.4. Étage de sortie

Il transmet l'information au système de commande.

Il peut notamment comporter une sortie de type PNP ou NPN.

**Remarque :** cette constitution correspond à une représentation fonctionnelle simplifiée. Elle peut varier selon le fabricant et le modèle.

## 4. Principe de fonctionnement des détecteurs

Il existe plusieurs principes physiques utilisés dans les détecteurs industriels.

### 4.1. Détecteur inductif

**Principe :**

Il utilise un champ électromagnétique pour détecter principalement les objets métalliques.

Lorsqu'une pièce métallique entre dans la zone de détection, elle provoque des courants induits qui perturbent l'oscillateur. Le circuit électronique détecte cette perturbation et commande la sortie.

**Applications :**
- Détection de pièces métalliques sur convoyeur.
- Détection de position d'un vérin.
- Détection de présence d'un arbre métallique.

### 4.2. Détecteur capacitif

**Principe :**

Il détecte les variations de capacité électrique provoquées par la présence d'un objet dans son champ de détection.

Il peut détecter :
- Les matières plastiques.
- Les liquides.
- Les poudres.
- Les matériaux métalliques.

**Applications :**
- Détection de niveau dans une cuve.
- Détection de présence de produits non métalliques.
- Détection de matières dans une trémie.

### 4.3. Détecteur photoélectrique

**Principe :**

Il utilise un faisceau lumineux pour détecter un objet.

Trois configurations courantes existent :

- Barrage : émetteur et récepteur séparés.
- Réflexion : utilisation d'un réflecteur.
- Diffus : la lumière réfléchie par l'objet revient vers le récepteur.

**Applications :**
- Comptage de bouteilles.
- Détection de cartons.
- Contrôle de présence sur une chaîne de production.

**Remarque :** la détection des objets transparents nécessite des modèles spécialement adaptés.

### 4.4. Détecteur ultrasonique

**Principe :**

Il émet des ultrasons et analyse l'écho réfléchi par l'objet.

Le temps de propagation permet de déterminer la distance de l'objet.

**Applications :**
- Détection d'objets.
- Contrôle de distance.
- Détection de niveau de liquides ou de solides.

**Remarque :** certains détecteurs ultrasoniques fournissent une sortie TOR, tandis que d'autres fournissent une mesure de distance sous forme analogique ou numérique.

## 5. Les détecteurs TOR (Tout Ou Rien)

TOR signifie Tout Ou Rien.

Un détecteur TOR fournit généralement deux états logiques :

| État | Signification |
|---|---|
| 0 | Objet ou condition non détecté |
| 1 | Objet ou condition détecté |

Ces informations sont utilisées par les automates pour exécuter des actions.

### 5.1. Exemple de raccordement d'un détecteur PNP

Prenons un détecteur inductif PNP alimenté en 24 V DC et raccordé à une entrée numérique d'un automate Siemens S7-1200.

| Fil | Fonction | Raccordement |
|---|---|---|
| Marron | Alimentation positive | +24 V DC |
| Bleu | Alimentation négative | 0 V DC |
| Noir | Sortie PNP | Entrée numérique API |

Lorsque le détecteur détecte une pièce métallique, sa sortie fournit généralement une tension proche de +24 V DC.

L'entrée numérique de l'automate passe alors à l'état logique 1.

### 5.2. Différence entre PNP et NPN

| Type | Comportement de la sortie activée |
|---|---|
| PNP | Fournit le potentiel positif à la charge |
| NPN | Relie la sortie au potentiel négatif (0 V) |

Le choix entre PNP et NPN dépend de la compatibilité avec le circuit d'entrée de l'automate.

**Attention :** il faut toujours vérifier le schéma de raccordement du fabricant et la compatibilité électrique du module d'entrée.

## 6. Applications industrielles

| Détecteur | Application | Information fournie |
|---|---|---|
| Inductif | Détection d'une pièce métallique | Présence/absence |
| Capacitif | Détection de matière dans une trémie | Présence/absence |
| Photoélectrique | Comptage de bouteilles | Passage détecté |
| Ultrasonique TOR | Détection d'un niveau haut | Niveau atteint/non atteint |
| Magnétique | Détection de position d'un vérin | Position atteinte/non atteinte |
| Fin de course | Détection d'ouverture d'une porte | Ouvert/fermé |

## 7. Application avec un automate Siemens S7-1200

Un détecteur magnétique est installé sur un vérin pneumatique pour signaler lorsque sa tige atteint sa position de sortie.

Supposons que le détecteur soit raccordé à l'entrée I0.1.

| État du vérin | État de I0.1 |
|---|---|
| Vérin non sorti complètement | FALSE |
| Vérin sorti complètement | TRUE |

Dans TIA Portal, cette information peut être utilisée pour autoriser l'étape suivante d'une séquence automatique.

Exemple logique :

SI Vérin_Sorti = TRUE

ALORS Autoriser le retour du vérin.

Le détecteur indique que la position est atteinte. Il ne mesure pas directement la distance parcourue par la tige.

## 8. Exercices d'application

### Exercice 1 : Identification

Sur un convoyeur, un détecteur inductif surveille le passage de pièces métalliques.

Quelle information fournit-il principalement ?

A. La température exacte de la pièce.

B. La présence ou l'absence de la pièce.

C. La masse de la pièce.

**Réponse : B.**

### Exercice 2 : Constitution

Dans un détecteur inductif, quel élément génère le champ électromagnétique ?

A. L'étage de sortie.

B. L'oscillateur électronique.

C. Le câble de raccordement.

**Réponse : B.**

### Exercice 3 : Choix d'un détecteur

Sur une chaîne de production, nous devons détecter des bouteilles en plastique transparent.

Quel détecteur serait particulièrement adapté ?

A. Détecteur inductif.

B. Détecteur photoélectrique adapté aux objets transparents.

C. Détecteur magnétique.

**Réponse : B.**

### Exercice 4 : Raccordement électrique

Un détecteur inductif PNP détecte une pièce métallique.

Quelle tension retrouve-t-on généralement sur son fil noir lorsque la sortie est activée ?

A. 0 V DC.

B. +24 V DC.

C. 230 V AC.

**Réponse : B.**

### Exercice 5 : Application pneumatique

Un détecteur magnétique est installé sur un vérin pneumatique pour signaler la sortie complète de sa tige.

Quelle information transmet-il principalement à l'automate ?

A. La pression exacte de l'air.

B. La température du vérin.

C. L'atteinte de la position de sortie.

D. La vitesse exacte de déplacement.

**Réponse : C.**

## 9. Synthèse : notions essentielles

| Notion | Définition |
|---|---|
| Détecteur | Dispositif qui identifie un état ou un événement |
| Détecteur inductif | Détecteur utilisant un champ électromagnétique pour détecter les objets métalliques |
| Détecteur capacitif | Détecteur exploitant une variation de capacité électrique |
| Détecteur photoélectrique | Détecteur utilisant un faisceau lumineux |
| Détecteur ultrasonique | Détecteur utilisant la propagation des ultrasons |
| Détecteur TOR | Détecteur fournissant généralement deux états logiques |
| PNP | Sortie qui fournit le potentiel positif lorsqu'elle est activée |
| NPN | Sortie qui relie la charge au potentiel négatif lorsqu'elle est activée |

## 10. Conclusion

Les détecteurs industriels jouent un rôle essentiel dans l'automatisation des installations.

Ils permettent d'identifier la présence d'objets, de contrôler des positions, de détecter des passages et de surveiller certaines conditions de fonctionnement.

Leurs informations sont exploitées par les automates programmables pour commander les équipements et assurer le déroulement des séquences automatiques.

La compréhension des détecteurs constitue une étape indispensable avant d'étudier la distinction entre capteur et détecteur, puis le fonctionnement des transmetteurs industriels.
