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
    ├─── repository      - all crud stuff.
    │   ├── stocks       - stocks related crud operation.
    │   ├── user         - stocks related crud operation.
    │
    ├── core             - application configuration, startup events, logging.
    ├── db               - db related stuff.
    │   ├── migrations   - manually written alembic migrations.
    │   └── repositories - all crud stuff.
    ├── models           - pydantic models for this application.
    │   ├── domain       - main models that are used almost everywhere.
    │   └── schemas      - schemas for using in web routes.
    ├── resources        - strings that are used in web responses.
    ├── services         - logic that is not just crud related.
    └── main.py          - FastAPI application creation and configuration.




