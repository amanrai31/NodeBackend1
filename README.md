# NodeBackend1
What we are using in this app =>JS, Node, express, mongoose

Note => We will push .envSample file(for refernce) as we cannot push .env. Update .env a/c .envSample

NOTE => Dev dependencies are used for development purpose only they do not go to PROD.  -D d flag used to install them.
1. nodemon (See "dev" script in package.json)
2. prettier  [ .prettierrc(rules of prettier)  and prettierignore(what to ignore by prettier)]
Note => If we change in env variables, we have to restart server manually, nodemon will not work there.
We will store our assets in public/temp folder
.gitkeep file. 

git config --global core.autocrlf true

### Files 
1. public > temp
2. src > [routes, controllers, middlewares, db, models, utils]

1. Go mongo Atlas
2. Create project
3. Create a cluster
4. give permissions to IPs you want to access your cluster. Or give 0.0.0.0/0 to allow all.
5. My DB access should be allowed for my backend server only.(AWS server, digital ocean wherever my BE server is deployed).
6. copy mongoDB URI from atlas and paste in .env file.

### 2 things to keep in mind while connecting to DB=>
1. Use try,catch OR promise(resolve,reject) because any wrong can happen while connecting to DB.
2. Use async/await because DB is far away.