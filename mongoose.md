# mongoose
mongoose 是 nodeJs 用来连接 mongoDB 的ODM ( Object-Document Mapping，对象文档映射)。

# 连接数据库
```js
const mongoose = require('mongoose')

// 连接本地数据库 test
mongoose.connect('mongodb://localhost/test', {
  useNewUrlParser: true,
  useUnifiedTopology: true
})
```

# Schema
模式

```js
const { Schema } = require('mongoose')

const UserSchema = new Schema({
  name: String,
  age: Number,
  like: Array
})
```

# Model
模型

```js
const { model } = require('mongoose')

// user 对应数据库 test 里的 users 集合, 此处不用加 s
const UserModel = model('user', UserSchema)
```

