# eslint (Alpine)


Minimal eslint image using Alpine.


# Usage

## Example usage via Docker Compose

### docker-compose.yml

```yaml
version: "2"
services:
  lint-js:
    image: 5monkeys/lint-eslint
    volumes:
      - "./.eslintrc.js:/.eslintrc.js"
      - ".:/code"
    command: /code/.*.js  /code/src/static/js/ --ignore-pattern '!.*.js'
```

### Running

```bash
$  docker-compose run --rm lint-js
```
