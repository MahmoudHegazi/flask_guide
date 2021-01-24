# flask_guide

# while using vagrant


### how to handle unknown counts of paramter came to your server in professional object 
##### this how the rest created
```
@app.route('/paypalcallback/<string:payload>', methods=['GET'])
def lols(payload):
    secured = '%s' % payload

    payment_object = {'complete_token':str(),'additonal_pramter':str()}
    paramters_object = {}
    # real important if not found & it will return list contains stirng nice
    paramter_list = secured.split('&')
    for query_paramter in paramter_list:
        half = query_paramter.split('=')
        paramters_object[half[0]] = half[1]
    return jsonify(paramters_object)
```

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
