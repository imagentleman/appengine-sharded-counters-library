# Sharded Counters Library for App Engine

A revision of the original sharding counters example library from Google (https://github.com/GoogleCloudPlatform/appengine-sharded-counters-python).

This forks adds:

- A reset method to set all the counters to zero.

- A delta parameter to increase the counter by any number (not just by 1), including negative values (the equivalent to decrement).

- A small refactor that encapsulates all the available methods to its related model (for portability).

The original provides:

- Simple Sharding: Uses a constant to define the number of shards and randomly
  picks an index up to this number when incrementing the counter. Each shard is
  stored in the datastore using one of these indices as ID.

- General Sharding: Stores the number of shards in the datastore and randomly
  picks an index up to this number when incrementing the counter. Each shard is
  stored in the datastore using one of these indices as ID, but also using a
  counter name as an ancestor.

## Products
- [App Engine][1]

## Language
- [Python][2]

## APIs
- [NDB Datastore API][3]
- [Memcache Python API][4]

## Dependencies
- [webapp2][5]
- [jinja2][6]


[1]: https://developers.google.com/appengine
[2]: https://python.org
[3]: https://developers.google.com/appengine/docs/python/ndb/
[4]: https://developers.google.com/appengine/docs/python/memcache/overview
[5]: http://webapp-improved.appspot.com/
[6]: http://jinja.pocoo.org/docs/
