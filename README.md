# TODO-List

**SCURTA DESCRIERE**

Aplicatia iti ofera posibilitatea de a-ti gestiona eficient activitatile dintr-o anumita perioada de timp. Fiecare client se poate inregistra pe platforma, creandu-si  un cont in care isi va putea stoca toate activitatile/evenimentele. Aplicatia dispune de un serviciu care urmareste fiecare activitate/eveniment si care te notifica prin mail cu o zi inainte ca in urmatoarea zi se va desfasura evenimentul respectiv.

**LIMBAJE/TEHNOLOGII FOLOSITE**

Aplicatia web este construita cu ajutorul frameworkului de python, Flask. Pe partea de front-end am folosit HTML & CSS, constructia paginilor fiind realizata cu ajutorul tamplate-urilor Jinja de care se foloseste Flask.
Pentru lucrul cu baza de date am folosit MongoDB.

**Bibliotecile de python folosite**

email_validator==1.3.0
Flask==2.2.2
Flask_PyMongo==2.3.0
Flask_WTF==1.1.1
pymongo==4.3.3
bcrypt==4.0.1
WTForms==3.0.1.

**INSTRUCTIUNI PENTRU RULARE**

Pentru a rula aplicatia se va intra in folderul our_scheduler si se vor rula urmatoarele comenzi in terminal:
sudo docker build -t scheduler
sudo docker run scheduler.
Se va porni un server local pentru develompment pentru aplicatie (adresa se poate gasi in informatiile date de server la inceput: localhost:5000)
Pentru a porni serviciul care verifica odata la un minut baza de date se vor rula urmatoarele comenzi 
sudo docker build -t cronpy . -f Dockerfile.checkdb
sudo docker run cronpy
NOTA: Am comentat infinite loopul din scriptul de bash ca sa fie mai usor la testare. Deci pentru testare practiv se ruleaza o singura data scriptul cron.py

