---
id: qb123iarkm1hwes6mvxjna8
title: hashPswd
desc: ''
updated: 1682333308280
created: 1682319457660
---

`hashPswd(pwd string) string`
# Purpose
Hashes passwords so they can be stored in the database.
# Parameters
+ pwd - the password being hashed
# Example
```go
u.passwordHash = hashPswd(request.FormValue("password"))
```
in: `LoginSignup.go`

# code
```go
func hashPswd(pwd string) string {
	hasher := sha256.New()
	hasher.Write([]byte(pwd))
	sha := base64.URLEncoding.EncodeToString(hasher.Sum(nil))
	return sha
}
```