# module d'authenfication

- ui : box avec user et pwd
    + [x] options labels
    + [x] logo (image)
    + [x] css / couleur / theme

- server: 
    + [x] entrée : colonne user / pwd / admin obligatoire
    + [x] entrée : colonne date début / date fin. Si renseigné, vérification, sinon message appropriée "Vous n'êtes plus habilité"
    + [x] entrée optionnelle : fonction d'authentification
    + [ ] Q : branchment sqlite
    + [x] sortie : T/F + liste de toutes les colonnes présentes dans les données hors pwd
    
sqlite : propose en hashage du pwd (openssl, ou autre). Voir pour l'initialisation
--> cryptage de la base entière sous forme de blob

# interface admin (autre module) : uniquement sqlite

- visualisation du tableau
    + [ ] modifier des données utilisateur (un à la fois)
    + [ ] demander de changer le pwd a la prochaine connexion -> stockage base externe sqlite
    + [ ] suppression de compte
    + [ ] création un à la fois via l'interface. Création multiple via fonction externe.
    
- dashboard de connexion
    + [ ] stockage des événements simples en sqlite
    + [ ] une ligne par connection : user, app, date_heure_connexion, date_heure_deconnexion
    + [ ] télécharger de la base / visualisation avec filter user et date
