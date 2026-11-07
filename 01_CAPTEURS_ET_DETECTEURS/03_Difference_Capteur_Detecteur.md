# LEÇON 03 — DIFFÉRENCE ENTRE CAPTEUR ET DÉTECTEUR

## 1. Objectifs de la leçon

À la fin de cette leçon, nous devons être capables de :

- Expliquer la différence entre un capteur et un détecteur.
- Comprendre pourquoi un détecteur est également un capteur au sens physique.
- Identifier les informations fournies par chacun.
- Reconnaître leurs applications dans l'industrie.
- Distinguer les signaux analogiques et numériques utilisés pour leur raccordement à un automate programmable industriel (API).

## 2. Rappel : qu'est-ce qu'un capteur ?

Un capteur est un dispositif qui réagit à une grandeur physique et permet d'obtenir une information exploitable sur cette grandeur.

Exemples :
- Une PT100 réagit à la température par une variation de résistance.
- Un capteur de pression réagit à la pression exercée sur son élément sensible.
- Un capteur de niveau permet de connaître la hauteur ou le niveau d'un liquide.

Un capteur peut donc permettre de connaître une valeur mesurée.

Exemple : une température de 75 °C.

## 3. Rappel : qu'est-ce qu'un détecteur ?

Un détecteur est un dispositif dont la fonction principale est de reconnaître la présence, l'absence ou l'apparition d'un état particulier.

Il fournit généralement une information de type tout ou rien (TOR).

Exemples :
- Un détecteur inductif indique la présence d'une pièce métallique.
- Un détecteur photoélectrique indique le passage d'un objet.
- Un détecteur de niveau haut signale que le liquide a atteint un seuil déterminé.

Le détecteur ne donne généralement pas une mesure continue de la grandeur surveillée. Il indique principalement si une condition est satisfaite ou non.

## 4. Quelle est la différence fondamentale ?

La différence repose principalement sur la fonction recherchée.

| Critère | Capteur de mesure | Détecteur |
|---|---|---|
| Fonction principale | Mesurer une grandeur physique | Détecter un état ou un événement |
| Information fournie | Une valeur mesurée | Une présence, une absence ou un état |
| Type de signal fréquent | Analogique ou numérique | Généralement TOR |
| Exemple | PT100 | Détecteur inductif |
| Information obtenue | Température de 75 °C | Pièce métallique présente |
| Application | Surveillance et régulation | Automatisation et commande |

**Attention :** cette distinction est fonctionnelle et non absolue. Un détecteur est également un capteur au sens physique, puisqu'il réagit à un phénomène physique pour produire une information.

La différence réside donc dans l'utilisation de l'information.

## 5. Pourquoi un détecteur est-il aussi un capteur ?

Prenons l'exemple d'un détecteur inductif.

Lorsqu'une pièce métallique s'approche de sa face sensible :
1. Le champ électromagnétique du détecteur est perturbé.
2. Le circuit électronique détecte cette perturbation.
3. Le détecteur change l'état de sa sortie.
4. L'automate reçoit une information indiquant la présence de la pièce.

Le détecteur réagit donc bien à un phénomène physique.

Il peut ainsi être considéré comme un capteur au sens général, mais on l'appelle détecteur parce que sa fonction principale est de signaler une présence ou une absence.

## 6. Exemples dans l'industrie

### 6.1 Mesure de température

Dans un moteur électrique, une PT100 peut être utilisée pour mesurer la température des enroulements.

Exemple :
- Température mesurée : 75 °C.
- L'information peut être exploitée pour surveiller l'échauffement du moteur.

Il s'agit d'une application de mesure.

### 6.2 Détection de présence

Sur une chaîne de production, un détecteur inductif peut vérifier la présence d'une pièce métallique.

Exemple :
- Pièce présente : sortie activée.
- Pièce absente : sortie désactivée.

Il s'agit d'une application de détection.

### 6.3 Mesure et détection de niveau dans une cuve

Considérons une cuve contenant de l'eau.

Nous installons deux appareils :

**Appareil 1 : transmetteur de niveau**

Il fournit une information continue sur le niveau du liquide.

Exemple :
- 0 % : cuve vide.
- 50 % : cuve à moitié remplie.
- 100 % : cuve pleine.

**Appareil 2 : détecteur de niveau haut**

Il signale lorsque le liquide atteint un seuil prédéfini, par exemple 80 %.

Exemple :
- Niveau inférieur à 80 % : détecteur non activé.
- Niveau égal ou supérieur à 80 % : détecteur activé.

Les deux appareils ont des fonctions complémentaires.

Le transmetteur permet de connaître le niveau, tandis que le détecteur permet de signaler le franchissement d'un seuil.

## 7. Différence entre signal analogique et signal TOR

### 7.1 Signal analogique

Un signal analogique peut représenter plusieurs valeurs dans une plage définie.

Exemple : un transmetteur de niveau utilisant une sortie 4–20 mA.

Pour une plage de mesure de 0 à 100 % :

| Niveau de la cuve | Signal de sortie |
|---|---|
| 0 % | 4 mA |
| 25 % | 8 mA |
| 50 % | 12 mA |
| 75 % | 16 mA |
| 100 % | 20 mA |

Ce signal est généralement raccordé à une entrée analogique (AI) de l'automate.

### 7.2 Signal TOR

Un signal TOR possède deux états :

- 0 : état inactif.
- 1 : état actif.

Exemple : un détecteur de niveau haut.

Lorsque le liquide atteint le seuil défini, le détecteur change d'état.

Ce signal est généralement raccordé à une entrée numérique (DI) de l'automate.

## 8. Application avec un automate Siemens S7-1200

Considérons une installation comprenant :

- Un transmetteur de pression avec une sortie 4–20 mA.
- Un détecteur de niveau bas.
- Un détecteur de niveau haut.

Les raccordements nécessaires sont :

| Instrument | Type de signal | Entrée automate |
|---|---|---|
| Transmetteur de pression | Analogique 4–20 mA | AI |
| Détecteur de niveau bas | TOR | DI |
| Détecteur de niveau haut | TOR | DI |

Bilan des entrées nécessaires :

- 1 entrée analogique (AI).
- 2 entrées numériques (DI).

**Remarque :** les adresses exactes des entrées dépendent de la configuration matérielle de l'automate et des modules utilisés.

## 9. Importance pour la maintenance industrielle

La distinction entre capteur de mesure et détecteur est importante pour les techniciens de maintenance.

Elle permet notamment de :

- Choisir correctement un instrument de remplacement.
- Identifier le type de signal à contrôler.
- Diagnostiquer une panne de mesure ou de détection.
- Vérifier le raccordement à l'automate.
- Comprendre les informations utilisées par le système de commande.

Exemples de pannes :

| Équipement | Symptôme | Contrôle à effectuer |
|---|---|---|
| Transmetteur de pression | Valeur incorrecte sur l'IHM | Vérifier la mesure, l'alimentation et le signal 4–20 mA |
| Détecteur inductif | Pièce non détectée | Vérifier l'alimentation, le câblage et la distance de détection |
| Détecteur de niveau haut | Alarme absente | Vérifier le détecteur, son raccordement et l'entrée automate |

## 10. Exercices d'application

**Exercice 1**

Un détecteur inductif détecte la présence d'une pièce métallique.

Pourquoi peut-on également le considérer comme un capteur au sens physique ?

**Correction :** parce qu'il réagit à une perturbation de son champ électromagnétique et transforme cette réaction en une information électrique exploitable.

**Exercice 2**

Quelle est la différence entre un transmetteur de niveau et un détecteur de niveau haut ?

**Correction :** le transmetteur fournit une information permettant de connaître le niveau du liquide, tandis que le détecteur signale que le niveau a atteint un seuil déterminé.

**Exercice 3**

Un transmetteur de pression possède une sortie 4–20 mA. À quel type d'entrée de l'automate doit-il être raccordé ?

**Correction :** à une entrée analogique (AI) compatible avec le signal 4–20 mA.

**Exercice 4**

Une installation possède :
- Un transmetteur de pression 4–20 mA.
- Un détecteur de niveau bas TOR.
- Un détecteur de niveau haut TOR.

Combien faut-il d'entrées analogiques et numériques ?

**Correction :**
- 1 entrée analogique (AI).
- 2 entrées numériques (DI).

## 11. Synthèse de la leçon

Le capteur et le détecteur sont deux notions étroitement liées.

Le capteur réagit à une grandeur physique pour fournir une information exploitable. Il peut être utilisé pour mesurer une valeur.

Le détecteur réagit également à un phénomène physique, mais sa fonction principale est de signaler une présence, une absence ou un état particulier.

Il faut donc retenir :

- Le capteur de mesure permet de connaître une grandeur.
- Le détecteur permet principalement de reconnaître un état.
- Un détecteur est un capteur au sens physique.
- Un transmetteur peut fournir un signal normalisé, comme 4–20 mA.
- Une mesure analogique est généralement raccordée à une entrée AI.
- Une information TOR est généralement raccordée à une entrée DI.

**Fin de la leçon 03.**
