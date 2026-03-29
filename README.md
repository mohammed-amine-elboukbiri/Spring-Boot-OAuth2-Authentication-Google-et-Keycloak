# 🔐 Spring Boot OAuth2 & OpenID Connect Authentication

> Implémentation d'une authentification sécurisée avec OAuth2 et OpenID Connect dans une application Spring Boot, intégrant des fournisseurs d'identité externes (Google, Keycloak).

---

## 🎯 Aperçu du projet

Ce projet démontre comment sécuriser une application **Spring Boot** de manière moderne en déléguant l'authentification à un fournisseur d'identité externe via le protocole **OAuth2** et **OpenID Connect (OIDC)**.

L'application agit en tant que **client OAuth2** et permet aux utilisateurs de se connecter via :
- 🌐 **Google** (fournisseur cloud)
- 🔑 **Keycloak** (serveur d'identité local)

Les informations du profil utilisateur (nom, email, photo) sont extraites depuis le **ID Token (JWT)** et affichées dans une interface web **Thymeleaf**.

---

### Configuration Google Cloud Console

1. Accéder à [console.cloud.google.com](https://console.cloud.google.com)
2. Créer un projet → **APIs & Services** → **Credentials**
3. Créer un **OAuth 2.0 Client ID** de type **Web application**
4. Ajouter l'URI de redirection : `http://localhost:8080/login/oauth2/code/google`

---

### Endpoints disponibles

| Endpoint | Accès | Description |
|----------|-------|-------------|
| `/` | Public | Page d'accueil |
| `/login` | Public | Page de connexion OAuth2 |
| `/profile` | Protégé | Profil utilisateur (nom, email, photo) |
| `/logout` | Authentifié | Déconnexion |

---

## 🎬 Démonstration vidéo



https://github.com/user-attachments/assets/704a0d6a-8844-4951-9260-dac19bb59d9b


---

---

## 📄 Licence

Ce projet est sous licence **MIT** — voir le fichier [LICENSE](LICENSE) pour plus de détails.
