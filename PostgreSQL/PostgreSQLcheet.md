*** Ouvrir PostgreSQL (dans le terminal) : ***
    sudo su postgres
*** puis *** 
    psql

*** Connection à PGCLI et PSQL : ***
 psql -U nom_utilisateur
 pgcli -u nom_utilisateur 

*** Créer un nouvel utilisateur : ***
    CREATE USER nom_utilisateur;

*** Créer un nouvel utilisateur avec mot de passe : ***
    CREATE USER nom_utilisateur WITH PASSWORD 'mot_de_passe';

*** Créer un nouvel utilisateur avec mot de passe et ROLE ***
    CREATE USER nom_utilisateur WITH NOM_ROLE(en majuscule) PASSWORD 'mot_de_passe';

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

*** Lier une base de données à un utilisateur : ***
    ALTER DATABASE nom_utilisateur OWNER TO nom_base_données;

*** Créer une base de données : ***
    CREATE DATABASE nom_base;
    (si aucune erreur ne s'affiche, cela veut dire qu'elle est créer)

*** Supprimer une base de données : ***
    DROP DATABASE nom_base;
    (toujours mettre le nom de la base !)

*** Créer une table : ***
    CREATE TABLE nom_table ([f3 via pgcli ou simplement entrer pour postgresql(mode multiligne)]
    id bigserial not null primary key, (première colonne)
    item varchar(200) [nombre de caractère maxi]
    );

*** Insérer une valeur dans une base de données : ***
    INSERT INTO nom_table(nom_colonne) VALUES('valeur');

*** Supprimer (toutes) les valeurs des lignes dans une base de données : ***
    DELETE FROM nom_base_donnees; (les supprime visuellement mais les id continue (ex : si on supprime la ligne 1 correspond à l'id 1, si on la supprime et qu'on entre d'autres valeurs, elles commenceront à 2))

*** Insérer une colonne dans une table déjà existante ***
    ALTER TABLE nom_table [f3 pour pgcli ou entrée]
    ADD COLUMN  "nom_colonne" TIMESTAMP;

*** Voir toutes les colonnes/lignes d'une base de données : ***
    SELECT * FROM nom_tableau;

*** Lister les bases de données : ***
    \l

*** Lister les rôles existants : ***
    \d

*** Se connecter à une base de données : ***
    \c base_donnees_nom;

*** Aide PostgreSQL : ***
    \?

*** Informations : ***
    \conninfo

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
    

D'abord créer un utilisateur puis une base de données et ensuite lier les deux. Supprimer d'abord la base de données avant l'utilisateur. 

Si user non authentifier : 
 => sudo vim /etc/postgresql/11/main/pg_hba.conf
puis modifier les "peer" en "md5"
puis redémarrer postgresql :
=> sudo service postgresql restart


