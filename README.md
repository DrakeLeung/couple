# couple
a comment parser 🌵 

## Intro
If comment:

```javascript
/*
 * @module setting/profile - hero's basic info
 * @action getHero - get a hero's profile
 * @api {GET} /api/heroes/:id
 * @param {Int} id - hero's id
 */
```

After parsed:

```javascript
{
  type: "project",
  body: [
    {
      type: "module",
      field: "setting/profile",
      description: "hero's basic info",
      body: [
        {
          type: "action",
          field: "getHero",
          description: "get a hero's profile",
          body: [
            {
              type: "api",
              datatype: "GET",
              field: "/api/heroes/:id"
            },
            {
              type: "param",
              datatype: "Int",
              field: "id",
              description: "hero's id"
            }
          ]
        }
      ]
    }
  ]
}
```

## Development

```bash
# install
npm i

# start, and open http://localhost:10001/docs/index.html
npm start

# build for production
npm run build
```
