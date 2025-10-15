<div align="center">

<center>
<h1 style="font-size:18pt;">
Labo 05 – Microservices, SOA, SBA, API Gateway, Rate Limit & Timeout
</h1>
</center>

<br>
<br>
<br>
<br>

<center>
<h2 style="font-size:16pt;">
PAR
</h2>
</center>

<br>
<br>

<center>
<h2 style="font-size:16pt;">
Marc CHARLEBOIS, CHAM65260301
</h2>
</center>

<br>
<br>
<br>
<br>
<br>
<br>

<center>
<h3 style="font-size:14pt;">
RAPPORT DE LABORATOIRE PRÉSENTÉ À MONSIEUR FABIO PETRILLO DANS LE CADRE DU COURS <em>ARCHITECTURE LOGICIELLE</em> (LOG430-01)
</h3>
</center>

<br>
<br>
<br>
<br>
<br>

<center>
<h3 style="font-size:14pt;">
MONTRÉAL, LE 28 OCTOBRE 2025
</h3>
</center>

<br>
<br>
<br>
<br>
<br>

<center>
<h3 style="font-size:14pt;">
ÉCOLE DE TECHNOLOGIE SUPÉRIEURE<br>
UNIVERSITÉ DU QUÉBEC
</h3>
</center>

<br>
<br>
<br>
<br>
<br>

</div>

---
## **Tables des matières**
- [**Tables des matières**](#tables-des-matières)
  - [**Question 1**](#question-1)
  - [**Question 2**](#question-2)
  - [**Question 3**](#question-3)
  - [**Question 4**](#question-4)
  - [**Question 5**](#question-5)
  - [**Question 5**](#question-5-1)
  - [**CI/CD**](#cicd)

<br>

---

<div align="justify">

### **Question 1**

> Quelle réponse obtenons-nous à la requête à `POST /payments` ? Illustrez votre réponse avec des captures d'écran/terminal.



### **Question 2**

> Quel type d'information envoyons-nous dans la requête à `POST payments/process/:id` ? Est-ce que ce serait le même format si on communiquait avec un service SOA, par exemple ? Illustrez votre réponse avec des exemples et captures d'écran/terminal.



### **Question 3**

> Quel résultat obtenons-nous de la requête à `POST payments/process/:id`?



### **Question 4**

> Quelle méthode avez-vous dû modifier dans `log430-a25-labo05-payment` et qu'avez-vous modifié ? Justifiez avec un extrait de code.



### **Question 5**

> À partir de combien de requêtes par minute observez-vous les erreurs 503 ? Justifiez avec des captures d'écran de Locust.


### **Question 5**

> Que se passe-t-il dans le navigateur quand vous faites une requête avec un délai supérieur au timeout configuré (5 secondes) ? Quelle est l'importance du timeout dans une architecture de microservices ? Justifiez votre réponse avec des exemples pratiques.


### **CI/CD**

Mon pipeline CI/CD fonctionne ainsi : lors de chaque push ou pull request, mon script CI s’exécute sur GitHub Actions, lance un environnement avec MySQL et Redis, installe les dépendances et exécute les tests pour valider mon code. Si tout est correct, mon script CD se déclenche automatiquement via un runner self-hosted installé sur ma VM, qui récupère le dépôt, génère le fichier .env, construit et démarre les conteneurs avec Docker Compose, puis affiche l’état et les logs pour confirmer le déploiement.

On peut voir ci-dessous que les deux workflows se sont exécutés correctement, ce qui confirme que l’application a été testée puis déployée sans erreur.



Le déploiement s’effectue sur mon runner auto-hébergé configuré sur la VM, qui exécute directement les commandes Docker.


La commande `docker ps` montre que les conteneurs sont bien lancés sur la VM et que l’application est en fonctionnement.
