# Auth api doc


the test_data proviede the front end request and response test case data

#### request post /login/

body: 
```
{username:"edison", password:"123"}
```
get response:
```
{code:-1, msg:"password incorrect"}
```

#### request post /login/

body: 
```
{username:"lily", password:"123"}
```
get response:
```
{code:-2, msg:"username not exist"}
```


#### request post /login/

body: 
```
{username:"root", password:"123"}
```
get response:
```
{code:1, msg:"login success", token:"fjdlkfjlafjdlaj3jk2l4j"}
```





#### request post /login/

body: 
```
{username:"lily"}
```
get response:
```
{code:1, msg:"login success", token:"fjdlkfjlafjdlaj3jk2l4j"}
```


#### request post /login/

body: 
```
{password:"123"}
```
get response:
```
{code:-1, msg:"username is required"}
```


#### request get /logout/

query: 
```
{id:1, username:"root"}
```
get response:
```
{code:1, msg:"logout success"}
```
 
 
#### request get /logout/

query: empty

get response:
```
{code:-1, msg:"error"}
```



 
#### request get /logout/

query: 
```
{id:3, username:"lily"}
```
get response:
```
{code:-1, msg:"username and id not match"}
```


## response a object list

``` json5
result: 
    [{
        id:{name:"文章id", desc:"添加提交的时候是没有id, 编辑提交的时候才有", type:"number"},
        title:{name:"文章标题"},
        category_name:{name:"文章分类名称"},
        author_name:{name:"文章作者姓名"},
        tag:{name:"文章标签"},
        created:{name:"创建时间", type:"number"}
    }]

```