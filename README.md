# 引入国密php版本的package

1. composer.json文件增加内容

```json
{
    "repositories": [
        {"type": "composer", "url": "https://repo.packagist.com/summer-guomi-php/"},
        {"packagist.org": false}
    ]
}
```

2. 增加auth.json文件

```shell
composer config --auth http-basic.repo.packagist.com cymsummer packagist_uut_874f4c157139c53a836b47bc1d3c99300f6026f4f0b41c1411c08f0b335601cde454
```

3. 更新composer.lock文件

```shell
composer update mirrors
```

4. 使用composer命令引入国密扩展库
```shell
composer require summer/guomi
```