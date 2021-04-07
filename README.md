# Express-OpenAPI

Found code from article here: [https://www.freecodecamp.org/news/how-to-build-explicit-apis-with-openapi/](https://www.freecodecamp.org/news/how-to-build-explicit-apis-with-openapi/)
- Above article explains how documentation was a pain with REST APIs since every API update requires a separate documentation update && a testing update
- Using the schema available in http://localhost:3030/api-docs we can now easily generate tests, a mock server, types or even a client!

## Auto-Generate Documentation
```
// OpenAPI UI
app.use(
  "/api-documentation",
  swaggerUi.serve,
  swaggerUi.setup(null, {
    swaggerOptions: {
      url: "http://localhost:3030/api-docs",
    },
  })
);
```
- use SwaggerUi to auto generate documentation

![Downloaded Swagger Screenshot from Article](/images/image-23.png)
