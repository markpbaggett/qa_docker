DLTN Metadata QA
================

Very basic config for running dltn_metadata_qa with Docker

Installing
----------

docker-compose --build


Running
-------

docker-compose up -d

Stopping
--------

docker-compose down

Using QA
--------

While Running, `docker-compose run dltn_qa bash`.

Then `cd qa` and `pipenv shell`.

By default, dltn_metadata_QA expects to find mongo on localhost.  We can't connect that way in the Docker network.

Instead:

```python
python addrecords.py -m MODS -s utk_ekcd -c this_is_a_test -mu mongo
```