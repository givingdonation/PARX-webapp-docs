---
id: rdsertz920b7ipcdong4bzo
title: main_APIs
desc: ''
updated: 1682337654113
created: 1682286667269
---

# main.go
Where all the handlers for the teacher side are called, and util functions are defined. Central go file for the program. Database is also opened (with `initdb`).

## APIs:
### Utils:
1. [[main_APIs.tplexec]]
2. [[main_APIs.hashPswd]]
## Interfaces
### TeacherPageHandlers
#### GETHandler
`GETHandler(writer http.ResponseWriter, request *http.Request)`

#### POSTHandler
`POSTHandler(writer http.ResponseWriter, request *http.Request)`

#### valHandler
`valHandler(writer http.ResponseWriter, request *http.Request)`

#### dataVal
`dataVal(requestMethod string) bool`

### Implimentations
1. EventInfo - teacherEvents.go
2. Prize - Prizes.go
3. UserData - LoginSignup.go
4. Winners - winners.go