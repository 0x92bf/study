#环境搭建
* 安装nodejs
* 安装CNPM  `npm install -g cnpm --registry=https://registry.npm.taobao.org`
* 安装CLI   `cnpm install -g @angular/cli`
* 在CMD中切换到工作目录，然后执行以下命令 cnpm install
* 执行ng serve进行测试

#目录分析
package.json npm工具配置文件
angular-cli.json  命令行配置文件
karma 单元测试追踪器，自动化测试
node_modules 第三方依赖文件

src/assets 存放静态资源
src/environments/environment.prod.ts 配置文件
src/main.ts  脚本的入口点
src/polyfills.ts 配置导入库文件

#编译项目
* 指定编译根目录  `ng build --base-href /admin/dist/`