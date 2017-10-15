集成了 [图灵](http://www.tuling123.com/) 官方的Api接口。

## 安装

 1. 安装包文件

	``` bash
	$ composer require jormin/laravel-tuling
	```

## 配置

1. 注册 ServiceProvider:
	
	```php
	Jormin\TuLing\TuLingServiceProvider::class,
	```

2. 创建配置文件：

	```shell
	php artisan vendor:publish
	```
	
	执行命令后会在 `config` 目录下生成本扩展配置文件：`laravel-tuling.php`。
	
3. 在 `.env` 文件中增加如下配置：

	- `TULING_API_KEY`：图灵ApiKey。

## 使用

1. 获取自动回复信息
    
    ```php
       $message = '西安天气'；
       $userID = '用户ID';
       Jormin\TuLing\TuLing::chat($message, $userID);
    ```
    
    消息字段详细见 [图灵官方文档](http://www.tuling123.com/help/h_cent_webapi.jhtml?nav=doc).

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
