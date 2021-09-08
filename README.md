# Stock Market Analysis
Stock market analysis is a widely studied problem as it offers practical applications for signal processing and predictive methods and a tangible financial reward. Creating a system that yields consistent returns is extremely challenging and is currently an open problem as stock market prices are extremely volatile and vary widely both within a given stock and comparatively amongst many stocks. Further, stock market data is influenced by a large number of factors including foreign and domestic economies, trade agreements, wars. 

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

    uvicorn app.main:app --reload


Web routes
----------

All routes are available on ``/docs`` or ``/redoc`` paths with Swagger or ReDoc.



Project structure
-----------------

Files related to application are in the ``app``  directories.
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




