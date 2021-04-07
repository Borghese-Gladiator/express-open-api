# Express-OpenAPI

Found code from article here: [https://www.freecodecamp.org/news/how-to-build-explicit-apis-with-openapi/](https://www.freecodecamp.org/news/how-to-build-explicit-apis-with-openapi/)

- Above article explains difficulties APIs encounter as they grow:
  - Harder to make changes (changing return values can break application)
  - Separately update documentation
  - Public APIs (cannot be changed as others build core functionality on exposed API)
  - Manual Integration Tests
## Solution
Standardize REST API definitions, so client SDKs, tests, mock servers and documentation can be auto generated from those specifications

## Auto-Generation
- Using the schema available in http://localhost:3030/api-docs we can now easily generate tests, a mock server, types or even a client!

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
- used SwaggerUi to auto generate documentation

![Downloaded Swagger Screenshot from Article](/image-23.png)
