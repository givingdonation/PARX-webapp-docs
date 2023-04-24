---
id: ex966vi1oz5kuhdxqzl8nyi
title: multiTplExec
desc: ''
updated: 1682332994086
created: 1682322170935
---

`tplExec(w http.ResponseWriter, filename string, information any, filename2 string) error`
# Purpose
Different version of [[main_APIs.tplexec]], used for when you need multiple templates to be parsed at once, so that you can use nested gohtml templates (components).
# Parameters
+ w - writer for http response
+ filename - gohtml template to be parsed
+ information - data for Execute
# Example
```go
err = tplExec(writer, "teacher_events.gohtml", events)
```
in: `TeacherEvents.go`

# code
```go
func tplExec(w http.ResponseWriter, filename string, information any) error {
	temp := template.Must(template.ParseFiles("./WebPages/" + filename))

	err := temp.Execute(w, information)
	if err != nil {
		return err
	}
	return nil
}
```