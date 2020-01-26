# Inherit data from models

You can inherit from a model and modify the field

``` json5
body:{
    "$ref": "./_data/models.json:Article",
    "$include":["id", "title", "summary", "category_id", "author_name", "source", "tag"],
    id:{name:"article id", desc:"has id field is edit, no id field is add", type:"number", required:false},

},
```