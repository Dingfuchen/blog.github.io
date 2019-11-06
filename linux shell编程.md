##linux简单脚本
***
###1. eval
将linux命令行以参数形式传到一个中间变量中，使其得以正常运行。如下命令会报错
```shell
set vcom = 'ls -l ; date'
$vcom
```
改为使用eval命令：
```shell
set vcom = 'ls -l ; date'
eval $vcom
```
得到正确执行结果。 
***   
###2. set  
***
###3. cut
将一行字符串根据分隔符进行解析。
```shell
-d ";" #将;作为分隔符
-f 3- #获取从第三个到最后一个字段
-f 1-3 #获取第一个到第三个字段
```
***
###4. 