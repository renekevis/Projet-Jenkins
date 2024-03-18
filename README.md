Ce script Jenkinsfile définit un pipeline Jenkins pour un processus de construction, de test et de déploiement d'une application Java à l'aide de Maven. Voici un résumé des principales étapes :

1 - Configuration des outils : Les outils Maven et JDK sont configurés pour être utilisés dans le pipeline.

2 - Étapes du pipeline :

'Fetch code': Récupération du code source à partir d'un référentiel Git.
'Build': Compilation et emballage de l'application à l'aide de Maven. Le résultat est archivé en tant qu'artefact.
'Test': Exécution des tests unitaires de l'application.
'Checkstyle Analysis': Analyse du code source avec Checkstyle pour détecter les violations des règles de codage.
'Sonar Analysis': Analyse statique du code avec SonarQube pour évaluer la qualité du code.
'Quality Gate': Attente du passage de la porte de qualité définie dans SonarQube.
'UploadArtifact': Publication de l'artefact résultant dans un référentiel Nexus.

3 - Post-actions : Envoi de notifications Slack pour informer sur le résultat du pipeline, avec une couleur différente selon le statut de la construction (SUCCESS ou FAILURE).
