# Framework-lab1
Ministerul Educatiei Republicii Moldova
Universitatea de Stat din Moldova
Facultatea de Matematica si Informatica



DARE DE SEAMA


Lucrarea de laborator nr. 1:
Framework





   Elaborat de: Diaconu Cristian, Gr. IA2101
A verificat: Nartea Nichita, Lector Universitar

Chisinau 2024



Sarcina nr. 1. Analiza cererilor HTTP

1. Ce metodă HTTP a fost utilizată pentru a trimite cererea?
Cererea utilizează metoda POST
2. Ce anteturi au fost trimise în cerere?
Anteturile trimise în cerere sunt:
•	Accept-Language: en-GB,en;q=0.9,en-US;q=0.8,ro;q=0.7
•	Accept-Encoding: gzip, deflate
•	Referer: http://sandbox.usm.md/login/
•	Origin: http://sandbox.usm.md
•	Content-Type: application/x-www-form-urlencoded; charset=UTF-8
•	Accept: */*
•	User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/130.0.0.0 Safari/537.36
•	X-Requested-With: XMLHttpRequest
•	Content-Length: 35
•	Connection: keep-alive
•	Host: sandbox.usm.md
3. Ce parametri au fost trimiși în cerere?
1.	username: 
studdent
2.	password: 
studpass
4. Ce cod de stare a fost returnat de server?
HTTP/1.1 401 Unauthorized
5. Ce anteturi au fost trimise în răspuns?
HTTP/1.1 401 Unauthorized
Server: nginx/1.24.0 (Ubuntu)
Date: Wed, 30 Oct 2024 09:59:02 GMT
Content-Type: text/plain;charset=UTF-8
Transfer-Encoding: chunked
Connection: keep-alive
Repetați pașii 3-5, introducând date corecte pentru autentificare (username: admin, password: password).

1. Ce metodă HTTP a fost utilizată pentru a trimite cererea?
Cererea utilizează metoda POST
2. Ce anteturi au fost trimise în cerere?
Anteturile trimise în cerere sunt:
Accept-Encoding: gzip, deflate
Accept-Language: en-GB,en;q=0.9,en-US;q=0.8,ro;q=0.7
Connection: keep-alive
Content-Length: 32
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
Host: sandbox.usm.md
Origin: http://sandbox.usm.md
Referer: http://sandbox.usm.md/login/
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/130.0.0.0 Safari/537.36
X-Requested-With: XMLHttpRequest
3. Ce parametri au fost trimiși în cerere?
3.	username: 
admin
4.	password: 
password
4. Ce cod de stare a fost returnat de server?
HTTP/1.1 200 OK
5. Ce anteturi au fost trimise în răspuns?
Server: nginx/1.24.0 (Ubuntu)
Date: Wed, 30 Oct 2024 10:06:24 GMT
Content-Type: text/plain;charset=UTF-8
Transfer-Encoding: chunked
Connection: keep-alive

Sarcina nr. 2. Crearea cererilor HTTP
Scrieți o cerere de tip GET către server la adresa http://sandbox.com, indicând în antetul User-Agent numele și prenumele dvs.
GET / HTTP/1.1
Host: sandbox.com
User-Agent: [Diaconu Cristian]

2.Scrieți o cerere de tip POST către server la adresa http://sandbox.com/cars, indicând în corpul cererii următorii parametri:
make: Toyota
model: Corolla
year: 2020

POST /cars HTTP/1.1
Host: sandbox.com
Content-Type: application/x-www-form-urlencoded
Content-Length: 25

make=Toyota&model=Corolla&year=2020

Scrieți o cerere de tip PUT către server la adresa http://sandbox.com/cars/1, indicând în antetul User-Agent numele și prenumele dvs., în antetul Content-Type valoarea application/json, iar în corpul cererii următorii parametri:

PUT /cars/1 HTTP/1.1
Host: sandbox.com
User-Agent: [Diaconu Cristian]
Content-Type: application/json
Content-Length: 53

{
    "make": "Toyota",
    "model": "Corolla",
    "year": 2021
}

Raspuns posibil:
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 53

{
    "status": "success",
    "message": "Car updated successfully"
}

•  200 OK: Cererea a fost procesată cu succes. De exemplu, un PUT sau GET reușit.
•  201 Created: Obiectul a fost creat cu succes, de exemplu, pentru o cerere POST reușită.
•  400 Bad Request: Serverul nu poate procesa cererea din cauza unui format invalid (ex: JSON incorect).
•  401 Unauthorized: Autentificare necesară; clientul nu a furnizat credențiale sau sunt incorecte.
•  403 Forbidden: Acces refuzat chiar dacă clientul este autentificat, din cauza permisiunilor insuficiente.
•  404 Not Found: Resursa nu a fost găsită, de exemplu, un GET sau PUT pe un id inexistent.
•  500 Internal Server Error: Eroare internă a serverului, care poate apărea dacă serverul întâmpină o problemă neașteptată.
Cerere de tip DELETE:

DELETE /cars/1 HTTP/1.1
Host: sandbox.com
User-Agent: [Diaconu Cristian]


Sarcina nr. 3. Sarcina suplimentară. HTTP_Quest

Secret: LSUOFQonFkUPEx0HEUgIIkJEVQ==
