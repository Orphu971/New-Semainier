# Semainier

Ma semaine sur un seul écran : sept jours colorés, trois moments par jour (matin, après-midi, soir), les tâches rangées par catégorie, et un bouton qui les répartit toutes seules dans les moments libres.

## Ce que fait l'appli

**La semaine**
- Chaque jour a sa couleur ; le jour en cours est encadré et sa ligne est teintée.
- Les cours de l'emploi du temps fixe (semaines A et B) apparaissent en gris hachuré.
- Chaque tâche affiche son nom en gros, son heure dans une étiquette noire et son annotation en italique.
- Un appui sur une tâche ouvre sa fiche. Un appui long puis un glissement la déplacent dans une autre case.
- Un appui sur la pastille du jour ouvre la journée entière, avec les annotations complètes.
- Les jours fériés et les vacances scolaires de La Réunion sont signalés en bandeau.

**Les tâches**
- Six catégories : activité professionnelle, maison, activités et loisirs, administratif, santé, rites et habitudes.
- Les rites et habitudes se posent en petits onglets dans une bande en haut du jour, au-dessus du matin.
- Dans une fiche : heure, échéance, annotation, priorité (étoile), rappel à l'heure, sous-tâches à cocher, documents en appui.
- Boutons rapides : reporter à demain, semaine prochaine, dupliquer, en faire une répétition.

**Les répétitions**
- Une tâche qui revient d'elle-même aux jours choisis, et selon les semaines A, B ou les deux.
- Chaque occurrence se coche séparément. On peut sauter un jour, ou détacher une occurrence pour ne modifier que ce jour-là.

**Les documents**
- Une bibliothèque, dans la bande « Documents » de l'onglet Tâches : des fichiers ou des liens.
- Un document peut être joint à une tâche ou à une répétition ; la tâche porte alors un trombone dans la grille.

**Répartir**
- Propose un moment pour chaque tâche en attente : les prioritaires d'abord, jamais sur une demi-journée de cours, deux tâches au plus par moment, en respectant l'heure et l'échéance notées.
- On peut changer un moment, demander une autre répartition, ou tout accepter.

**Le menu**
- Mes cours et semaines A / B, mes répétitions, bilan de la semaine, semaine type (enregistrer une semaine et la reposer ailleurs), impression A4, apparence claire ou sombre, sauvegarde.

## Mettre en ligne avec GitHub Pages

1. Sur GitHub, créer un dépôt public, par exemple `semainier`.
2. « Add file » → « Upload files » : déposer **le contenu** de ce dossier (`index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `README.md`), puis « Commit changes ».
3. « Settings » → « Pages » → Source : « Deploy from a branch », branche `main`, dossier `/ (root)` → « Save ».
4. Après une à deux minutes, l'appli est à l'adresse `https://VOTRE-NOM.github.io/semainier/`.

## Installer sur le téléphone

- Android (Chrome) : ouvrir l'adresse, menu ⋮ → « Ajouter à l'écran d'accueil ».
- iPhone / iPad (Safari) : bouton Partager → « Sur l'écran d'accueil ».

L'appli fonctionne ensuite sans connexion.

## Vos données

Tout est enregistré **sur cet appareil**, dans le navigateur : rien ne part sur un serveur, et rien ne passe d'un appareil à l'autre.

- Menu → « Sauvegarde et restauration » écrit un fichier `.json` contenant les tâches, les cours, les répétitions et les réglages. C'est ce fichier qui sert à transférer le semainier sur un autre appareil, ou à le remettre après un changement de téléphone.
- **Les documents** : les fichiers ajoutés sont rangés dans la réserve du navigateur (tous formats, jusqu'à 50 Mo par fichier). La sauvegarde `.json` contient leur **nom**, mais **pas le fichier lui-même**. Après une restauration sur un autre appareil, ces documents apparaissent comme indisponibles ; les documents ajoutés sous forme de **lien**, eux, restent valables partout.
- Vider les données du navigateur efface le semainier : faites une sauvegarde de temps en temps.

## Les rappels

Le rappel d'une tâche s'appuie sur les notifications du navigateur. Il faut les autoriser à la première demande, et l'appli doit être ouverte ou en arrière-plan récent. Téléphone en veille depuis longtemps, le rappel peut ne pas arriver : ce n'est pas un réveil.

## Le calendrier

Les jours fériés se calculent chaque année, Pâques compris, avec le 20 décembre propre à La Réunion. Les vacances scolaires couvrent l'année 2026-2027 ; pour les années suivantes, modifier la liste `VAC` au début du script dans `index.html`.

## Mettre à jour

Remplacer les fichiers dans le dépôt et changer le numéro dans `sw.js` (`semainier-v7` → `semainier-v8`) pour que les téléphones prennent la nouvelle version.
