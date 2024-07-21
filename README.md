# vue_test

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### bugs 1: yarn 安装依赖 报 error Error: certificate has expired

问题原因：HTTPS 证书验证失败 ，解决方案就是跳过校验 执行命令

yarn config set "strict-ssl" false -g

转自：https://zhuanlan.zhihu.com/p/685336907
