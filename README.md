Automatisation — GitHub Actions
Pour recevoir le dashboard par mail chaque matin à 9h31 sans intervention manuelle, suivez ces étapes.
1. Créer un compte GitHub sur https://github.com et créer un nouveau repository public nommé morning-market-dashboard.
2. Uploader le notebook morning_market_dashboard_email.ipynb dans le repository via "uploading an existing file".
3. Configurer les secrets dans Settings → Secrets and variables → Actions → New repository secret :
Nom du secretValeurFRED_API_KEYVotre clé FRED (https://fredaccount.stlouisfed.org)EMAIL_SENDERVotre adresse GmailEMAIL_PASSWORDVotre Gmail App Password (https://myaccount.google.com/apppasswords)EMAIL_TOL'adresse qui reçoit le rapport
4. Créer le fichier workflow en cliquant sur "Add file" → "Create new file", nommez-le .github/workflows/morning_dashboard.yml et collez ce contenu :A exécuté une commande, lu un fichierA exécuté une commande, lu un fichier5. Tester manuellement dans l'onglet Actions → Morning Market Dashboard → Run workflow.
