---
id: 5cc2ve9qkeeglp1tx423zyg
title: tplexec
desc: ''
updated: 1682330180670
created: 1682286708358
---

`tplExec(w http.ResponseWriter, filename string, information any) error`
# Purpose
Parses gohtml templates, and with the struct information, it makes an http response.
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