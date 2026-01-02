# Email Notifications Setup

Pour que les notifications par email fonctionnent, vous devez configurer les variables d'environnement suivantes dans votre fichier `.env` du backend:

```env
# Email Configuration
EMAIL_SERVICE=gmail
EMAIL_USER=your-email@gmail.com
EMAIL_PASSWORD=your-app-password
```

## Configuration Gmail

1. **Activer l'authentification 2FA** sur votre compte Gmail
2. **Générer un mot de passe d'application**:
   - Aller à https://myaccount.google.com/apppasswords
   - Sélectionner "Mail" et "Windows Computer" (ou autre appareil)
   - Google génèrera un mot de passe de 16 caractères
   - Utiliser ce mot de passe dans `EMAIL_PASSWORD`

## Installer nodemailer

```bash
cd backend
npm install nodemailer
```

## Services email supportés

Vous pouvez utiliser n'importe quel service SMTP (Gmail, SendGrid, Mailgun, etc.)

## Fonctionnalités

- ✅ Email de bienvenue lors de l'inscription
- ✅ Notification d'email lors de chaque changement de statut d'application
  - Applied
  - In Review
  - Rejected
  - Accepted
