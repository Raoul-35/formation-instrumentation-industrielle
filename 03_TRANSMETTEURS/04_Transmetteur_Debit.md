# LEÇON 04 — TRANSMETTEUR DE DÉBIT INDUSTRIEL

## 1. Définition du débit

Le débit représente la quantité de fluide qui traverse une section de canalisation pendant une unité de temps.

Il existe deux grandes catégories :

### 1.1. Débit volumique (Qv)

Il représente le volume de fluide transporté par unité de temps.

Unités courantes :

- m³/h : mètres cubes par heure.

- L/min : litres par minute.

- L/s : litres par seconde.

Formule :

Qv = V / t

Avec :

- Qv : débit volumique.

- V : volume transporté.

- t : durée du transport.

Exemple : une pompe transfère 600 litres en 10 minutes.

Qv = 600 / 10 = 60 L/min.

### 1.2. Débit massique (Qm)

Il représente la masse de fluide transportée par unité de temps.

Unités courantes :

- kg/h.

- t/h.

- kg/s.

Exemple : une installation consomme 500 kg de vapeur par heure.

Son débit massique est de 500 kg/h.

## 2. Relation entre débit, section et vitesse

Dans une canalisation :

Qv = A × v

Avec :

- A : section intérieure de la canalisation en m².

- v : vitesse moyenne du fluide en m/s.

Cette relation montre que le débit augmente avec la vitesse du fluide lorsque la section reste constante.

## 3. Les principales technologies de mesure du débit

### 3.1. Débitmètre électromagnétique

#### Principe

Il fonctionne selon la loi de Faraday sur l'induction électromagnétique.

Les bobines produisent un champ magnétique. Lorsque le liquide conducteur traverse ce champ, une tension électrique est induite.

Des électrodes détectent cette tension, qui est liée à la vitesse du fluide.

L'électronique de traitement exploite cette information pour calculer le débit volumique.

#### Constitution

- Bobines électromagnétiques.

- Électrodes.

- Tube de mesure.

- Revêtement isolant.

- Électronique de traitement.

#### Applications

- Eau potable.

- Eaux usées.

- Boues conductrices.

- Produits chimiques conducteurs.

#### Limitation

Il ne convient généralement pas aux fluides non conducteurs comme les huiles et les hydrocarbures.

### 3.2. Débitmètre ultrasonique

#### Principe

Il utilise des ondes ultrasonores pour déterminer la vitesse du fluide.

Deux méthodes principales existent.

**A. Méthode par temps de transit**

Deux capteurs échangent des ultrasons dans le sens du fluide et dans le sens opposé.

La différence entre les temps de propagation permet de déterminer la vitesse du fluide.

**B. Méthode Doppler**

Elle exploite le décalage de fréquence des ultrasons réfléchis par des particules ou des bulles présentes dans le fluide.

#### Types d'installation

- Intrusif : les éléments de mesure sont en contact avec le fluide.

- Clamp-on : les capteurs sont fixés à l'extérieur de la conduite.

#### Avantage du Clamp-on

Il permet de mesurer le débit sans découper la canalisation et sans nécessairement interrompre le processus.

#### Applications

- Réseaux d'eau industrielle.

- Circuits de refroidissement.

- Traitement d'eau.

- Certaines canalisations de produits chimiques.

La qualité de mesure dépend notamment du fluide, du matériau de la conduite et des conditions d'installation.

### 3.3. Débitmètre à pression différentielle

#### Principe

Un élément de restriction, comme une plaque à orifice, est installé dans la canalisation.

Le passage réduit provoque une accélération du fluide et une diminution de sa pression statique.

Une différence de pression apparaît entre l'amont et l'aval de la restriction.

Un transmetteur de pression différentielle mesure cette différence.

#### Relation fondamentale

Qv = K × √ΔP

Avec :

- Qv : débit volumique.

- K : constante dépendant de la géométrie et des caractéristiques du fluide.

- ΔP : pression différentielle.

Le débit est proportionnel à la racine carrée de la pression différentielle, dans les conditions usuelles d'application.

Exemple :

Si ΔP est multipliée par 4, le débit est multiplié par 2.

Applications :

- Mesure du débit de vapeur.

- Mesure du débit de gaz.

- Mesure du débit de liquides.

## 4. Comparaison des technologies

| **Technologie** | **Principe** | **Avantage** | **Limitation** |
| :-: | :-: | :-: | :-: |
| Électromagnétique | Induction électromagnétique | Bonne précision pour les liquides conducteurs | Ne convient généralement pas aux huiles |
| Ultrasonique | Ondes ultrasonores | Installation Clamp-on possible | Sensible aux conditions d'installation |
| Pression différentielle | Différence de pression | Utilisable pour liquides, gaz et vapeur | Entraîne une perte de charge |

## 5. Transmission du signal vers le PLC

Un transmetteur de débit peut fournir un signal normalisé de 4–20 mA.

Exemple de configuration :

- LRV = 0 m³/h.

- URV = 100 m³/h.

- Span = 100 m³/h.

| **Débit** | **Signal** |
| :-: | :-: |
| 0 m³/h | 4 mA |
| 25 m³/h | 8 mA |
| 50 m³/h | 12 mA |
| 75 m³/h | 16 mA |
| 100 m³/h | 20 mA |

Formule de conversion :

Q = LRV + ((I - 4) / 16) × (URV - LRV)

Exemple : pour 14 mA sur une plage de 0 à 100 m³/h :

Q = 0 + ((14 - 4) / 16) × 100

Q = 62,5 m³/h.

Le PLC reçoit le courant sur une entrée analogique compatible, convertit le signal en valeur numérique et applique l'échelle configurée.

## 6. Débit instantané et débit totalisé

### 6.1. Débit instantané

Il représente le débit mesuré à un instant donné.

Exemple : 45 m³/h.

### 6.2. Débit totalisé

Il représente le volume cumulé pendant une période.

Formule :

V = Q × t

Exemple : une pompe fonctionne à 20 m³/h pendant 3 heures.

V = 20 × 3 = 60 m³.

Le totalisateur peut être intégré au débitmètre, au PLC ou au système de supervision.

## 7. Maintenance et diagnostic

Un débitmètre peut fournir une mesure incorrecte à cause de plusieurs problèmes.

| **Point de contrôle** | **Risque** |
| :-: | :-: |
| Sens de circulation | Mesure incorrecte |
| Présence de bulles d'air | Mesure instable selon la technologie |
| Conduite non remplie | Erreur de mesure |
| Encrassement | Perturbation de la mesure |
| Câblage électrique | Perte ou instabilité du signal |
| Configuration | Mauvaise valeur affichée |

### Exemple de diagnostic

Une pompe fonctionne, mais l'IHM affiche un débit de 0 m³/h.

Démarche :

1. Vérifier si le fluide circule réellement.

2. Vérifier l'alimentation du transmetteur.

3. Contrôler le signal 4–20 mA.

4. Vérifier le câblage et l'entrée analogique du PLC.

5. Vérifier la configuration et la mise à l'échelle.

Une pompe en fonctionnement ne signifie pas nécessairement qu'il y a un débit. Une vanne fermée, une conduite obstruée ou une pompe désamorcée peuvent empêcher le transfert du fluide.

## 8. Synthèse

Le transmetteur de débit permet de mesurer et de transmettre la quantité de fluide circulant dans une installation industrielle.

Les principales technologies étudiées sont :

- Électromagnétique.

- Ultrasonique.

- Pression différentielle.

Le signal 4–20 mA permet au PLC de recevoir la mesure et de l'exploiter pour l'affichage, les alarmes, la régulation et la totalisation.

## 9. Évaluation finale

1. Quelle est la différence entre débit volumique et débit massique ?

2. Quelle technologie permet de mesurer le débit sans découper une conduite ?

3. Quel est le principe du débitmètre à pression différentielle ?

4. Un transmetteur configuré de 0 à 100 m³/h délivre 16 mA. Quel débit correspond à ce courant ?

5. Une pompe transfère 30 m³/h pendant 5 heures. Quel volume total est transféré ?

### Résultats de l'évaluation

Score obtenu : 5/5, soit 100 %.

