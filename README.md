## Boilerplate de Parse para Android 

Esta es una plantilla básica pre-configurada con Parse (BaaS),
si deseas saber más acerca de Parse, revisa estos enlaces:
[The Parse Open Source Project](http://parseplatform.org/)
[Parse Server](https://github.com/parse-community/parse-server)


## Configuración inicial

Primero, abre el archivo:

     strings.xml

Y reemplace las strings "**" en:

     <string name="parse_app_id"> ** </string>
     <string name="parse_client_key"> ** </string>
    
Estos valores son usados para inicializar Parse
```
Parse.initialize(this, "YOUR_APP_ID", "YOUR_CLIENT_KEY");
```

Para este caso vamos a utilizar el servidor [Parse Server](https://github.com/parse-community/parse-server)

     <string name="parse_server_url">http://SERVER:PORT</string>
    
## Prueba Final

Cree una clase llamada: "TestClass" en su servidor Parse y agregue una columna llamada "mensaje".

Sin el dashboard, desde tu implementación de  [Parse Server](https://github.com/parse-community/parse-server):

`const schema = new Parse.Schema('MyClass');`  
`schema.addString('field');`  
`schema.addIndex('index_name', {'field', 1}, { unique : true });`  
`schema.save();`

Después, agregue una fila y coloque el texto "Hola mundo" en la columna y ejecute la aplicación.