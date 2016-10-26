# Node with Yarn Docker

These images are based on the official node image and have [yarn](https://yarnpkg.com) installed and have a non-root user called `app` (/home/app) set up.

Your `package.json` and `yarn.lock` files will be copied across and installed, and then your code will be copied across to the WORKDIR.

You can get your node webapp running easily with a Dockerfile like:
```
FROM jsixc/node-yarn-app:4

EXPOSE 8080
```
