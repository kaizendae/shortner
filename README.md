
## Setup
Run a postgres database on docker

`docker run --name pg-shortner -p 5444:5432 -e POSTGRES_PASSWORD=shortnerpass -e POSTGRES_USER=postgres -e POSTGRES_DB=shortnerdb -it postgres:11`

get the values from the last command and put `DATABASE_URL="postgresql://postgres:shortnerpass@localhost:5444/shortnerdb?schema=public"`in your .env file.

To interact with the database I recommend using pg-cli https://www.pgcli.com/install

```
insert into "ShortLink" ("createdAt", url, slug) values ( now(), 'https://google.com', 'ggl');
insert into "ShortLink" ("createdAt", url, slug) values ( now(), 'https://nextjs.org', 'nextjs');
insert into "ShortLink" ("createdAt", url, slug) values ( now(), 'https://tailwindcss.com/', 'tw');
insert into "ShortLink" ("createdAt", url, slug) values ( now(), 'https://twitter.com/', 'twtr');
insert into "ShortLink" ("createdAt", url, slug) values ( now(), 'https://medium.com/', 'mdm');
insert into "ShortLink" ("createdAt", url, slug) values ( now(), 'https://guichet.ma/', 'gct');
```
## Run

the development server:

```
yarn dev
```

