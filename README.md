# django-library

## About The Project
django-library stores details about different books.

## Clone the Repo

```sh
git clone https://github.com/untletch/django-library.git
```

## Run the app locally

```sh
cd django-library
git checkout dev
pip install -r requirements.txt
python manage.py runserver
```

## Run the tests

```sh
python manage.py test
```

# REST API

The REST API to the app is described below.

## Get list of books

### Request

`GET /api/`

```sh
curl "localhost:8000" \
--header "Accept: application/json" \
--include
```

### Response

```console
HTTP/1.1 200 OK
Date: Thu, 03 Nov 2022 12:30:11 GMT
Server: WSGIServer/0.2 CPython/3.9.12
Content-Type: application/json
Vary: Accept, Cookie
Allow: GET, HEAD, OPTIONS
X-Frame-Options: DENY
Content-Length: 1099
X-Content-Type-Options: nosniff
Referrer-Policy: same-origin
Cross-Origin-Opener-Policy: same-origin

[{"title":"Eloquent JavaScript, Third Edition","subtitle":"A Modern Introduction to Programming","author":"Marijn Haverbeke","isbn":"9781593279509"},{"title":"Practical Modern JavaScript","subtitle":"Dive into ES6 and the Future of JavaScript","author":"Nicolás Bevacqua","isbn":"9781491943533"},{"title":"Understanding ECMAScript 6","subtitle":"The Definitive Guide for JavaScript Developers","author":"Nicholas C. Zakas","isbn":"9781593277574"},{"title":"Speaking JavaScript","subtitle":"An In-Depth Guide for Programmers","author":"Axel Rauschmayer","isbn":"9781449365035"},{"title":"Learning JavaScript Design Patterns","subtitle":"A JavaScript and jQuery Developer's Guide","author":"Addy Osmani","isbn":"9781449331818"},{"title":"You Don't Know JS Yet","subtitle":"Get Started","author":"Kyle Simpson","isbn":"9798602477429"},{"title":"Pro Git","subtitle":"Everything you neeed to know about Git","author":"Scott Chacon and Ben Straub","isbn":"9781484200766"},{"title":"Django for APIs","subtitle":"Build web APIs with Python and Django","author":"William S. Vincent","isbn":"9781735467221"}]
```
