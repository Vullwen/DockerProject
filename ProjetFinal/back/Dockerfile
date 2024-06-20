# Image flask
FROM python:3.8

# On travail la dedans
WORKDIR /app

# Copie les dépendances dans le conteneur
COPY requirements.txt .

# Les installe
RUN pip install --no-cache-dir -r requirements.txt

# Copie tout le code de l'application dans le conteneur
COPY app.py ./app/app.py

# Expose le port 5000
EXPOSE 5000

# Définit la commande pour démarrer l'application Flask
CMD ["python", "app/app.py"]

