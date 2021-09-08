#Logistic Regression on Titanic Dataset
In this project I'm attempting to do data analysis on the Titanic Dataset. In the first step I'm doing a very quick data exploration and preprocessing on a visual level, plotting some simple plots to understand the data better. Then I've done some data cleaning and built a Classifier that can predict whether a passenger survived or not.

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
    ├── api              - web related stuff.
    │   ├── dependencies - dependencies for routes definition.
    │   ├── errors       - definition of error handlers.
    │   └── routes       - web routes.
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




