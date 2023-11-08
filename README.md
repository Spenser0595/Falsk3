# My test project
Voici un exemple simple de code Flask pour créer une page HTML avec un texte centré horizontalement et verticalement :

1. Créez un dossier nommé "templates" dans le répertoire de votre application Flask.
2. À l'intérieur du dossier "templates", créez un fichier nommé "index.html".
3. Utilisez le code suivant pour le fichier "index.html" :

```html
<!DOCTYPE html>
<html>
<head>
    <title>Page d'accueil</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .center-text {
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="center-text">
        <h1>Bienvenue dans mon site internet</h1>
    </div>
</body>
</html>
```

4. Utilisez le code suivant dans votre application Flask pour rendre cette page :

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

if __name__ == '__main__':
    app.run(debug=True)
```

Placez ce code Python dans un fichier nommé "app.py" à la racine de votre projet Flask.

Assurez-vous que Flask est installé (`pip install Flask`) et exécutez votre application avec la commande `python app.py`. Ensuite, accédez à `http://127.0.0.1:5000/` dans votre navigateur pour voir la page d'accueil avec le texte centré.
