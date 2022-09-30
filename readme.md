django-admin startproject webacc
python manage.py startapp ecommerce
python manage.py migrate
python manage.py makemigrations ecommerce
python manage.py createsuperuser
python manage.py runserver


sudo apt update
sudo apt install git
git --version

sudo apt-get update
sudo apt-get install docker-ce
sudo apt-get install docker-ce-cli
sudo apt-get install -y docker.io
sudo apt-get install docker-compose-plugin

sudo ufw allow http
sudo ufw allow https

git clone https://github.com/duysy/web_acc_deploy.git