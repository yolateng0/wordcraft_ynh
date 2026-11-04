## Contrôle d'accès (SSO / LDAP)

WordCraft n'a pas de comptes utilisateurs propres. L'accès est contrôlé par le portail SSO de YunoHost (SSOWAT), qui s'appuie sur l'annuaire LDAP du serveur. L'utilisateur se connecte une fois sur le portail, puis ouvre WordCraft sans second identifiant.

La permission s'appelle `wordcraft.main` (ou `wordcraft__2.main` pour une seconde instance).

Restreindre l'app à un groupe :

```
yunohost user group create redacteurs
yunohost user group add redacteurs alice
yunohost user permission update wordcraft.main --remove all_users --add redacteurs
```

La rendre publique, ou la remettre à tous les utilisateurs :

```
yunohost user permission update wordcraft.main --add visitors
yunohost user permission update wordcraft.main --remove visitors --add all_users
```

Les mêmes réglages existent dans l'interface d'administration, sous **Utilisateurs > Groupes et permissions**.

## Données

Les documents sont ouverts et enregistrés dans le navigateur de l'utilisateur. Rien n'est stocké sur le serveur : il n'y a donc aucune donnée à sauvegarder.
