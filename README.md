# fakeApi
This is full fake REST API server.

## Routes

Based on the previous `db.json` file, here are all the default routes. You can also add [other routes](#add-custom-routes) using `--routes`.

### Plural routes

```
GET    /ideas
GET    /ideas/1
POST   /ideas
PUT    /ideas/1
PATCH  /ideas/1
DELETE /ideas/1
```

### Filter

Use `.` to access deep properties

```
GET /ideas?id=1&id=2
GET /ideas?state=Done
```

### Paginate

Use `_page` and optionally `_limit` to paginate returned data.

In the `Link` header you'll get `first`, `prev`, `next` and `last` links.


```
GET /ideas?_page=1
GET /ideas?_page=1&_limit=20
```

_10 items are returned by default_

