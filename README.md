# docker-partitur
Dockerizing my Partitur app

Depends on the code in <https://bitbucket.org/philip_diderichsen/lanchart_partitur>, which generates an SQLite db with corpus data.


Run with an environment variable containing the volume containing the SQLite db. Since the variable is not used inside the container, a warning will be issued ("`WARNING: The OUTPUT_VOLUME_PATH variable is not set. Defaulting to a blank string.`"). This can be ignored.

```
cd docker-partitur
OUTPUT_VOLUME_PATH=/opt/parse_textgrids/output docker-compose up -d --build
```
