# Démo d'intégration continue avec AWS

## Configuration du dépôt GitHub

La première étape de notre parcours CI consiste à configurer un dépôt GitHub pour stocker le code source de notre application Python. Si vous avez déjà un dépôt, n'hésitez pas à passer cette étape. Sinon, créons un nouveau dépôt sur GitHub en suivant ces étapes :

- Rendez-vous sur github.com et connectez-vous à votre compte.
- Cliquez sur le bouton "+" en haut à droite et sélectionnez "Nouveau dépôt".
- Donnez un nom à votre dépôt et ajoutez une description facultative.
- Choisissez l'option de visibilité appropriée en fonction de vos besoins.
- Initialisez le dépôt avec un fichier README.
- Cliquez sur le bouton "Créer un dépôt" pour créer votre nouveau dépôt GitHub.

Super ! Maintenant que notre dépôt est configuré, passons à l'étape suivante.

## Création d'un AWS CodePipeline

À cette étape, nous allons créer un AWS CodePipeline pour automatiser le processus d'intégration continue pour notre application Python. AWS CodePipeline orchestrera le flux des modifications depuis notre dépôt GitHub jusqu'au déploiement de notre application. Suivez ces étapes :

- Rendez-vous sur la console de gestion AWS et accédez au service AWS CodePipeline.
- Cliquez sur le bouton "Créer un pipeline".
- Donnez un nom à votre pipeline et cliquez sur le bouton "Suivant".
- Pour l'étape source, sélectionnez "GitHub" comme fournisseur source.
- Connectez votre compte GitHub à AWS CodePipeline et sélectionnez votre dépôt.
- Choisissez la branche que vous souhaitez utiliser pour votre pipeline.
- À l'étape de construction, sélectionnez "AWS CodeBuild" comme fournisseur de construction.
- Créez un nouveau projet CodeBuild en cliquant sur le bouton "Créer un projet".
- Configurez le projet CodeBuild avec les paramètres nécessaires pour votre application Python, tels que l'environnement de construction, les commandes de construction et les artefacts.
- Enregistrez le projet CodeBuild et retournez à CodePipeline.
- Continuez à configurer les étapes du pipeline, comme le déploiement de votre application à l'aide d'AWS Elastic Beanstalk ou toute autre option de déploiement appropriée.
- Vérifiez la configuration du pipeline et cliquez sur le bouton "Créer un pipeline" pour créer votre AWS CodePipeline.

Super travail ! Notre pipeline est maintenant prêt à fonctionner. Passons à l'étape suivante pour configurer AWS CodeBuild.

## Configuration d'AWS CodeBuild

À cette étape, nous allons configurer AWS CodeBuild pour construire notre application Python en fonction des spécifications que nous définissons. CodeBuild se chargera de la construction et de l'emballage de notre application en vue du déploiement. Suivez ces étapes :

- Dans la console de gestion AWS, accédez au service AWS CodeBuild.
- Cliquez sur le bouton "Créer un projet de construction".
- Donnez un nom à votre projet de construction.
- Pour le fournisseur source, choisissez "AWS CodePipeline".
- Sélectionnez le pipeline que vous avez créé à l'étape précédente.
- Configurez l'environnement de construction, tel que le système d'exploitation, le runtime et les ressources de calcul nécessaires pour votre application Python.
- Spécifiez les commandes de construction, telles que l'installation des dépendances et l'exécution des tests. Personnalisez cela en fonction des besoins de votre application.
- Configurez la configuration des artefacts pour générer les sorties de construction nécessaires au déploiement.
- Vérifiez les paramètres du projet de construction et cliquez sur le bouton "Créer un projet de construction" pour créer votre projet AWS CodeBuild.

Fantastique ! Avec AWS CodeBuild correctement configuré, nous sommes maintenant prêts à voir la magie de l'intégration continue en action.

## Déclencher le processus d'intégration continue

À cette dernière étape, nous allons déclencher le processus d'intégration continue en apportant une modification à notre dépôt GitHub. Voyons comment cela fonctionne :

- Rendez-vous sur votre dépôt GitHub et apportez une modification au code source de votre application Python. Il peut s'agir d'une correction de bogue, d'une nouvelle fonctionnalité ou de tout autre changement que vous souhaitez apporter.
- Validez et poussez vos modifications vers la branche configurée dans votre AWS CodePipeline.
- Rendez-vous sur la console AWS CodePipeline et accédez à votre pipeline.
- Vous devriez voir le pipeline démarrer automatiquement dès qu'il détecte les modifications dans votre dépôt.
- Détendez-vous pendant qu'AWS CodePipeline s'occupe du reste. Il récupérera le code le plus récent, déclenchera le processus de construction avec AWS CodeBuild et déploiera l'application si vous avez configuré l'étape de déploiement.

Bravo ! Vous venez d'effectuer une intégration continue avec succès à l'aide des services AWS.
