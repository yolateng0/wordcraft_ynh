## Access control (SSO / LDAP)

WordCraft has no user accounts of its own. Access is controlled by the YunoHost SSO portal (SSOWAT), which relies on the LDAP directory of your server. Users log in once on the portal and then open WordCraft without a second login.

The permission is called `wordcraft.main` (or `wordcraft__2.main` for a second instance).

Restrict the app to a group:

```
yunohost user group create redacteurs
yunohost user group add redacteurs alice
yunohost user permission update wordcraft.main --remove all_users --add redacteurs
```

Make it public or back to all users:

```
yunohost user permission update wordcraft.main --add visitors
yunohost user permission update wordcraft.main --remove visitors --add all_users
```

The same settings are available in the admin interface under **Users > Groups and permissions**.

## Data

Documents are opened and saved in the user's browser. Nothing is stored on the server, so there is no data to back up.
