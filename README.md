# Projet-fin-d-ann-e
Voici notre projet 
1.Structure du site
Page d’accueil – index.php
Page principale du site :
Formulaire d’inscription avec les champs :
Nom
Prénom
Email
Mot de passe
Ville
Email
Code postal
Le formulaire envoie les données vers traitement.php pour enregistrement.
---
2.Page de contact – contact.php
Permet aux visiteurs d’envoyer un message à l’artiste.
Champs du formulaire :
Sujet
Message
Questionnaire
Les données sont enregistrées dans la base via PHP.
---
3.Traitement – traitement.php
Script PHP qui gère l’enregistrement des données envoyées depuis les formulaires.
Fonctionnalités :
Récupération des données via $_POST
Vérification des champs
Connexion à MySQL
Insertion des données dans les tables (utilisateurs)
Protection possible contre les injections SQL avec des requêtes préparées
---
4.Modification et suppression – modife.php et supprime.php
#### modife.php – Modification des données utilisateur
Permet aux utilisateurs de modifier leurs informations.
Fonctionnement :
Récupère les informations de l’utilisateur (via son ID ou son email).
Affiche un formulaire pré-rempli avec les anciennes données.
L’utilisateur peut modifier :
Nom
Prénom
Email
Ville
Code postal
Une fois le formulaire soumis, les nouvelles informations sont mises à jour dans la base de
données MySQL via une requête UPDATE.
supprime.php – Suppression des données utilisateur
La page supprime.php permet à l'utilisateur de supprimer définitivement ses informations
du site. Cela peut être nécessaire si un utilisateur ne souhaite plus faire partie de la base
de données ou a décidé de se retirer de l'interaction avec l'artiste.
Fonctionnement :
L'utilisateur fournit son ID ou son email via un formulaire ou une URL pour identifier son
compte.
Une fois l'utilisateur identifié, une requête DELETE est exécutée dans la base de données
pour supprimer toutes les informations associées à ce compte.
Un message de confirmation est affiché, ou bien l'utilisateur est redirigé vers une autre
page pour confirmer la suppression ou revenir à la page d'accueil. DELETE FROM clients
WHERE id = ?x;
---
5.Tableau des projets – tableau.php
La page tableau.php permet à l'artiste de mettre en avant ses projets réalisés, tout en
offrant une vue d'ensemble des œuvres et accompagnées de leurs tarifs associés. C'est un
espace où les visiteurs peuvent découvrir le travail de l'artiste de manière plus visuelle et
détaillée.
Fonctionnement :
Présentation des projets : Chaque projet est illustré par une photo de l'œuvre.
Tarification claire : Pour chaque projet, un tarif est affiché afin de donner aux visiteurs une
idée précise des coûts liés aux créations de l'artiste.
Photos des projets : Les photos des œuvres sont présentées sous forme d'images (.jpg) . En
cliquant dessus, les visiteurs peuvent voir les images en haute résolution, offrant ainsi une
expérience immersive grâce à une lightbox.
