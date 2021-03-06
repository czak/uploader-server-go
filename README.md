# uploader-server-go
First project in Go for https://github.com/czak/uploader app


# starting

Install [go](https://go-lang.org) & run command: `go run uploader.go`

# starting with Docker

```
docker build -t uploader-server-go .
docker run -d -p 8080:8080 --name uploader-server uploader-server-go
```

# testing:

Use this `curl` for uploading sample:

```
curl -i  http://localhost:8080/upload/ -XPOST -F image=@sample.png
HTTP/1.1 100 Continue

HTTP/1.1 200 OK
Date: Fri, 17 Jul 2015 09:12:53 GMT
Content-Length: 127
Content-Type: text/plain; charset=utf-8

{"link":"http://localhost:8080/image/ba682fcc5026599799eaf72cf9ee23fc-sample.png","filename":"sample.png","Time":1437124373475}
```

To examinate upload use command and see your image in browser.

```open http://localhost:8080/image/ba682fcc5026599799eaf72cf9ee23fc-sample.png```

(c) Copyright 2015 RaVbaker

This piece of software is provided as is. No warranty.
