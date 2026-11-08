# LEÇON 03 — TRANSMETTEUR DE NIVEAU INDUSTRIEL

## 1. Définition et rôle

Un transmetteur de niveau est un instrument qui mesure en continu la hauteur ou la quantité d'un produit présent dans une cuve, un réservoir, un bassin ou un silo.

Il transforme la mesure en un signal exploitable par un système de contrôle-commande : automate programmable industriel (API/PLC), régulateur ou système de supervision.

Exemple : une cuve de 5 mètres peut avoir un niveau de :
- 0 % : cuve vide ;
- 25 % : 1,25 m ;
- 50 % : 2,5 m ;
- 75 % : 3,75 m ;
- 100 % : 5 m.

## 2. Différence entre transmetteur et détecteur de niveau

| Appareil | Information fournie | Exemple |
|---|---|---|
| Transmetteur de niveau | Mesure continue | Niveau : 63 % |
| Détecteur de niveau | État tout ou rien (TOR) | Niveau haut atteint : OUI/NON |

Une installation peut utiliser simultanément un transmetteur pour connaître le niveau réel et des détecteurs pour signaler des seuils haut ou bas.

## 3. Mesure hydrostatique

### 3.1. Principe

La mesure hydrostatique repose sur la pression exercée par la colonne de liquide.

La pression hydrostatique est donnée par :

P = ρ × g × h

Avec :
- P : pression hydrostatique en pascals (Pa) ;
- ρ : masse volumique du liquide en kg/m³ ;
- g : accélération de la pesanteur, environ 9,81 m/s² ;
- h : hauteur de liquide en mètres (m).

Pour une eau de masse volumique de 1 000 kg/m³ et une hauteur de 5 m :

P = 1 000 × 9,81 × 5 = 49 050 Pa

Soit environ 0,49 bar.

### 3.2. Configurations courantes

- Transmetteur monté au fond de la cuve, raccordé à une prise de pression.
- Sonde hydrostatique immergée et suspendue dans le liquide.

Dans une cuve ouverte, la pression mesurée au fond est liée à la hauteur de liquide.

Dans une cuve fermée et pressurisée, il faut tenir compte de la pression présente au-dessus du liquide. Une mesure différentielle peut être nécessaire.

### 3.3. Influence de la masse volumique

La pression hydrostatique dépend de la masse volumique.

Si la hauteur reste constante mais que la masse volumique diminue, la pression diminue également. Le transmetteur peut alors indiquer un niveau inférieur au niveau réel si la configuration suppose une masse volumique constante.

### 3.4. Applications

- Réservoirs d'eau industrielle ;
- Stations de pompage ;
- Forages ;
- Châteaux d'eau ;
- Bassins de traitement des eaux.

## 4. Mesure ultrasonique

### 4.1. Principe

Le transmetteur ultrasonique utilise des ondes sonores à haute fréquence.

Fonctionnement :
1. Il émet une onde ultrasonique vers la surface du liquide.
2. L'onde rencontre la surface.
3. Une partie de l'onde est réfléchie.
4. Le transmetteur reçoit l'écho.
5. Il mesure le temps aller-retour.
6. Il calcule la distance jusqu'à la surface.

La distance est calculée par :

d = (v × t) / 2

Avec :
- d : distance entre le transmetteur et la surface ;
- v : vitesse du son dans l'air ;
- t : temps aller-retour.

La division par deux est nécessaire parce que l'onde effectue un trajet aller et un trajet retour.

### 4.2. Calcul du niveau

Si la hauteur de référence de la cuve est de 5 m et que la distance mesurée jusqu'à la surface est de 3,43 m :

h = 5 − 3,43 = 1,57 m

Niveau (%) = (1,57 / 5) × 100 = 31,4 %

### 4.3. Avantages et limites

Avantages :
- Mesure sans contact avec le liquide ;
- Installation généralement simple ;
- Pas de sonde immergée ;
- Adapté à de nombreuses applications.

Limites :
- Sensibilité à la mousse ;
- Influence possible de la vapeur et des variations de température de l'air ;
- Perturbations possibles par les turbulences et les obstacles ;
- Nécessité de respecter une distance minimale de mesure appelée zone morte ou distance de blocage.

### 4.4. Applications

- Bassins de traitement des eaux usées ;
- Réservoirs d'eau ;
- Cuves de stockage compatibles avec cette technologie.

## 5. Mesure radar

### 5.1. Principe

Le transmetteur radar utilise des ondes électromagnétiques.

Fonctionnement :
1. Il émet une onde électromagnétique vers la surface du produit.
2. Une partie de l'énergie est réfléchie.
3. Le transmetteur reçoit le signal réfléchi.
4. Il analyse le temps de propagation ou le décalage de fréquence, selon la technologie.
5. Il détermine la distance jusqu'à la surface.
6. Il calcule le niveau.

### 5.2. Radar sans contact

Le transmetteur est installé au sommet de la cuve.

Exemple :
- Hauteur de référence : 5 m ;
- Distance mesurée : 1,5 m.

Hauteur du liquide :

h = 5 − 1,5 = 3,5 m

Niveau :

Niveau (%) = (3,5 / 5) × 100 = 70 %

### 5.3. Radar à ondes guidées (GWR)

Le radar à ondes guidées utilise une sonde ou un câble introduit dans la cuve.

L'impulsion électromagnétique se propage le long de cette sonde. Une partie est réfléchie lorsqu'elle rencontre une discontinuité diélectrique, notamment la surface du produit.

Le transmetteur exploite le signal réfléchi pour déterminer le niveau.

### 5.4. Avantages et limites

Avantages :
- Mesure sans contact pour le radar classique ;
- Faible sensibilité aux variations de température de l'air ;
- Généralement moins sensible à la vapeur que l'ultrasonique ;
- Adapté à de nombreuses applications industrielles.

Limites :
- Coût généralement plus élevé ;
- Performances dépendantes du produit, de la géométrie de la cuve et des obstacles ;
- Choix du modèle nécessaire selon les conditions de température et de pression.

La présence de mousse peut également perturber certaines mesures radar selon ses caractéristiques et le modèle utilisé.

## 6. Mesure capacitive

### 6.1. Principe

Le transmetteur capacitif exploite la variation de capacité électrique liée à la présence du produit autour de sa sonde.

La capacité d'un condensateur dépend notamment :
- De la surface des électrodes ;
- De la distance entre les électrodes ;
- Des propriétés électriques du matériau situé entre elles.

Lorsque le niveau du produit change, la partie de la sonde entourée par le liquide change également. Les propriétés diélectriques autour de la sonde varient et modifient la capacité mesurée.

L'électronique du transmetteur exploite cette variation pour déterminer le niveau.

### 6.2. Avantages et limites

Applications :
- Certaines cuves de produits chimiques ;
- Certaines installations alimentaires ;
- Certains produits liquides ou solides en vrac.

Limites :
- La mesure dépend des propriétés électriques du produit ;
- La conductivité et la permittivité doivent être prises en compte ;
- Un choix et un étalonnage adaptés sont nécessaires.

## 7. Comparaison des quatre technologies

| Technologie | Grandeur physique exploitée | Contact avec le produit |
|---|---|---|
| Hydrostatique | Pression | Oui, généralement |
| Ultrasonique | Propagation des ondes sonores | Non |
| Radar sans contact | Ondes électromagnétiques | Non |
| Radar à ondes guidées | Ondes électromagnétiques guidées | Sonde en contact |
| Capacitive | Capacité électrique | Généralement oui |

## 8. Sorties des transmetteurs de niveau

Selon le modèle, un transmetteur peut fournir :
- 4–20 mA ;
- 0–10 V ;
- Des communications numériques : HART, PROFIBUS PA, FOUNDATION Fieldbus ou autres protocoles compatibles.

Le signal 4–20 mA est très utilisé dans l'industrie.

### 8.1. Exemple de conversion

Un transmetteur est configuré pour mesurer de 0 à 10 m et fournit un signal de 4 à 20 mA.

| Niveau | Hauteur | Courant |
|---|---:|---:|
| 0 % | 0 m | 4 mA |
| 25 % | 2,5 m | 8 mA |
| 50 % | 5 m | 12 mA |
| 75 % | 7,5 m | 16 mA |
| 100 % | 10 m | 20 mA |

Formule de conversion du courant vers le niveau :

Niveau (%) = ((I − 4) / 16) × 100

Formule de conversion vers la hauteur :

h = (Niveau (%) / 100) × Hmax

Avec :
- I : courant mesuré en mA ;
- Hmax : hauteur maximale configurée.

## 9. Application à un automate programmable industriel

Exemple d'installation :
- Une cuve d'eau ;
- Un transmetteur radar 4–20 mA ;
- Un automate Siemens S7-1200 ;
- Une pompe de remplissage ;
- Une IHM WinCC.

L'automate reçoit la mesure analogique, la met à l'échelle et peut :
- Afficher le niveau en mètres ou en pourcentage ;
- Déclencher une alarme de niveau bas ;
- Déclencher une alarme de niveau haut ;
- Commander une pompe selon le programme.

Attention : les entrées analogiques intégrées d'une CPU S7-1200 1214C standard sont en 0–10 V. Pour recevoir directement un signal 4–20 mA, il faut un module d'entrée analogique compatible avec le courant, choisi selon sa référence exacte.

Le transmetteur mesure et transmet l'information. C'est le programme de l'automate qui décide des actions à effectuer.

## 10. Exemple de commande avec hystérésis

Considérons une pompe de remplissage commandée selon les seuils suivants :
- Niveau inférieur ou égal à 20 % : démarrage de la pompe ;
- Niveau supérieur ou égal à 80 % : arrêt de la pompe ;
- Entre 20 et 80 % : maintien de l'état précédent.

Cette commande évite les démarrages et arrêts trop fréquents lorsque le niveau oscille autour d'un seuil.

Les protections électriques et mécaniques de la pompe doivent être traitées séparément dans le système de commande.

## 11. Synthèse à retenir

- Le transmetteur hydrostatique déduit le niveau à partir de la pression.
- Le transmetteur ultrasonique utilise des ondes sonores.
- Le transmetteur radar utilise des ondes électromagnétiques.
- Le transmetteur capacitif exploite la variation de capacité électrique.
- Le signal 4–20 mA permet de transmettre une mesure continue à un automate.
- Le choix de la technologie dépend du produit, de la cuve et des conditions de fonctionnement.

## 12. Évaluation

1. Quelle technologie utilise la pression exercée par une colonne de liquide ?
2. Pourquoi divise-t-on par deux le temps de propagation dans une mesure ultrasonique ?
3. Quelle est la différence fondamentale entre l'ultrasonique et le radar ?
4. Quel courant correspond à 50 % d'une plage 4–20 mA ?
5. Pourquoi une variation de masse volumique peut-elle fausser une mesure hydrostatique ?

---
Fin de la leçon 03 — Transmetteur de niveau industriel.
