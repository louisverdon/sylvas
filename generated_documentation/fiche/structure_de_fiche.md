# Structure de Fiche pour Sessions de JDR

> [!info] Objectif de ce document
> Ce document récapitule la structure idéale pour les fiches de jeu de rôle, permettant au MJ de s'y retrouver facilement pendant les sessions et d'avoir toutes les informations nécessaires organisées de façon logique et efficace.

## I. Organisation Générale
1. **Nom du lieu principal** (ville, village, donjon)
2. **Description générale** (5 phrases maximum)
3. **Liste des lieux d'intérêt avec liens et PNJ principaux** (organisés par quartier/zone)
4. **Détails des quartiers et leurs points d'intérêt**
5. **Zones à aventures** (si applicable)
6. **Événements spéciaux**

## II. Structure Détaillée

### A. En-tête de lieu
1. **Nom du lieu**
2. **Description immersive** (en italique, et toujours à la deuxième personne commençant par "Vous...")
3. **Liste des lieux d'intérêt avec PNJ** (organisés par quartier/zone)
   ```markdown
   ## Lieux d'Intérêt de la Ville/du Village
   - [[#Quartier/Zone 1]] : Lieu A (PNJ), Lieu B (PNJ)
   - [[#Quartier/Zone 2]] : Lieu C (PNJ), Lieu D (PNJ)
   ```

### B. Description des Quartiers/Zones
1. **Nom du quartier/zone**
2. **Description immersive** (en italique, commençant obligatoirement par "Vous...")
3. **Liste des points d'intérêt du quartier avec liens et PNJ**
   ```markdown
   ### Points d'intérêt du Quartier
   - [[#Lieu A]] : PNJ (rôle)
   - [[#Lieu B]] : PNJ (rôle)
   ```
4. **Détails de chaque lieu du quartier**

### C. Description des Points d'Intérêt
1. **Nom du lieu**
2. **Description immersive** (en italique, toujours à la deuxième personne commençant par "Vous..." et décrivant ce que le personnage voit, entend, ressent ou perçoit)
3. **PNJ présents**
   - Nom -- Description physique. **Intentions:** objectifs du PNJ
   - *Quêtes* ou informations importantes
4. **Objets interactifs**
5. **Événements déclencheurs** (en italique)
   ```markdown
   _Si événement déclencheur_: Conséquence
   ```
6. **Conditions temporelles** (uniquement si nécessaire)
   ```markdown
   > [!example] ⏰ Conditions Temporelles
   > - **Matinée (6h-12h):** Description/état du lieu
   > - **Soirée (18h-0h):** Description/état du lieu
   > - **Nuit (0h-6h):** `FERMÉ` ou description nocturne
   ```
7. **Informations commerciales** (dans des callouts avec emojis)
   ```markdown
   > [!note] 🏠 Services disponibles
   > **Service** — Description: `X pièces d'argent/or/cuivre`
   
   > [!tip] 🍺 Consommations
   > **Item** — Prix: `X pièces d'argent/or/cuivre`
   
   > [!tip] 💰 Offre de travail
   > **Tâche** — Récompense: `X pièces d'or par unité`
   
   > [!note] 💎 Trésor
   > **À récupérer:** Description du trésor
   ```

### D. Format des PNJ
1. **Nom (rôle)** -- description physique
2. **Intentions:** motivations et objectifs
3. **Si combat:** PV et dégâts
4. **Informations spéciales**

## III. Zones à Aventures
1. **Nom de la zone**
2. **Table de rencontres** (dans un callout spécial)
   ```markdown
   > [!warning] 🎲 Table d'Événements Aléatoires
   > **Lancez 1dX:**
   > 1. Description rencontre 1
   > 2. Description rencontre 2 → *Si condition*: Conséquence
   > ...
   > X. Description combat ─ `Y PV` ─ Dégâts: `1dZ`
   ```
3. **Description des rencontres possibles**
4. **Statistiques de combat** (format standardisé)
   ```markdown
   ─ `X PV` ─ Dégâts: `1dY`
   ```

## IV. Événements
1. **Nom de l'événement**
2. **Conditions de déclenchement** (en italique)
3. **Conséquences et récompenses** (dans un callout avec emoji)
   ```markdown
   > [!success] 🏆 Récompenses
   > **Quêtes accomplies:**
   > - **Action 1:** Conséquence `(effet mécanique)`
   > - **Action 2:** Conséquence `(effet mécanique)`
   ```

## V. Utilisation des Callouts et Emojis

### Types de Callouts
- **note**: 🏠 Pour les services, logements et informations générales
- **tip**: 🍺 Pour les consommations, 💰 pour les offres de travail
- **warning**: 🎲 Pour les tables d'événements aléatoires
- **success**: 🏆 Pour les récompenses et accomplissements
- **example**: ⏰ Pour les conditions temporelles (heures d'ouverture, événements programmés)

### Formatage des Prix et Valeurs
Utilisez le format code (\`texte\`) pour mettre en évidence:
- Les prix: `5 pièces d'or`
- Les statistiques: `3 PV`
- Les dégâts: `1d6`
- Les effets mécaniques: `(+1 PV)`

### Utilisation des Conditions Temporelles
> [!important] À utiliser avec parcimonie
> Les conditions temporelles doivent être utilisées uniquement lorsqu'elles sont importantes pour le gameplay ou l'histoire, et seulement pour les lieux où le moment de la journée/semaine modifie significativement l'expérience des joueurs. Évitez de les ajouter à chaque lieu pour ne pas alourdir vos fiches.

#### Types de Conditions Temporelles
1. **Heures d'ouverture standard**
   ```markdown
   > [!example] ⏰ Heures d'Ouverture
   > - **Ouvert:** 6h-23h tous les jours
   > - **Fermé:** Dimanche et jours de fête
   > 
   > _Si arrivée pendant fermeture:_ La porte est verrouillée
   ```

2. **Variations selon moment de la journée**
   ```markdown
   > [!example] ⏰ Conditions Temporelles
   > - **Matinée (6h-12h):** Clientèle calme, petit-déjeuner servi
   > - **Soirée (18h-23h):** Ambiance festive, barde présent
   > - **Nuit (23h-6h):** `FERMÉ`
   ```

3. **Événements programmés**
   ```markdown
   > [!example] ⏰ Événements Programmés
   > - **Mercredi soir:** Soirée musicale 
   > - **Premier du mois:** Réunion du conseil
   ```

4. **Conditions narratives**
   ```markdown
   > [!example] ⏰ Événements Narratifs
   > - **Avant l'annonce du couvre-feu:** Ouvert jusqu'à 23h
   > - **Après l'annonce:** Fermeture à 20h
   ```

## VI. Exemple Concret

### Village de Honeywood
> *Vous arrivez dans un petit village bucolique entouré de champs de blé doré et de ruches bourdonnantes. L'air est doux et parfumé de miel, tandis que les villageois s'affairent à leurs tâches quotidiennes. Au centre, vous apercevez une place animée où se dressent la mairie et une taverne accueillante.*

## Lieux d'Intérêt du Village
- [[#Place du Village]] : La mairie (Molaire), Taverne du Saoulôt (Garrik)
- [[#Périphérie]] : Maison du chasseur (Charles)

## Place du Village
> *Vous traversez la place centrale pavée où quelques villageois discutent près d'un puits en pierre. Des oiseaux picorent des miettes entre les pavés, tandis que l'enseigne de la taverne grince doucement sous la brise. Vous remarquez l'imposant bâtiment de la mairie qui se dresse sur un côté de la place.*

### Points d'intérêt de la Place
- [[#La Mairie]] : Molaire (maire)
- [[#La Taverne du Saoulôt]] : Garrik (tavernier)

### La Mairie
> *Vous entrez dans un bâtiment solide aux murs en pierre calcaire. Une grande table en chêne massif occupe le centre de la pièce principale, couverte de parchemins et de registres. Vous sentez l'odeur du bois ciré et de l'encre fraîche qui imprègne les lieux.*

➤ **Molaire (maire)** -- jovial, soigné. **Intentions:** maintenir l'ordre
- *Quête:* Trouver du gibier

> [!example] ⏰ Heures d'Ouverture
> - **Ouvert:** 8h-17h (jours de semaine)
> - **Fermé:** Week-end et jours de fête
> 
> _Si urgence pendant fermeture:_ Molaire peut être trouvé à la taverne ou à son domicile

_Si les joueurs mentionnent Philippo_: Le maire révèle des tensions dans le village

> [!note] 🏠 Services disponibles
> **Auberge** — Souper et couchage: `3 pièces d'argent`

### La Taverne du Saoulôt
> *Vous poussez la porte en bois de la taverne et êtes accueilli par la chaleur d'un feu de cheminée. Les rires et conversations emplissent la salle où des tables robustes accueillent les habitués. Vous humez l'arôme enivrant de la bière fraîche et du ragoût mijotant dans la marmite.*

➤ **Garrik (tavernier)** -- jovial, occupé
- *Information:* Rumeurs locales

> [!example] ⏰ Conditions Temporelles
> - **Matinée (6h-12h):** Calme, petit-déjeuner servi
> - **Après-midi (12h-18h):** Clientèle modérée
> - **Soirée (18h-23h):** Pleine animation, musique
> - **Nuit (23h-6h):** `FERMÉ` 
> 
> _Si arrivée après 23h:_ Porte verrouillée, lumière faible à l'étage (Garrik y dort)

> [!tip] 🍺 Consommations
> - **Bière ordinaire**: `7 pièces de cuivre`
> - **Hydromel**: `2 pièces d'argent`

### Maison du Chasseur
> *Vous approchez d'une cabane rustique à la lisière du village. Des peaux d'animaux sèchent sur des cadres en bois, et diverses armes de chasse sont accrochées près de l'entrée. Vous percevez l'odeur du cuir tanné et de la fumée de bois qui s'échappe de la cheminée.*

➤ **Charles (chasseur)** -- léger embonpoint, regard perçant
- *Quête:* Chasser du gibier pour le festin

> [!tip] 💰 Offre de travail
> - **Chasse au sanglier**: `3 pièces d'or par sanglier`

## VII. Conseils Supplémentaires
1. Gardez les descriptions concises mais évocatrices
2. Utilisez le format italique pour les événements déclencheurs
3. Maintenez une liste claire des PNJ avec leurs rôles
4. Incluez toujours les liens vers les différents lieux d'intérêt
5. Utilisez les callouts avec emojis pour mettre en évidence les informations commerciales
6. **N'utilisez les conditions temporelles que lorsqu'elles sont vraiment pertinentes** pour l'histoire ou le gameplay
7. **Après chaque description de quartier**, listez tous les points d'intérêt de ce quartier avec leurs PNJ avant de détailler chaque lieu
8. **Pour l'immersion**, toutes les descriptions doivent être à la deuxième personne et commencer par "Vous..." (ex: "Vous entrez...", "Vous apercevez...", "Vous sentez...")

- **Formatage:** Utiliser le formatage Markdown pour améliorer la lisibilité
- **Points clés:** Mettre en gras les informations essentielles
- **Concision:** Éviter les longues descriptions, privilégier l'efficacité
- **Organisation visuelle:** Utiliser les callouts, emojis, listes à puces, indentations et séparateurs
- **Préparation:** Anticiper les actions des joueurs avec des notes sur les réactions possibles des PNJ
- **Rencontres aléatoires:** Prévoir une variété d'événements (combats, énigmes, découvertes, PNJ)
- **Équilibre:** Inclure à la fois des rencontres faciles et difficiles pour maintenir l'intérêt
- **Différenciation visuelle:** Utiliser différents types de callouts et emojis pour distinguer rapidement les types d'information
- **Perspective immersive:** Utiliser systématiquement "Vous..." pour débuter les descriptions afin de plonger directement les joueurs dans l'action
- **Sobriété temporelle:** N'utiliser les conditions temporelles que pour les lieux où le moment de visite fait vraiment une différence

> [!tip] Astuce de MJ
> Laissez des espaces pour ajouter des notes pendant la session, comme des décisions importantes des joueurs ou des éléments improvisés à conserver. 