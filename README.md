# local-dev-docker-nuxtjs

## How to use

```
$ git@github.com:Yamada-Factory/local-dev-docker-nuxtjs.git

$ cd local-dev-docker-nuxtjs

$ git clone git@github.com:{nuxt-project}.git

$ cp .env.sample .env

$ vim .env
dir=nuxt-project

$ docker-compose up -d
```


### vue.js ver

```
$ git@github.com:Yamada-Factory/local-dev-docker-nuxtjs.git

$ cd local-dev-docker-nuxtjs

$ git clone git@github.com:{vue-project}.git

$ cp .env.sample .env

$ vim .env
dir=vue-project

$ vim Dockerfile
- EXPOSE 3000
+ EXPOSE 8080

$ vim docker-compose.yml
- command: sh -c "npm install && npm run dev"
+ command: sh -c "npm install && npm run serve"

- - "3000:3000"
+ - "8080:8080"

$ docker-compose up -d
```
