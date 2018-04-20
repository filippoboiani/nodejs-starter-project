# Node JS - Typescript - MongoDB - Docker

This repo is intended for those who need an extremely simple [Express][1] application using [Typescript][2] and [MongoDB][3].

## Compile and Run the application (for development)

0. Run: 

```
npm install 
``` 

1. A You only need to run the following:

```
npm run tsc
```

1. B Alternatively you may run the following to tell the Typescript compiler to run everytime it detects a filesystem change.

```
npm run tsc -- --watch
```

These commands will tell the Typescript compiler to build the application based on the `tsconfig.json`.
If everything has been successfull you will see a newly created `dist` directory.
This is where the Typescript compiler has placed the generated `.js` files based of the optional `outDir` parameter in the `tsconfig`.

3. A We can now run the app with the following command.

```
node dist/server.js
```

3. B You can also run the commmand using nodeamon

```
nodemon dist/server.js
```

4. Open a browser at the following url [http://localhost:3000/welcome](http://localhost:3000/welcome).

## Automation 

1. For a faster strart you can user the following: 

```
npm start
```

**Note**: you need to install mongodb on your local machine and run it with the correct configuration. More stuff to come. 

## With Docker 

1. Run: 

```
docker-compose up --build 
```

This command will take by default the docker-compose.yml file in the repo, build the images and start the containers. 

## Summary

This application, though simple, gives a good basis for creating future Express applications with Typescript.

You have learned how to intialise a Typescript application from the command line.
You have also seen how to make use of Typings within a Typescript application.
Learning how to use typings is very important when working with Typescript as they give the compiler a better knowledge of the application.
The more the compiler knows, the better it can help you out.

You have also learned a bit about structuring an Express application.
Many Express tutorials bundle code into one big `server.js` file.
This leads to an application that is very difficult to maintain and is not representative of real world applications.
However we have seen here that it is possible to _mount_ Express Router instances so that applications can be broken down into modular parts.
This leads to more maintainable and scalable applications.

## Next Steps?

// TODO

---
## References

[1]: http://expressjs.com/
[2]: https://www.typescriptlang.org/
[3]: https://www.mongodb.com/
