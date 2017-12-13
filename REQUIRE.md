#require路径问题
## 相对路径
./a/a.php

../common.php

相对路径需要一个参考目录才能确定文件的最终路径，在包含解析中，不管包含嵌套多少层，这个参考目录是程序执行入口文件所在目录。

##绝对路径
/a.php

c:/a.php

##未确定路径
a/a.php

common.inc.php

>开始以为这也是相对路径，但在php的include/require包含机制中，这种类型的路径跟以 . 开头的相对路径处理是完全不同的。require './a.php' 和 require 'a.php' 是不同的！

`function import($path) { 
     $old_dir = getcwd();        // 保存原“参照目录”
     chdir(dirname(__FILE__));    // 将“参照目录”更改为当前脚本的绝对路径
     require_once($path);
     chdir($old_dir);            // 改回原“参照目录”
 }`