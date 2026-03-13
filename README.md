TP1 – Microservice avec docker

Dans ce tp, le but est de créer un microservice simple avec python et flask, puis de le lancer dans un conteneur docker

Le microservice expose une petite api qui renvoie un message quand on accède à la route

Structure du projet
-app.py
-Dockerfile
-requirements.txt
-README.md

app.py : code du microservice flask

Dockerfile : permet de construire l image docker

requirements.txt : dépendances python

Lancer le projet

Construire l’image docker :
docker build -t microservice .

Lancer le conteneur :
docker run -p 5000:5000 microservice

Tester l api

Dans un terminal :
curl http://localhost:5000

Réponse attendue :
{
"message": "Hello from Dockerized Microservice!"
}

Docker permet de lancer l application dans un environnement isolé avec toutes ses dépendances
Cela évite les problèmes d installation sur différentes machines
