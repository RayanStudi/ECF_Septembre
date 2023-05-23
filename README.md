# Le Quai Antique - Site Web

## Prérequis

Pour exécuter ce projet en local, vous aurez besoin des logiciels suivants :

- PHP 8.1 avec l'extension PDO
- Symfony 5.4
- MariaDB 10.6
- XAMPP

Vous aurez également besoin d'un navigateur moderne pour afficher le site web.

## Installation

1. **Cloner le dépôt** : Commencez par cloner le dépôt sur votre machine locale en utilisant la commande `git clone`.

2. **Installer XAMPP** : Si ce n'est pas déjà fait, installez XAMPP sur votre ordinateur.

3. **Démarrer les services Apache et MariaDB** : Ouvrez le panneau de contrôle XAMPP et démarrez les services Apache et MariaDB.

4. **Configurer la base de données** : Ouvrez la ligne de commande MariaDB et créez une nouvelle base de données pour le projet en utilisant la commande `CREATE DATABASE nom_de_la_base;`. Ensuite, utilisez la commande `SOURCE chemin_vers_le_fichier_sql;` pour importer le fichier SQL fourni dans le dépôt.

5. **Configurer Symfony** : Naviguez dans le répertoire du projet cloné en ligne de commande et exécutez `composer install` pour installer les dépendances Symfony. Configurez ensuite le fichier `.env` pour qu'il pointe vers la base de données que vous venez de créer.

6. **Lancer le serveur de développement Symfony** : Toujours dans le répertoire du projet, exécutez `symfony server:start` pour démarrer le serveur de développement Symfony.

7. **Ouvrir le site dans le navigateur** : Ouvrez votre navigateur et accédez à l'adresse `http://localhost:8000` (ou l'adresse que vous indique Symfony) pour voir le site.

## Création d'un compte administrateur

Pour créer un compte administrateur, vous devez suivre les étapes suivantes :

1. Inscrivez-vous sur le site en tant que nouvel utilisateur.
2. Ouvrez la ligne de commande MariaDB et naviguez jusqu'à la base de données du projet.
3. Localisez l'utilisateur que vous venez de créer et modifiez le champ `roles` pour y inclure `'ROLE_ADMIN'`. Pour ce faire, vous pouvez utiliser une commande SQL similaire à la suivante :
```sql
UPDATE user SET roles = '["ROLE_USER", "ROLE_ADMIN"]' WHERE email = 'votre_email@example.com';

