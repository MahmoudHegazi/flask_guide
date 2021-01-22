# flask_guide

# while using vagrant

to run the venv

```python

mkdir project
cd project
# always-copy is important for vagrant
virtualenv env --always-copy

```

# db migrate

```python3

pip install Flask-Migrate


from flask import Flask
from flask_sqlalchemy import SQLAlchemy
from flask_migrate import Migrate

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///app.db'

db = SQLAlchemy(app)
migrate = Migrate(app, db)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(128))
    
    flask db init
```
