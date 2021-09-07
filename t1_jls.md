# Tarea 1

## Jose Luis Sandin

### _Queries_

```sh

- 12. 

  db.restaurants.find({cuisine:{$ne:"American"},
  "grades.score":{$gt:70},
  "address.coord":{$lt:-65.754168}})

- 13.
  db.restaurants.find({cuisine:{$ne:"American"},
  "grades.grade":"A",
  borough:{$ne:"Brooklyn"}})

- 14.
  db.restaurants.find({name:/^Wil/},{"restaurant_id":1,name:1,
  borough:1, cuisine:1,_id:0})

- 15.
  db.restaurants.find({name: /ces$/},{"restaurant_id":1,name:1,
  borough:1, cuisine:1,_id:0})

- 16.
  db.restaurants.find({name:/Reg/},{"restaurant_id":1,name:1,
  borough:1,cuisine:1,_id:0})

- 17.
  db.restaurants.find({borough:"Bronx", $or:[{"cuisine":"American"},
  {cuisine:"Chinese"}]})

- 18.
  db.restaurants.find({"borough":{$in:["Staten Island","Queens","Bronx","Brooklyn"]}},
  {"restaurant_id":1,"name":1,"borough":1,"cuisine":1,_id:0})

- 19.
  db.restaurants.find({"borough":{$nin:["Staten Island","Queens","Bronx","Brooklyn"]}},
  {"restaurant_id":1,"name":1,"borough":1,"cuisine":1,_id:0})

- 20.
  db.restaurants.find({"grades.score":{$not:{$gt:10}}},{"restaurant_id":1,
  "name":1,"borough":1,"cuisine":1,_id:0})

- 21.
  db.restaurants.find({$or:[{name:/^Wil/},{$and:[{"cuisine":{$ne:"American"}},
  {"cuisine":{$ne:"Chinese"}}]}]},
  {"restaurant_id":1,"name":1,"borough":1,"cuisine":1,_id:0})

- 22.
  db.restaurants.find({"grades.grade":"A","grades.score":11,
  "grades.date":ISODate("2014-08-11T00:00:00.000Z")},
  {"restaurant_id":1,"name":1,"grades":1,_id:0})

- 23.
  db.restaurants.find({"grades":{$elemMatch:{
  "grade":"A","score":9,
  "date":ISODate("2014-08-11T00:00:00.000Z")}}},
  {"restaurant_id":1,"name":1,"grades":1,_id:0})

- 24.
  db.restaurants.find({"address.coord":{$gt:42,$lte:52}},
  {"restaurant_id":1,"name":1,"address":1,_id:0})

- 25.
  db.restaurants.find({},{name:1, _id:0}).sort({name:1})

- 26.
  db.restaurants.find({},{name:1,_id:0}).sort({name:-1})

- 27.
  db.restaurants.find({},{"cuisine":1,"borough":1,_id:0}).sort({"cuisine":1,"borough":-1})

- 28.
  db.restaurants.find({"address.street":{$exists:true}},{name:1,_id:0})

- 29.
  db.restaurants.find({"address.coord":{$type:1}})

- 30.
  db.restaurants.find({"grades.score":{$mod:[7,0]}},
  {"restaurant_id":1,"grades":1,name:1,_id:0})

- 31.
  db.restaurants.find({name:/.*mon.*/},
  {name:1,"borough":1,"address.coord":1,"cuisine":1,_id:0})

- 32.
  db.restaurants.find({name:/^Mad/},
  {name:1,borough:1,"address.coord":1,cuisine:1,_id:0})
  
```