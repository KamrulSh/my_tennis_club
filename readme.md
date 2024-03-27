### Django Create Project

`django-admin startproject my_tennis_club`

### Run the Django Project

`python3 manage.py runserver`

### Django Create App

`python3 manage.py startapp members `

### Django Models

> Migrate

`python3 manage.py makemigrations members`

`python3 manage.py migrate`

> View SQL

`python3 manage.py sqlmigrate members 0001`

### Django Insert Data (Add records)

`python3 manage.py shell`

> Add the code

```python
from members.models import Member

Member.objects.all()
```

```python
member1 = Member(first_name='K', last_name='Shahin', email='k.shahin@gmail.com', phone='1234567890', date_of_birth='2024-03-27')
member2 = Member(first_name='L', last_name='Shahin', email='l.shahin@gmail.com', phone='1234567890', date_of_birth='2024-03-27')
member3 = Member(first_name='M', last_name='Shahin', email='m.shahin@gmail.com', phone='1234567890', date_of_birth='2024-03-27')
members_list = [member1, member2, member3]
for x in members_list:
  x.save()

Member.objects.all().values()
```
