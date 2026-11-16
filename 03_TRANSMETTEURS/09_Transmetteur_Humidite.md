# LEÇON 09 — TRANSMETTEURS D’HUMIDITÉ INDUSTRIELLE

## 1. Objectifs de la leçon

À la fin de cette leçon, nous devons être capables de :

- Distinguer l'humidité absolue de l'humidité relative.
- Comprendre le fonctionnement des capteurs d'humidité.
- Identifier les principales technologies de mesure.
- Comprendre le fonctionnement d'un transmetteur d'humidité.
- Exploiter un signal analogique 4–20 mA.
- Comprendre le rôle du point de rosée dans les installations industrielles.
- Intégrer un transmetteur d'humidité à un automate Siemens S7-1200.
- Identifier les principales anomalies et effectuer un premier diagnostic.

---

## 2. Généralités sur l'humidité

L'humidité représente la quantité de vapeur d'eau présente dans l'air.

Dans l'industrie, sa surveillance est importante pour garantir la qualité des produits, protéger les équipements et maintenir de bonnes conditions de fonctionnement.

Il existe plusieurs grandeurs permettant de caractériser l'humidité de l'air.

### 2.1. Humidité absolue

L'humidité absolue représente la masse de vapeur d'eau contenue dans un volume donné d'air.

Elle s'exprime généralement en grammes par mètre cube (g/m³).

**Exemple :**

Un volume d'air de 1 m³ contient 12 grammes de vapeur d'eau.

L'humidité absolue est donc :

Humidité absolue = 12 g/m³.

### 2.2. Humidité relative

L'humidité relative (HR) représente le rapport entre la quantité de vapeur d'eau réellement présente dans l'air et la quantité maximale de vapeur d'eau que cet air peut contenir à la même température.

Elle s'exprime en pourcentage (% HR).

**Exemple :**

Une humidité relative de 75 % signifie que l'air contient 75 % de la quantité maximale de vapeur d'eau qu'il pourrait contenir à cette température.

### 2.3. Influence de la température

L'humidité relative dépend fortement de la température.

Lorsque l'air est chauffé sans ajout ni retrait de vapeur d'eau, sa capacité à contenir de la vapeur d'eau augmente. Son humidité relative diminue généralement.

Inversement, lorsque l'air est refroidi sans changement de sa teneur en vapeur d'eau, son humidité relative augmente.

**Exemple :**

Dans une salle industrielle, l'air présente une humidité relative de 75 % à 20 °C.

Si cet air est chauffé sans modification de sa teneur en vapeur d'eau, son humidité relative diminue.

Cette propriété est importante dans les installations de climatisation, de ventilation et de séchage industriel.

---

## 3. Technologies des capteurs d'humidité

Les capteurs d'humidité permettent de détecter les variations de la teneur en vapeur d'eau dans l'air.

Les deux principales technologies étudiées sont les technologies capacitive et résistive.

### 3.1. Capteur capacitif

Le capteur capacitif utilise un matériau sensible à l'humidité placé entre deux électrodes.

Lorsque l'humidité change, les propriétés électriques du matériau changent, notamment sa capacité électrique.

Le circuit électronique mesure cette variation afin de déterminer l'humidité relative.

**Principe :**

Variation de l'humidité → Variation de la capacité électrique → Traitement électronique → Mesure de l'humidité.

### 3.2. Capteur résistif

Le capteur résistif utilise un matériau dont la résistance électrique varie en fonction de l'humidité.

Lorsque le matériau absorbe ou libère de l'humidité, ses propriétés électriques changent.

Le circuit électronique mesure cette variation de résistance pour déterminer l'humidité.

**Principe :**

Variation de l'humidité → Variation de la résistance électrique → Traitement électronique → Mesure de l'humidité.

### 3.3. Comparaison des deux technologies

| Critère | Capteur capacitif | Capteur résistif |
|---|---|---|
| Grandeur électrique mesurée | Capacité électrique | Résistance électrique |
| Principe | Variation de capacité | Variation de résistance |
| Application | Mesure de l'humidité relative | Mesure de l'humidité relative |
| Utilisation | Instruments industriels et systèmes HVAC | Certains instruments de mesure d'humidité |

Le choix dépend des performances recherchées, de l'environnement, de la précision et des caractéristiques du fabricant.

---

## 4. Transmetteur d'humidité industrielle

### 4.1. Définition

Un transmetteur d'humidité est un appareil qui mesure l'humidité à l'aide d'un capteur, traite le signal obtenu et fournit une sortie exploitable par un système de contrôle ou de supervision.

Il peut notamment fournir :

- Un signal analogique 4–20 mA.
- Un signal analogique 0–10 V.
- Une communication numérique, selon le modèle.

### 4.2. Différence entre capteur et transmetteur

Le capteur détecte les variations d'humidité.

Le transmetteur exploite cette information et la transforme en un signal normalisé ou numérique destiné à un système de contrôle.

**Chaîne de mesure :**

Humidité de l'air → Capteur → Électronique de traitement → Sortie du transmetteur → Automate programmable.

### 4.3. Exemple industriel

Dans une salle de stockage, un transmetteur mesure l'humidité relative.

Il est configuré avec :

- Plage minimale : 0 % HR.
- Plage maximale : 100 % HR.
- Signal de sortie : 4–20 mA.

L'automate reçoit le courant et calcule la valeur d'humidité correspondante.

---

## 5. Conversion du signal 4–20 mA

Le signal 4–20 mA permet de transmettre une mesure analogique entre un transmetteur et un automate programmable.

Pour une plage de mesure de 0 à 100 % HR :

| Humidité relative | Courant de sortie |
|---:|---:|
| 0 % HR | 4 mA |
| 25 % HR | 8 mA |
| 50 % HR | 12 mA |
| 62,5 % HR | 14 mA |
| 75 % HR | 16 mA |
| 87,5 % HR | 18 mA |
| 100 % HR | 20 mA |

### 5.1. Formule de conversion

La formule générale est :

HR = LRV + [(I - 4) / 16] × (URV - LRV)

Avec :

- HR : humidité relative calculée.
- I : courant mesuré en mA.
- LRV : valeur minimale de la plage de mesure.
- URV : valeur maximale de la plage de mesure.

Pour une plage de 0 à 100 % HR :

HR = [(I - 4) / 16] × 100

### 5.2. Exemple de calcul

Un transmetteur possède une plage de mesure de 0 à 100 % HR.

L'automate mesure un courant de 14 mA.

Calcul :

HR = [(14 - 4) / 16] × 100

HR = (10 / 16) × 100

**HR = 62,5 %**

L'humidité relative mesurée est donc de 62,5 % HR.

### 5.3. Pourquoi utiliser le 4–20 mA ?

Le signal 4–20 mA présente plusieurs avantages :

- Bonne immunité aux perturbations électriques.
- Transmission sur de longues distances.
- Détection possible de certaines anomalies de boucle.
- Facilité d'intégration dans les systèmes industriels.

Le courant de 4 mA représente le zéro de mesure, appelé zéro vivant.

Un courant nul peut notamment indiquer une coupure de boucle ou un défaut d'alimentation. Il ne permet toutefois pas, à lui seul, d'identifier précisément l'origine du problème.

---

## 6. Point de rosée et applications industrielles

### 6.1. Définition du point de rosée

Le point de rosée est la température à laquelle l'air, refroidi à pression donnée et sans modification de sa teneur en vapeur d'eau, atteint la saturation et commence à condenser.

Lorsque la température de l'air atteint son point de rosée, de l'eau liquide peut apparaître.

### 6.2. Importance du point de rosée dans l'air comprimé

Dans les réseaux d'air comprimé, la surveillance du point de rosée permet de contrôler les performances des sécheurs.

Une humidité excessive peut provoquer :

- La corrosion des canalisations.
- La détérioration des électrovannes.
- Des dysfonctionnements des instruments pneumatiques.
- La contamination des produits dans certaines industries.

**Exemple industriel :**

Un sécheur d'air comprimé délivre normalement de l'air avec un point de rosée sous pression de -20 °C.

Si le point de rosée remonte à +5 °C, cela peut indiquer une dégradation des performances du sécheur.

Une intervention de maintenance peut alors être nécessaire.

Attention : le point de rosée sous pression doit être interprété en tenant compte de la pression du réseau. Les valeurs acceptables dépendent des exigences de l'installation.

### 6.3. Principales applications industrielles

| Installation | Objectif de la mesure |
|---|---|
| Sécheur d'air comprimé | Surveiller l'humidité de l'air comprimé |
| Salle électrique | Limiter les risques de condensation |
| Industrie agroalimentaire | Contrôler les conditions de conservation |
| Industrie pharmaceutique | Maintenir les conditions environnementales requises |
| Climatisation industrielle | Réguler l'humidité de l'air |
| Entrepôt de stockage | Surveiller les conditions de conservation |

Dans les réseaux d'air comprimé, on utilise souvent des transmetteurs de point de rosée plutôt que de simples transmetteurs d'humidité relative.

---

## 7. Intégration au Siemens S7-1200

### 7.1. Principe de raccordement

Un transmetteur d'humidité équipé d'une sortie 4–20 mA peut être raccordé à une entrée analogique compatible de l'automate.

La chaîne de mesure est :

Transmetteur d'humidité → Module d'entrée analogique → S7-1200 → WinCC.

### 7.2. Attention à la compatibilité des entrées analogiques

Sur une CPU Siemens S7-1200 standard comme la CPU 1214C, les entrées analogiques intégrées sont généralement des entrées en tension 0–10 V.

Elles ne doivent donc pas être considérées comme des entrées directement compatibles avec un transmetteur 4–20 mA.

Pour recevoir directement le signal 4–20 mA, il faut utiliser un module d'entrée analogique compatible, par exemple une référence appropriée de la gamme SM 1231.

La référence exacte du module, ses caractéristiques électriques et son schéma de raccordement doivent toujours être vérifiés dans la documentation Siemens.

### 7.3. Affichage sur WinCC

Une fois le signal correctement acquis et mis à l'échelle dans le programme automate, WinCC peut afficher :

- L'humidité relative en % HR.
- Les seuils de préalarme et d'alarme.
- L'évolution de l'humidité dans le temps.
- Les défauts de mesure.

**Exemple :**

Un transmetteur mesure une humidité relative de 75 % HR.

L'automate reçoit le signal correspondant de 16 mA et affiche 75 % HR sur l'IHM.

---

## 8. Diagnostic des défauts

Un transmetteur d'humidité peut présenter plusieurs anomalies pendant son fonctionnement.

| Symptôme | Causes possibles |
|---|---|
| Valeur affichée à 0 % | Défaut de câblage, alimentation ou configuration |
| Valeur instable | Perturbations électriques, condensation ou capteur défectueux |
| Valeur bloquée | Capteur ou électronique défectueux |
| Valeur incohérente | Mauvais étalonnage ou mauvaise configuration |
| Signal inférieur à 4 mA | Défaut de boucle ou signalisation de défaut selon le modèle |
| Signal supérieur à 20 mA | Défaut possible ou signalisation spécifique selon la configuration |

### 8.1. Méthode de diagnostic

Lorsqu'une mesure d'humidité devient incohérente, le technicien doit procéder méthodiquement.

1. Vérifier la présence de l'alimentation 24 V DC, si le transmetteur fonctionne sous cette tension.
2. Vérifier les connexions et le câblage.
3. Contrôler la continuité des conducteurs.
4. Mesurer le courant de la boucle avec un multimètre adapté.
5. Comparer le courant mesuré à la valeur attendue.
6. Vérifier la configuration du transmetteur.
7. Contrôler le paramétrage de l'entrée analogique de l'automate.
8. Comparer la mesure avec un instrument de référence approprié.

Il ne faut pas remplacer immédiatement un transmetteur sans avoir recherché l'origine du défaut.

---

## 9. Synthèse de la leçon

| Notion | À retenir |
|---|---|
| Humidité absolue | Masse de vapeur d'eau par volume d'air, généralement en g/m³ |
| Humidité relative | Rapport exprimé en pourcentage |
| Capteur capacitif | Mesure une variation de capacité électrique |
| Capteur résistif | Mesure une variation de résistance électrique |
| Transmetteur | Traite la mesure et fournit un signal exploitable |
| Signal 4–20 mA | Signal analogique normalisé |
| Point de rosée | Température à laquelle commence la condensation |
| S7-1200 | Nécessite une entrée compatible avec le signal du transmetteur |

### Formule essentielle

Pour une plage de 0 à 100 % HR :

HR = [(I - 4) / 16] × 100

---

## 10. Évaluation finale

### Question 1

Quelle est la différence fondamentale entre l'humidité absolue et l'humidité relative ?

A. L'humidité absolue s'exprime en pourcentage et l'humidité relative en grammes par mètre cube.

B. L'humidité absolue représente une quantité de vapeur d'eau, tandis que l'humidité relative représente un rapport exprimé en pourcentage.

C. Les deux grandeurs représentent exactement la même chose.

**Réponse : B.**

### Question 2

Quel est le principe de fonctionnement d'un capteur d'humidité capacitif ?

A. Il mesure la variation de résistance d'un matériau.

B. Il mesure la variation de capacité électrique d'un matériau sensible à l'humidité.

C. Il mesure directement la pression atmosphérique.

**Réponse : B.**

### Question 3

Un transmetteur d'humidité possède une plage de mesure de 0 à 100 % HR et une sortie de 4–20 mA.

L'automate mesure 18 mA. Quelle est l'humidité relative correspondante ?

A. 75 % HR.

B. 87,5 % HR.

C. 90 % HR.

**Réponse : B.**

Calcul :

HR = [(18 - 4) / 16] × 100

HR = 87,5 %.

### Question 4

Dans un réseau d'air comprimé industriel, quel est le rôle principal de la surveillance du point de rosée ?

A. Mesurer la vitesse de rotation du compresseur.

B. Détecter le risque de condensation de l'eau dans les canalisations.

C. Mesurer le débit d'air comprimé.

**Réponse : B.**

### Question 5

Tu dois raccorder un transmetteur d'humidité avec une sortie 4–20 mA à une CPU Siemens S7-1200 dont les entrées analogiques intégrées acceptent uniquement 0–10 V.

Quelle solution choisis-tu ?

A. Raccorder directement le transmetteur sur l'entrée 0–10 V.

B. Utiliser un module d'entrée analogique compatible 4–20 mA.

C. Raccorder le transmetteur sur une entrée numérique TOR.

**Réponse : B.**

### Résultat de l'évaluation

**5 bonnes réponses sur 5 — 20/20.**

---

## 11. Conclusion

Les transmetteurs d'humidité industrielle jouent un rôle important dans la surveillance et la régulation des conditions environnementales.

Ils permettent de contrôler l'humidité dans les salles industrielles, les installations de climatisation, les sécheurs d'air comprimé et les zones de stockage.

La maîtrise des technologies capacitive et résistive, du signal 4–20 mA et du point de rosée permet au technicien de mieux comprendre les systèmes de mesure et d'assurer leur maintenance.

La bonne intégration de ces instruments dans un automate programmable contribue à améliorer la surveillance et la fiabilité des installations industrielles.
