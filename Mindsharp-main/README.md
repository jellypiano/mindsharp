# Mindsharp: Quiz Generator

-Running Mindsharp locally
It can be deployed locally with the following instructions:

-Environment variables
You'll need to create a `.env` file in the root of the project with the following key-value pair:
```
OPENAI_SECRET_KEY=<your openai API key>
```

-Dependencies
You'll also need to install dependencies:
```shell
$ cd lib && pip3 install -e . && cd ..
$ cd site && pip3 install -r requirements.txt
$ cd frontend && npm install --legacy-peer-deps
```

-Database
When developing/running locally, we use SQLite to store generated items:
```shell
$ cd site
$ python3 create_db.py # set up local sqlite database
```

-Running the server + frontend
In one shell:
```shell
$ cd site
$ flask --app backend/main --debug run --port 5000 # run server in debug mode
```

In another shell:
```shell
$ cd site/frontend && npm run dev -- --port 3000
```
