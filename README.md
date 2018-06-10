### Install
```
git submodule add --name protocol git@github.com:neronmoon/Bullet_protocol.git protocol
git submodule update --init
```

### For python
```
protoc --python_out=. protocol/*.proto
```
