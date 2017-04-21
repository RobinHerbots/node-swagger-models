# node-swagger-models

Generate javascript models from a self-documenting Swagger API.

- backbone models
- plain json

## Install

    $ npm install -g node-swagger-models

## Usage

node-swagger-models nsmconfig.json

nsmconfig.json
```
{
  "fileOutput": "./tmp",
  "api": "http://localhost:1802/api-docs/v1/swagger.json",
  "format": "backbone"
}
```

node-swagger-models

package.json
```
...
node-swagger-models : {
  "fileOutput": "./tmp",
  "api": "http://localhost:1802/api-docs/v1/swagger.json",
  "format": "backbone"
}
...
```

## Notes

There is support for a vender extension on the swagger schemadefintion.  
x-key to denote the primary key of the model.  
For the backbone models this will translate to the idAttribute.

For an example of a venderextension with swashbuckle (dotnet) see the extra folder.  
(If you know better ways to create a venderextension, please let me know)

Other models can be generated by creating a template in lib/formatters/.