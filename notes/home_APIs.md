---
id: 9qq6567yjjk7wk7nyi3i5sl
title: home_APIs
desc: ''
updated: 1682325810211
created: 1682321854459
---

# home.go
Where all the handlers for the teacher side are 

## APIs:
### Utils:
1. [[main_APIs.multiTplExec]]

## Structs
### HomeData
Used to store the data displayed on home.gohtml.

### PrizeData
The prizes for the different grades names and the points required.

## Interfaces
### StudentPageHandlers
#### GETStudentHandler
`GETStudentHandler(writer http.ResponseWriter, request *http.Request)`
### Implimentations
1. EventInfo
2. HomeData