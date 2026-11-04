WordCraft is an open-source word processor written in Rust, with a Word-like interface (ribbon, styles, tables, track changes). It reads and writes .docx files and runs directly in the browser thanks to WebAssembly.

Documents are opened and saved from the browser: the server only serves the application. Access is protected by the YunoHost SSO portal, so only your YunoHost users (LDAP directory) can open it by default.
