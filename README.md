# Server Example

## How to use

Install packages

```
yarn install
```

Start server

```
yarn start-server
```

## How to config other routes

1. Add the key on `db.json` file

```json
{
  "users": [],
  "posts": [],
  "comments": []
}
```

2. Config the permission in `routes.json`

```
{
    "users": 400,
    "posts": 640,
    "comments": 660
}
```

3. Restart your server

## Route Permissions

|    Route     | Resource permissions                                                                                 |
| :----------: | :--------------------------------------------------------------------------------------------------- |
| **`/664/*`** | User must be logged to _write_ the resource. <br> Everyone can _read_ the resource.                  |
| **`/660/*`** | User must be logged to _write_ or _read_ the resource.                                               |
| **`/644/*`** | User must own the resource to _write_ the resource. <br> Everyone can _read_ the resource.           |
| **`/640/*`** | User must own the resource to _write_ the resource. <br> User must be logged to _read_ the resource. |
| **`/600/*`** | User must own the resource to _write_ or _read_ the resource.                                        |
| **`/444/*`** | No one can _write_ the resource. <br> Everyone can _read_ the resource.                              |
| **`/440/*`** | No one can _write_ the resource. <br> User must be logged to _read_ the resource.                    |
| **`/400/*`** | No one can _write_ the resource. <br> User must own the resource to _read_ the resource.             |

[Json Server Auth Documentation](https://github.com/jeremyben/json-server-auth/blob/master/README.MD)
