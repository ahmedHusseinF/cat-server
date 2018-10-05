# Cat API - 3yourmind task

### Getting Started

```bash
npm install
npm run dev
```

Visit `http://localhost:3000/api/v1/cats/cute` to see expected JSON response.

Visit `http://localhost:3000/api/v1/cats/cute/0` to see cached image

By default config sets cache to 10 seconds

### Development

```bash
npm run dev
```

### Running tests

```bash
npm test
```

### Building a container

```bash
docker build .
```
cause why not

## API

### GET `/api/v1/cats/:tag`

PARAMS

- `tag` `string` `required`
- `base64` `boolean` `optional` `default:false`
- `tag` `string` `optional` `default:5`

RESPONSE `200`

```js
{
  cats: [
    'http://localhost:3000/api/v1/cats/cute/0',
    'http://localhost:3000/api/v1/cats/cute/1',
    'http://localhost:3000/api/v1/cats/cute/2',
    'http://localhost:3000/api/v1/cats/cute/3',
    'http://localhost:3000/api/v1/cats/cute/4'
  ]
}
```

### GET `/api/v1/cats/:tag/:id`

RESPONSE `200`

Image File

Example:
![Cute Cate](./example.jpeg)