
> 搬运整理，原作者不详

# FileUtil PHP文件操作

PHP Library for simple to create/move/delete file/dir


## Install 

```
composer require jaeger/file-util
```

## Examples
```php
<?php
 use Jaeger\FileUtil;

 //测试建立文件夹,建一个a/1/2/3文件夹
 FileUtil::createDir('a/1/2/3');   

 //测试建立文件,在b/1/2/文件夹下面建一个3文件
 FileUtil::createFile('b/1/2/3'); 

 //测试建立文件,在b/1/2/文件夹下面建一个3.exe文件
 FileUtil::createFile('b/1/2/3.exe'); 

 //测试复制文件夹,建立一个d/e文件夹，把b文件夹下的内容复制进去
 FileUtil::copyDir('b','d/e');      

 //测试复制文件,建立一个b/b文件夹，并把b/1/2文件夹中的3.exe文件复制进去
 FileUtil::copyFile('b/1/2/3.exe','b/b/3.exe');

 //测试移动文件夹,建立一个b/c文件夹,并把a文件夹下的内容移动进去，并删除a文件夹
 FileUtil::moveDir('a/','b/c');   

 //测试移动文件,建立一个b/d文件夹，并把b/1/2中的3.exe移动进去
 FileUtil::moveFile('b/1/2/3.exe','b/d/3.exe'); 

 //测试删除文件,删除b/d/3.exe文件
 FileUtil::unlinkFile('b/d/3.exe');

 //测试删除文件夹,删除d文件夹
 FileUtil::unlinkDir('d');     
                  
```
