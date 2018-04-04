# Installation

1. Install nodejs

```
NODE_VSN=v8.9.3
wget -O node.tgz https://nodejs.org/dist/${NODE_VSN}/node-${NODE_VSN}-darwin-x64.tar.gz
tar -zxf node.tgz -C bin --strip=2 node-${NODE_VSN}-darwin-x64/bin/node
```
2. Initialize git submodules

```
git submodule init && git submodule update
```
3. Install alfred

```
docker run --rm -it -v "$PWD":/usr/src/app -w /usr/src/app golang bash
GOPATH=/usr/src/app/build GOOS=darwin GOARCH=amd64 go get github.com/kcmerrill/alfred
cp ../build/bin/darwin_amd64/alferd bin/
```
