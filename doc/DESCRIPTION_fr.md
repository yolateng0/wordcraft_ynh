WordCraft est un traitement de texte open source écrit en Rust, avec une interface proche de Word (ruban, styles, tableaux, suivi des modifications). Il lit et écrit les fichiers .docx et tourne directement dans le navigateur grâce à WebAssembly.

Les documents sont ouverts et enregistrés depuis le navigateur : le serveur ne fait que servir l'application. L'accès est protégé par le portail SSO de YunoHost : par défaut, seuls vos utilisateurs YunoHost (annuaire LDAP) peuvent l'ouvrir.
