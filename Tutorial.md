

# Activate env
 ./venv/Scripts/activate

# Connection URI Format  
 #Windows (note 3 leading forward slashes and backslash escapes)
 sqlite:///C:\\absolute\\path\\to\\foo.db

# env variable
 $env:FLASK_APP = "database.py"  

# enter flask shell
  flask shell

# create database
  from database import db
  db.create_all() 

# add records
 >>> from yourapplication import User
 >>> admin = User(username='admin', email='admin@example.com')
 >>> guest = User(username='guest', email='guest@example.com')

# save records
 >>> db.session.add(admin)
 >>> db.session.add(guest)
 >>> db.session.commit()

# Accessing the data in database :

>>> User.query.all()
>>> User.query.filter_by(username='admin').first()


