# fillRouge
Nom du Projet : "EcoLife - Application de Suivi Écologique" Description détaillée :

Fonctionnalités clés:
Inscription et Profils Utilisateurs : 

Les utilisateurs s'inscrivent en fournissant des informations telles que leur nom, adresse e-mail et emplacement géographique. Ils détaillent également leurs habitudes de vie actuelles, leurs objectifs de durabilité, et leurs préférences environnementales. Les profils utilisateurs comprennent des sections dédiées aux habitudes quotidiennes, aux réalisations écologiques, aux défis en cours, et aux projets de durabilité personnels. 

Suivi d'Actions Écologiques :

Les utilisateurs enregistrent leurs actions écologiques quotidiennes à l'aide d'une interface intuitive. Cela peut inclure des actions telles que le recyclage, la consommation de produits locaux, et la réduction de la consommation d'énergie. Chaque action enregistrée génère automatiquement des points écologiques, et des notifications sont envoyées pour féliciter l'utilisateur et lui donner des suggestions pour des actions similaires. 

Tableau de Bord Écologique : 

Un tableau de bord interactif permet aux utilisateurs de visualiser l'impact cumulé de leurs actions écologiques au fil du temps. Des graphiques et des statistiques présentent des informations sur la réduction des émissions de carbone, la préservation des ressources, et d'autres mesures de durabilité. Des notifications régulières informent les utilisateurs des nouveaux graphiques ajoutés au tableau de bord, des jalons atteints, et des conseils pour maximiser leur impact écologique. 

Communauté Écologique : 

Une section communautaire encourage les utilisateurs à partager leurs succès, à proposer des défis écologiques, et à collaborer sur des projets de durabilité. Des notifications sont générées pour les nouveaux défis proposés, les discussions populaires au sein de la communauté, et les événements écologiques locaux. 

Notifications Personnalisées :

Le système de notification envoie des messages personnalisés en fonction du profil de chaque utilisateur. Par exemple, un utilisateur engagé dans la réduction des déchets pourrait recevoir des suggestions spécifiques à ce domaine. Les notifications sont également utilisées pour rappeler aux utilisateurs des défis en cours, des événements locaux à venir, et des opportunités de collaboration. 

Technologies : 

Backend : Java avec Spring (Spring Boot), Spring Security, WebSocket pour les notifications en temps réel. 
Frontend : Angular avec une interface utilisateur réactive et des graphiques interactifs pour le suivi des actions écologiques. 
Base de Données : PostgreSQL pour stocker les informations sur les utilisateurs, leurs actions écologiques et les discussions de la communauté.


les classes sont:
1. Classe Utilisateur :
    - Attributs :
      - idUtilisateur : int
      - nom : String - email : String
      - localisation : String
      - pointsEcologiques : int
      - objectifsDurabilite : List<String>
    - Méthodes :
      - enregistrerActionEcologique(action : ActionEcologique) : void
      - rejoindreDefiEcologique(defi : DefiEcologique) : void
      - ajouterProjet(personnel : ProjetEcologique) : void
2. Classe ActionEcologique :
    - Attributs :
      - idAction : int
      - typeAction : String
      - pointsGagnes : int
   - Méthodes :
     - getDescription() : String
3. Classe TableauDeBord :
   - Attributs :
     - actionsEnregistrees : List<ActionEcologique>
     - statistiques : Statistiques
   - Méthodes :
     - ajouterAction(action : ActionEcologique) : void
     - genererStatistiques() : void
4. Classe DefiEcologique :
   - Attributs :
     - idDefi : int
     - description : String
     - participants : List<Utilisateur>
   - Méthodes :
     - ajouterParticipant(utilisateur : Utilisateur) : void
     - notifierParticipants(message : String) : void
5. Classe ProjetEcologique :
   - Attributs :
     - idProjet : int
     - description : String
     - participants : List<Utilisateur>
   - Méthodes :
     - ajouterParticipant(utilisateur : Utilisateur) : void
     - partagerProgression() : void
 6. Classe Statistiques :
    - Attributs :
      - emissionCarboneReduite : double
      - ressourcesPreservees : double
    - Méthodes :
      - calculerEmissionCarboneReduite() : double
      - calculerRessourcesPreservees() : double
