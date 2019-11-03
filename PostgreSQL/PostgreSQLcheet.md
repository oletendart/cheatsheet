*** Ouvrir PostgreSQL (dans le terminal) : ***
    sudo su postgres
*** puis *** 
    psql

*** Créer un nouvel utilisateur : ***
    CREATE USER nom_utilisateur;

*** Créer un nouvel utilisateur avec mot de passe : ***
    CREATE USER nom_utilisateur WITH PASSWORD 'mot_de_passe';

*** Supprimer un utilisateur existant : ***
    DROP USER nom_utilisateur;

*** Lister tous les utilisateurs existants : ***
    \du 

*** Attribuer/supprimer un rôle à un utilisateur : ***
    CREATE ROLE nom_utilisateur WITH NOM_DU_ROLE; (ajout)
    DROP ROLE nom_utilisateur WITH NOM_DU_ROLE; (suppression)

*** Création/Suppression d'un rôle groupe : ***
    CREATE ROLE nom; (ajout)
    DROP ROLE nom; (suppression)

*** Ajouter/Supprimer un membre dans un rôle groupe : ***
    GRANT role_groupe TO role1, ...; (ajouter)
    REVOKE role_groupe TO role1, ...; (supprimer)

*** Réinitialiser un rôle (n'importe lequel) : ***
    RESET ROLE;

*** Créer une base de données : ***
    CREATE DATABASE nom_base;
    (si aucune erreur ne s'affiche, cela veut dire qu'elle est créer)

*** Supprimer une base de données : ***
    DROP DATABASE nom_base;
    (toujours mettre le nom de la base !)

*** Lister les bases de données : ***
    \l

*** Lister les rôles existants : ***
    \d

*** Quitter PostgreSQL : ***
    quit 
*** ou ***
    exit
*** ou ***
    \q

*** Commentaires dans PostgreSQL : ***
    -- suivi_du_commantaire;

*** Terminer une action : ***
Avec un point virgule à la fin de l'action.

*** Appeler les rôles depuis le terminal : ***
    createuser nom_utilisateur; (créer)
    dropuser nom_utilisateur; (Supprimer)


