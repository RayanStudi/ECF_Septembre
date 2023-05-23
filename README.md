# Le Quai Antique - Site Web

## Prérequis

Pour exécuter ce projet en local, vous aurez besoin des logiciels suivants :

- PHP 8.1 avec l'extension PDO
- Symfony 5.4
- MariaDB 10.6
- XAMPP

Vous aurez également besoin d'un navigateur moderne pour afficher le site web.

## Création d'un compte administrateur

Pour créer un compte administrateur, vous devez suivre les étapes suivantes :

1. Inscrivez-vous sur le site en tant que nouvel utilisateur.
2. Ouvrez la ligne de commande MariaDB et naviguez jusqu'à la base de données du projet.
3. Localisez l'utilisateur que vous venez de créer et modifiez le champ `roles` pour y inclure `'ROLE_ADMIN'`. Pour ce faire, vous pouvez utiliser une commande SQL similaire à la suivante :
```sql
UPDATE user SET roles = '["ROLE_USER", "ROLE_ADMIN"]' WHERE email = 'votre_email@example.com';

