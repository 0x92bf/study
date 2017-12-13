# 一级标题
##二级标题
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
###三级标题
* 1
* 2
* 3
![图片](地址)

[教程](http://www.jianshu.com/p/1e402922ee32/)



***
>这是引用

*粗体*

`protected function write($level,$msg)
 	{
 		if(($level & $this->level) == $level )
 		{
 			$msg = '['.date('Y-m-d H:i:s').']['.$this->getLevelStr($level).'] '.$msg."\n";
 			$this->handler->write($msg);
 		}
 	}`