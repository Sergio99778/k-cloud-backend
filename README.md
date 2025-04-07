# K-Cloud-Backend REST API for Making a NAS

## Why

I DO NOT WANT TO USE NEXT CLOUD

This is my own solution

## Setup

1. Install dependencies

```bash
npm install
```

2. Setup env variables; see `.env.example`

*env variables*
* FILE_ROOT - the directory where the files will be stored

example:
```env
FILE_ROOT="/home/user/data"
```

* DATABASE_URL 
Location and name of the database, start with *file:*
example:
```env
DATABASE_URL="file:///home/user/database.db"
```

* SECRET_KEY - the key for JWT

It is a string and can be anything

* CORS_LIST - the domain and IP addresses for CORS
example:
```env
CORS_LIST="http://192.168.50.239:3000|http://localhost:3000|http://localhost"
```

* SETTINGS (optional)
Path where a JSON file with some options will be stored
- Note: The file will be deleted in every `build` if you do not set up this variable -
example:
```env
SETTINGS="/home/user/K/settings.json"
```

* NEST_APP_CLUSTER (optional)
It can only be 2 possible values:
1 for enable cluster
0 for disable the cluster mode

3. Prisma

Initialize the database with the command:

```bash
npx prisma db push
```

4. Run the app
Build the app:
```bash
npm run build
```
Once the app is built you can run it using one of these commands:
* `npm run start:prod-3072`
* `npm start`
* `npm run start:prod-2048`