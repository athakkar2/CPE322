# Lab 4 Documentation

## Part A: Stevens Django Server

First, I SSH'd into my Raspberry Pi running [Kali Linux](https://en.wikipedia.org/wiki/Kali_Linux) on my laptop. Then I had to install the necessary packages, but on Kali Linux I was not able to use the commands that were provided in Professor Lu's documentation. So I used the following commands to install the necessary packages:

```BASH
sudo apt install python3-setuptools
sudo apt install python3-django
sudo apt install python3-djangorestframework
sudo apt install python3-django-filter
sudo apt install python3-markdown
sudo apt install python3-requests
sudo apt install mariadb-server mariadb-client
sudo apt install python3-mysqldb
```

Then I set up MariaDB by running the following command and following the prompts which can be found in the [output log](lab4a.txt):

```BASH
sudo mysql_secure_installation
```

I then started my Django project, started the Django app using the manage.py file that was made, and created a MySQL database that would hold the data I give in the admin page of the website. After creating the database, I used the settings.txt file in Professor Lu's documentation to help change the settings.py file created by Django to use MySQL instead of SQLite3. I also had to add the username and password of the MariaDB user I created so that Django could access the database.

```BASH
django-admin startproject stevens
cd stevens
python3 manage.py startapp myapp
sudo mysql -u root -p
cd stevens
emacs settings.py
```

Then I had to copy the necessary files into my local Stevens project that would be used to host the website:

```BASH
cp ~/iot/lesson4/stevens/urls.py .
cd ..
cd myapp
cp ~/iot/lesson4/stevens/admin.py .
cp ~/iot/lesson4/stevens/models.py .
cp ~/iot/lesson4/stevens/views.py .
mkdir static templates
cd templates
mkdir myapp
cd myapp
cp ~/iot/lesson4/stevens/index.html .
cd ~/stevens/myapp/static
cp ~/iot/lesson4/static/favicon.ico .
mkdir myapp
cd myapp
cp ~/iot/lesson4/static/*css .
cp ~/iot/lesson4/static/*js .
cd ~/stevens
```

After copying the files into my local folder, I had to create a superuser that could access all the sections of the site including the admin page:

```BASH
python3 manage.py makemigrations myapp
python3 manage.py migrate
python3 manage.py createsuperuser
```

Finally I ran the Django server on my [Local Area Network](https://en.wikipedia.org/wiki/Local_area_network) so that I could access it on my laptop instead of using VNC because I have latency issues with VNC:

```BASH
python3 manage.py runserver 0.0.0.0:8000
```

After the server was running, I now had to access the admin page of the site to input time and temperature data that would appear at the frontend of the page. The admin page takes in the username and password made when you make the superuser, and once logged in the admin site looks like below:

![Django Admin page](Lab4A_1.png)

Once the time and temperature data is posted to the database, the home page can pull this data making the frontend of the website look like this:

![Home Page](Lab4A_2.png)

## Part B: MyCPU Django Server
