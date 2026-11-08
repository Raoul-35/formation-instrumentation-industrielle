# LEÇON 04 — TRANSMETTEUR DE PRESSION INDUSTRIEL

## 1. Définition et rôle

Un transmetteur de pression est un instrument qui mesure la pression d'un fluide (liquide ou gaz) et convertit cette mesure en un signal exploitable par un système de contrôle-commande.

Les signaux de sortie les plus courants sont :
- 4–20 mA ;
- 0–10 V ;
- des signaux numériques ou protocoles de communication, selon le modèle.

Le transmetteur permet de surveiller une pression, de déclencher des alarmes ou de participer à la régulation d'un procédé industriel.

## 2. Applications industrielles

On rencontre les transmetteurs de pression dans :
- Les conduites de refoulement des pompes.
- Les réseaux d'air comprimé.
- Les chaudières et circuits vapeur.
- Les installations hydrauliques.
- Les cuves et réservoirs.
- Les circuits de refroidissement.

Exemple : sur une station de pompage, un transmetteur installé sur la conduite de refoulement permet de surveiller la pression fournie par la pompe.

Le transmetteur effectue la mesure. C'est ensuite le programme de l'automate qui détermine les actions à réaliser.

## 3. Constitution générale

Un transmetteur de pression comprend généralement :
1. Un raccordement au procédé.
2. Une membrane sensible à la pression.
3. Un élément de mesure.
4. Un circuit électronique de traitement.
5. Une sortie électrique ou numérique.
6. Un boîtier de protection.

La membrane réagit à la pression appliquée. L'élément de mesure transforme cette déformation en une information électrique exploitable par l'électronique.

## 4. Principales technologies de mesure

### 4.1. Technologie piézorésistive

La pression provoque une déformation d'un élément sensible dont la résistance électrique varie.

L'électronique exploite cette variation pour déterminer la pression.

### 4.2. Technologie capacitive

La pression déplace une membrane et modifie la capacité électrique d'un condensateur.

Cette variation permet de déterminer la pression appliquée.

### 4.3. Technologie piézoélectrique

Certains matériaux produisent une charge électrique lorsqu'ils subissent une contrainte mécanique.

Cette technologie est notamment utilisée pour mesurer des pressions dynamiques et des phénomènes rapides.

Attention : ces technologies ne sont pas interchangeables dans toutes les applications. Le choix dépend du procédé et des caractéristiques recherchées.

## 5. Les différentes références de pression

Il faut distinguer trois notions.

### 5.1. Pression relative

Elle est mesurée par rapport à la pression atmosphérique.

Exemple : un manomètre indiquant 5 bar mesure généralement 5 bar relatifs.

### 5.2. Pression absolue

Elle est mesurée par rapport au vide absolu.

Relation :

P absolue = P relative + P atmosphérique

Exemple :

- Pression relative : 5 bar.
- Pression atmosphérique approximative : 1 bar.

P absolue ≈ 6 bar.

### 5.3. Pression différentielle

Elle représente la différence entre deux pressions.

ΔP = P amont − P aval

Exemple :

- Pression amont d'un filtre : 6 bar.
- Pression aval : 5,2 bar.

ΔP = 6 − 5,2 = 0,8 bar.

La pression différentielle permet notamment de surveiller l'encrassement d'un filtre.

## 6. Le transmetteur de pression différentielle

Un transmetteur de pression différentielle possède deux raccordements de pression :
- HP : côté haute pression.
- LP : côté basse pression.

Il mesure la différence entre ces deux pressions.

Applications :
- Surveillance de l'encrassement des filtres.
- Mesure de débit par organe déprimogène.
- Mesure de niveau hydrostatique dans certaines cuves.

Une augmentation de la différence de pression aux bornes d'un filtre peut indiquer son colmatage.

## 7. Sortie normalisée 4–20 mA

Un transmetteur peut convertir une plage de pression en un courant compris entre 4 et 20 mA.

Exemple : transmetteur configuré de 0 à 10 bar.

| Pression | Courant |
|---:|---:|
| 0 bar | 4 mA |
| 2,5 bar | 8 mA |
| 5 bar | 12 mA |
| 7,5 bar | 16 mA |
| 10 bar | 20 mA |

Formule de conversion de la pression vers le courant :

I = 4 + [(P − LRV) / (URV − LRV)] × 16

Formule inverse :

P = LRV + [(I − 4) / 16] × (URV − LRV)

Avec :
- I : courant mesuré en mA.
- P : pression.
- LRV : valeur basse configurée.
- URV : valeur haute configurée.

Exemple :

Pour une plage de 0 à 10 bar et un courant de 12 mA :

P = 0 + [(12 − 4) / 16] × 10

P = 5 bar.

## 8. LRV, URV, Range et Span

- LRV (Lower Range Value) : valeur basse de la plage configurée.
- URV (Upper Range Value) : valeur haute de la plage configurée.
- Range : plage de mesure configurée entre LRV et URV.
- Span : étendue de mesure, égale à URV − LRV.

Exemple :

- LRV = 2 bar.
- URV = 12 bar.
- Span = 10 bar.

À 12 mA, la pression correspond à :

P = 2 + [(12 − 4) / 16] × 10

P = 7 bar.

### Précision exprimée en pourcentage du span

Si la précision annoncée est de ±0,5 % du span et que le span vaut 10 bar :

Erreur maximale indicative = 0,005 × 10 = ±0,05 bar.

Il faut toujours vérifier si le fabricant exprime la précision en pourcentage du span, de la lecture ou d'une autre référence.

## 9. Boucle de courant 4–20 mA à deux fils

Dans une boucle classique à deux fils :
- Les deux conducteurs participent à l'alimentation du transmetteur.
- Le même circuit transporte le signal de mesure.
- Le courant varie en fonction de la pression mesurée.

Exemple :
- 0 bar : 4 mA.
- 5 bar : 12 mA.
- 10 bar : 20 mA.

### Le zéro vivant (Live Zero)

Le courant de 4 mA représente le début de la plage de mesure, et non une absence de signal.

Cela permet de distinguer :
- Une mesure normale à la valeur minimale : 4 mA.
- Une éventuelle perte de courant : 0 mA.

Un courant nul peut notamment provenir :
- D'un conducteur coupé.
- D'une alimentation absente.
- D'un mauvais raccordement.
- D'un transmetteur défaillant.

Le courant nul ne permet pas, à lui seul, d'identifier précisément la cause.

## 10. Raccordement à un automate programmable

La chaîne de mesure peut être représentée ainsi :

Transmetteur de pression → Boucle 4–20 mA → Entrée analogique → Automate → IHM.

L'entrée analogique mesure le courant et le convertit en une valeur numérique exploitable par la CPU.

### Attention au matériel Siemens S7-1200

La CPU S7-1200 1214C standard possède des entrées analogiques intégrées de type 0–10 V. Elles ne reçoivent pas directement un signal 4–20 mA.

Pour recevoir directement le courant, il faut choisir un module d'entrée analogique compatible, par exemple une version appropriée du SM 1231.

La famille SM 1231 existe en plusieurs variantes. Il faut vérifier la référence exacte, les plages de mesure et le schéma de raccordement avant toute installation.

Il faut également distinguer les entrées analogiques actives et passives. Le câblage dépend de la conception du module et du transmetteur.

## 11. Diagnostic et maintenance

En cas de mesure incohérente, vérifier méthodiquement :

1. L'alimentation du transmetteur.
2. Le câblage et les connexions.
3. L'état du raccordement au procédé.
4. Le courant réel dans la boucle.
5. La configuration LRV et URV.
6. Le diagnostic de l'entrée analogique.
7. L'affichage et la mise à l'échelle dans le système de contrôle.

Exemple : si WinCC affiche 0 bar, il faut déterminer si la pression est réellement nulle ou si la chaîne de mesure présente un défaut.

Les interventions électriques doivent respecter les procédures de sécurité et de consignation applicables.

## 12. Synthèse

Un transmetteur de pression :
- Mesure une pression physique.
- Utilise une technologie de détection adaptée.
- Convertit la mesure en un signal exploitable.
- Peut transmettre la mesure en 4–20 mA.
- Peut être utilisé pour surveiller la pression, le débit ou le niveau selon sa configuration.

À retenir : le transmetteur mesure et transmet l'information ; l'automate traite cette information et détermine les actions de commande.

## 13. Exercices de révision

**Exercice 1**

Un transmetteur est configuré de 0 à 10 bar. Quel courant correspond à 5 bar ?

**Exercice 2**

Un transmetteur possède une plage de 2 à 12 bar. Quel est son span ?

**Exercice 3**

Un filtre possède une pression amont de 8 bar et une pression aval de 7,5 bar. Calculer la pression différentielle.

**Exercice 4**

Pourquoi utilise-t-on 4 mA comme valeur basse au lieu de 0 mA ?

**Exercice 5**

Quel équipement faut-il ajouter à une CPU S7-1200 1214C standard pour recevoir directement un signal 4–20 mA ?

---
**Fin de la leçon 04 — Transmetteur de pression**
