# MongoDB 
all about MongoDB shell 

### To show All Databases that you have `show dbs`

### Which Database Currently you are using  `db`

### Create new DB Or Switch DB `use <Your DB name>`

### Drop DB  `db.dropDatabase()`

### Create Collection `db.createCollection('<Collection name>')`

### To Show all Collections  `show collections`

### Adding new Row 
```db.users.insert({name: 'Ali',age: 22,hopis: ['dance', 'sleep'],date: Date()})```

### Insert Multiple Rows
```db.posts.insertMany([
  {
    title: 'Post Two',
    body: 'Body of post two',
    category: 'Technology',
    date: Date()
  },
  {
    title: 'Post Three',
    body: 'Body of post three',
    category: 'News',
    date: Date()
  },
  {
    title: 'Post Four',
    body: 'Body of post three',
    category: 'Entertainment',
    date: Date()
  }
])```
Get All Rows
db.posts.find()
Get All Rows Formatted
db.find().pretty()
Find Rows
db.posts.find({ category: 'News' })
Sort Rows
# asc
db.posts.find().sort({ title: 1 }).pretty()
# desc
db.posts.find().sort({ title: -1 }).pretty()
Count Rows
db.posts.find().count()
db.posts.find({ category: 'news' }).count()

Find One Row
db.posts.findOne({ category: 'News' })
Find Specific Fields
db.posts.find({ title: 'Post One' }, {
  title: 1,
  author: 1
})
Update Row
db.posts.update({ title: 'Post Two' },
{
  title: 'Post Two',
  body: 'New body for post 2',
  date: Date()
},
{
  upsert: true
})
Update Specific Field
db.posts.update({ title: 'Post Two' },
{
  $set: {
    body: 'Body for post 2',
    category: 'Technology'
  }
})

Rename Field
db.posts.update({ title: 'Post Two' },
{
  $rename: {
    likes: 'views'
  }
})
Delete Row
db.posts.remove({ title: 'Post Four' })
