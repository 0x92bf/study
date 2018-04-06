##windows安装(目前版本2.0.14)
* 下载composer
* composer require "fxp/composer-asset-plugin:^1.2.0"
* 命令行运行composer create-project --prefer-dist yiisoft/yii2-app-advanced project2

##初始化项目
* cd project2
* init (0开发模式;1生产模式)

##安装swagger
* 根目录下composer.json require增加 "zircote/swagger-php": "^2.0"
* 运行 composer update
* swagger-ui文件放入根目录

##iis配置
* 设置header  Access-Control-Allow-Headers:*

##controller 方法运行顺序
* init
* actions
* beforeAction
* behaviors
* 自定义方法 

##gii命令行
```yii gii/model --ns=common\models --tableName=d_stock --modelClass=Dstock```

```yii gii/controller --baseClass=\yii\rest\ActiveController --controllerClass=mobile\controllers\DstockController```

##RBAC
* 数据库迁移
components 内添加 
```
'authManager' => [
                 'class' => 'yii\rbac\DbManager',
                          ],
```
```
php yii migrate/up --migrationPath=@yii/rbac/migrations
```
