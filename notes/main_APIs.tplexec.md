---
id: 5cc2ve9qkeeglp1tx423zyg
title: tplexec
desc: ''
updated: 1682287056675
created: 1682286708358
---


# code (go)
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