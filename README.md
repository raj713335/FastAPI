## Start the FastAPI APP

```commandline
uvicorn books:app --reload
uvicorn TodoApp.main:app --reload


if __name__ == '__main__':
    uvicorn.run("main:app", host=os.getenv("APP_HOST", "localhost"), port=int(os.getenv("APP_PORT", 5000)),
                reload=True)
```


## Swagger

```commandline
http://127.0.0.1:8000/docs
```

## Pydantic v1 vs Pydantic v2

FastAPI is now compatible with both Pydantic v1 and Pydantic v2.
Based on how new the version of FastAPI you are using, there could be small method name changes.


The three biggest are:
- .dict() function is now renamed to .model_dump()
- schema_extra function within a Config class is now renamed to json_schema_extra
- Optional variables need a =None example: id: Optional[int] = None

## SQL Queries
.mode table
INSERT INTO todos(title, description, priority, complete) VALUES ('Go to Store', 'To pick up eggs', 4, False);\


## ALEMBIC COMMANDS

```commandline
pip install alembic
```

| VAR                           | DESCRIPTION                                 |
|-------------------------------|---------------------------------------------|
| alembic init {folder name}    | Initializes a new, generic environment      |
| alembic revision -m {message} | creates a new revision of the environment   |
| alembic upgrade {revision #}  | Run our upgrade migration to our database   |
| alembic downgrade -1          | Run our downgrade migration to our database |


## Pytest 

```commandline
pytest --disable-warnings
```
