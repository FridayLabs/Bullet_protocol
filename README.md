### Install
```
git submodule add --name protocol git@github.com:neronmoon/Bullet_protocol.git protocol
git submodule update --init
```

### For python
```
find protocol -type f -name "*.proto" -exec protoc --python_out=. {} \;
```
