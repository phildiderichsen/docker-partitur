# docker-partitur
Dockerizing my Partitur app

Depends on: 
- https://bitbucket.org/philip_diderichsen/parse_textgrids, which generates an SQLite db with corpus data.
- <https://bitbucket.org/philip_diderichsen/lanchart_partitur>, which builds the partitur app.


Run with environment variables specifying volumes:
- `DB_PATH`: The folder containing the SQLite db.
- `CODE_PATH`: The folder containing the partitur code.
 
Since the variables are not used inside the container, a warning will be issued (`WARNING: The DB_PATH variable is not set. Defaulting to a blank string.`"). This can be ignored.

```
cd docker-partitur
DB_PATH=/opt/parse_textgrids/output CODE_PATH=/opt/lanchart_partitur docker-compose up -d --build
```

Note! different syntax in Windows PowerShell:

```
cd docker-partitur
$env:DB_PATH='C:\custom_software\parse_textgrids\output' ; $env:CODE_PATH='C:\custom_software\lanchart_partitur' ; docker-compose up -d --build
```
