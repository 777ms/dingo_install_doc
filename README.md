# dingo_install_doc


### 手动添加 "dingo/api": "2.0.0-alpha2"


```
"require": {
    "php": ">=7.0.0",
    .
    .
    .
    "viacreative/sudo-su": "~1.1",    # <--- 注意这里需要添加逗号
    "dingo/api": "2.0.0-alpha2"   # <--- 这里没有逗号哦
},
```

`$ composer update`

`$ php artisan vendor:publish` 将配置信息导入到 config 文件夹

常规会把类似于以下的配置添加到 ./.env 文件中
```
API_STANDARDS_TREE=prs
API_SUBTYPE=laravel
API_PREFIX=api
API_VERSION=v1
API_DEBUG=true
```
鉴于线上环境项目维护者可能没有 root 权限，所以尽量不要再添加环境变量

### 如果是通过 git clone 将项目克隆到本地，则可以通过，在 ./.env.example 中添加

```
# dingo config
API_STANDARDS_TREE=
API_SUBTYPE=
API_PREFIX=
API_VERSION=
API_DEBUG=

```