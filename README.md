# Stock Market Analysis

## Preconditions:

- Python 3

## Run local

### Install dependencies

```
pip install -r requirements.txt
```

### Run server

```
uvicorn app.main:app --reload
```


To run the web application in debug use::

    alembic upgrade head
    uvicorn app.main:app --reload


Web routes
----------

All routes are available on ``/docs`` or ``/redoc`` paths with Swagger or ReDoc.



Project structure
-----------------

Files related to application are in the ``app`` or ``tests`` directories.
Application parts are:


    app
    ├─── repository           - all crud stuff.
    │   ├── stocks.py         - stocks related crud operation.
    │   ├── user.py           - stocks related crud operation.
    │
    ├── routers               - web routes.
    │   ├── __init__.py       
    │   └── authentication.py - all crud stuff.
    │   └── stocks.py         
    │   └── user.py
    │
    ├── __init__.py
    ├── database.py           - database connection related stuff.
    ├── hashing.py            - convert plain password into hash password.
    ├── models.py             - pydantic models for this application.
    ├── oauth2.py             - jwt token generation
    ├── schemas.py            - schemas for using in web routes.
    ├── token.py              - token generation and token verification.
    └── main.py               - FastAPI application creation and configuration.




