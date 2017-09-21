# Puppeteer Docker
A [GoogleChrome/puppeteer](https://github.com/GoogleChrome/puppeteer) docker container.

## Usage

```
docker run -v <project folder path>:/app -t oozman/puppeeter
```

Where `<project folder path>` is your absolute path to your node.js project folder.

**Example:**

```
docker run -v /Users/johndoe/awesomeapp:/app -t oozman/puppeteer
```

### Note:
* Make sure your project contains `index.js` file. This is the one that will be called on `docker run`.
* It's recommended when declaring a puppeteer instance, make sure you add ` args: ['--no-sandbox'] }` as parameters. Example:
  ```
  const browser = await puppeteer.launch({ args: ['--no-sandbox'] });
  ```
