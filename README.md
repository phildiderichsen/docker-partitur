# docker-partitur
Dockerizing my Partitur app

Depends on the code in <https://bitbucket.org/philip_diderichsen/lanchart_partitur>.


Run with an environment variable containing the volume containing the SQLite db.

```
cd docker-partitur
OUTPUT_VOLUME_PATH=/opt/parse_textgrids/output docker-compose up -d --build
```
