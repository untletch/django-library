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
pip install -r requirements.txt
python manage.py runserver
```

## Run the tests

```sh
python manage.py test
```

# REST API

The REST API to the app is described below.

## Get list of articles

### Request

`GET /api/`

```sh
curl "localhost:8080" \
--header "Accept: application/json" \
--include
```

### Response

```console
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Sun, 29 May 2022 12:58:05 GMT
Content-Length: 113

[{"id":1,"title":"Article 1","content":"Article 1 body"},{"id":2,"title":"Article 2","content":"Article 2 body"}]
```

## Get a specific article

### Request

`GET /article/id`

```sh
curl "localhost:8080/article/view/1" \
--header "Accept: application/json" \
--include
```

### Response

```console
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
Date: Sun, 29 May 2022 13:04:13 GMT
Content-Length: 55

{"id":1,"title":"Article 1","content":"Article 1 body"}
```

## Get a non-existent article

### Request

`GET /article/view/id`

```sh
curl "localhost:8080/article/view/1000" \
--header "Accept: application/json" \
--include
```

### Response
```console
HTTP/1.1 404 Not Found
Content-Type: application/json; charset=utf-8
Date: Sun, 29 May 2022 12:56:05 GMT
Content-Length: 54

{"Error Code":404,"Error Message":"Article not found"}
```
