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
sudo apt -y install apt-transport-https ca-certificates curl gnupg2 software-properties-common
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io

sudo curl -L https://github.com/docker/compose/releases/download/1.25.3/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version

sudo ufw allow http
sudo ufw allow https

git clone https://github.com/duysy/web_acc_deploy.git

cd web_acc_deploy/
docker-compose run web python manage.pyc migrate
docker-compose run web python manage.pyc createsuperuser 
docker-compose up

