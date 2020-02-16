# global field settings

All response has field code and msg, you can set it in `_settings.json5`

the original response field

``` json5
response:{
    // code:{name:"response result code", type:"int", desc:"success is 1"}, // remove the field code
    // msg:{name:"response result message", type:"string", desc:""}, // remove the field msg
    data: {
        "-name":"data field name",
        "-desc":"data field description",
        "$ref": "./_data/models.json:Article", // or do not use define
        "$exclude":["category_id"]
    }
}
```

set field in `_settings.json5`

``` json5
{
    project_name: "Panda Api",
    project_desc: "Panda Api is a simple api manage tool",
    global: {
    apis:{
        response:{
            code:{name:"response result code", type:"int", desc:"success is 1"},
            msg:{name:"response result message", type:"string", desc:""},
      }
    }
  }
}
```



the response will render out

``` json5
response:{
    code:{name:"response result code", type:"int", desc:"success is 1"},
    msg:{name:"response result message", type:"string", desc:""},
    data: {
        "-name":"data field name",
        "-desc":"data field description",
        "$ref": "./_data/models.json:Article", // or do not use define
        "$exclude":["category_id"]
    }
}
```

