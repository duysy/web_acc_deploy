django-admin startproject webacc
python manage.py startapp ecommerce
python manage.py migrate
python manage.py makemigrations ecommerce
python manage.py createsuperuser
python manage.py runserver