# global field settings

All response has field code and msg, you can set it in `_settings.json5`

``` json5
{
    project_name: "Panda Api",
    project_desc: "Panda Api is a simple api manage tool",
    global: {
    api:{
        response:{
        code:{name:"response result code", type:"int", desc:"success is 1"},
        msg:{name:"response result message", type:"string", desc:""},
      }
    }
  }
}
```



