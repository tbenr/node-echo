node-echo
=========

node.js echo server, returns request data to response

## openshift commands:

### create yaml template
```
oc new-app https://github.com/tbenr/node-echo.git --name=echonjs-a \
    -e OPENSHIFT_NODEJS_PORT=8080
    -o yaml > app.yaml
```

note: changing default port 8080 requires to change service port in yaml

### create app (build\deploy)
```
oc create -f app.yaml
```

### remove app (delete bc and service)
```
oc delete -f app.yaml
```